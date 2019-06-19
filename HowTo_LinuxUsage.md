
----------------------------------------------
Virtualboxの基本操作
----------------------------------------------

Hostキーとして、デフォルトでは右Ctrlキーが割り当てられる。このキーを押すことで、Virtual Boxの中と外を行き来できる。

----------------------------------------------
共通
----------------------------------------------

フォルダ内のファイル数のカウント: ls -Ul|wc -l

nohup  .... &    として実行すれば、ログアウト後もコンピュータの処理は継続される。

----------------------------------------------
CentOS編
----------------------------------------------

CentOSのインストール・初期設定
CentOSをVirtual BoxのGuest OSとしてインストールする際には、一緒に"Guest Additions"というモジュールをインストールしたほうが使いやすい。マウスがintegrateされる。また、Guest OSの解像度が最適化される。(http://qiita.com/SUZUKI_Masaya/items/ac0c9e8eb060f84f25a3)
ショートカットの設定は、無効化されているものも多いので、見直しが必要
日本語入力の設定: gnome状にインプットメソッドが選択できない形になっている際には、IbusとAnthyが利用される形になっているか、確認が必要
音が出ない際には、hypervisor側の設定を見直す。
ネットワーク接続がうまくいかないときには、/etc/sysconfig/network-scripts/ifcfg-xxxファイルの中で、NM_CONTROLLED="no"として、Network Managerを無効にすると、わかりやすくなることもある。


Guest Additionがうまく動作していない場合、下記を実施してみると直ることがある。

cd /opt/VBoxGuestAdditions-*/init  
sudo ./vboxadd setup

但し、上記の/optにVBoxGuestAdditions-*が存在しない場合、対応するisoファイルをダウンロードする必要有。

wget http://download.virtualbox.org/virtualbox/5.0.20/VBoxGuestAdditions_5.0.20.iso

上記のダウンロードするisoファイルは、http://download.virtualbox.org/virtualbox/を見て適宜、正しいものに修正する。


yumの設定
ホスト側のウィルス対策ソフトの設定が必要な場合もある
普通にpingも通り、browserが見れても、yumが通らない場合あり
proxyの設定のケースもあるが、それでもうまくいかないケースあり
symantec endpoint protectionでは、「ネットワーク脅威防止」の項目を修正してうまくいった。
また、yum installやyum update実行前に、yum clean allをすると、うまくいくことがある。
必要に応じて、リポジトリを追加して利用する
yum -y install epel-release

yumが壊れたとき
重複したパッケージを削除するなどを下記のリンクを利用して実施
https://qiita.com/masayuki14/items/d5b190bf90e5cb799880


iptablesの設定
　　"getenforce"で現在のiptablesの稼働状況が分かり、"setenforce 0"でiptablesを止めることができる

selinuxの設定
    /etc/selinuxのファイル内に、selinux disabledを記載することで、selinuxを無効化できる

firewallの設定
   "systemctl stop firewalld.service"で、firewalldを一時的に止めることができる。永続的に止める場合には、stopの代わりにdisableを付ける。

terminalの色設定
    terminalを起動したら、「設定」をクリックして、その中のprofileを作成する。そのprofileの中で色設定をすればOK

[マウント]
共有フォルダのマウント
mount -t vboxsf LinuxShare WinShare
vboxsf stands for virtual box shared file

但し、このままではrootがmountしたものはrootでないと書き込みできないので、オプション指定をする必要有。

mount -t vboxsf -o uid=take Dropbox Dropbox

CDROMのマウント
    mount -t iso9660 -o loop [iso イメージファイル名] /mnt/iso

Webdavフォルダのマウント
    davfs2をapt-getによりインストール。その後、下記のとおりにmountを実施
    mount -t davfs https://dav.box.com/dav webdav_box
    尚、webdav_boxは、任意のディレクトリで構わない。

nfsフォルダのマウント
    Centos 7では、パッケージが必要。
    yum -y install nfs-utils
    mount -t nfs [target host]:[target dir] [local dir]

smbフォルダのマウント (研究室NASのマウント)
    yum install samba-client samba-winbind cifs-utils
    mount.cifs //usl-5p.develop.net/disk1 /mnt/usl-5pm/ -o user=take,pass=xxxxxxxx
    mount.cifs //192.168.0.12/homes/take /mnt/nas -o user=take,pass=password,vers=3.0

    vers=3.0がなぜ必要かはよくわかっていないが、うまくいかないときはこれを付けるとうまくいく

[マウント状況の確認]
cat /etc/mtab

[マウントの解除]
umount /dev/cdrom

[ネットワークの確認]
・トラフィックの確認
     syntax:   tcpdump -nni [interface name]
     e.g.:        tcpdump -nni eth1

・ルーティングテーブルの確認
    netstat -rn

・ルーティングテーブルの変更 (staticな変更)
   /etc/sysconfig/network-scripts/route-eth1
   変更したら、/etc/init.d/network restartを忘れずに実施
   この際に、ifcfg-eth1に、HWADDRが指定されていないと、restartがうまくいかないことがあるので注意

・NIC設定の確認
    /etc/udev/rules.d/70-persistent-net.rules


[ハードウェア情報の確認]

メモリ容量の確認
cat /proc/meminfo

[OpenVPN]
インストールはyumにて実施。但し、epel (enterprise linux)リポジトリを読み込めるようにしておく必要有
起動は、下記の通り。但し、引数の設定ファイル内で、証明書など3種類の指定が必要。
/usr/sbin/openvpn /etc/openvpn/client.ovpn &

[browser install]
Chromeは、下記に従いインストール。但し、非常に重い。
http://www.tecmint.com/install-google-chrome-on-redhat-centos-fedora-linux/


[audio player]
Banshee Media Playerをまずは使ってみる。

[利用するソフト]
  PDF viewer: evince

[強制終了]
ps aux | grep プログラム名
kill プロセスID

killでうまくプロセスを停止できない場合には、kill -9 プロセスIDとすると、強制終了できる。


[MSV]
Schema validator.

yum install msv-xmlgen

Example:
msv -verbose iodef_schema.xsd

msv -verbose iodef-sci.xsd iodef-sci-MTIexample.xml


----------------------------------------------
Kali Linux編
----------------------------------------------


[Kali Linuxのインストール]
Virtualboxでは、Debian 64 bitとしてインストール

[vboxsfタイプのマウント]
apt-getにて、virtualbox-guest-utilsをインストールする必要有。

[Snortのインストール]
Kali Linuxにてインストールを実施した際のメモ。
まずはインストール: apt-get install snort
独自のルールを作成するファイルcustom.rulesを作成
alert icmp any any -> any any (msg:"Test Rule";sid:10001;rev:1;)   これにより、icmp packetがすべてalertとして記録される。
snort.confを編集し、custom.rulesをincludeする
snortを実行: /usr/local/bin/snort -Dd -A full -c /etc/snort/snort.conf -u snort -g snort

Snortログ解析の可視化ツールであるBaseについては、現在インストール中。下記のサイトが参考になる。
https://www.howtoforge.com/intrusion-detection-with-snort-mysql-apache2-on-ubuntu-7.10#-get-base-basic-analysis-and-security-engine


----------------------------------------------
Cygwin編
----------------------------------------------

Xを利用するための手続き
1. apt-cygにてxorg-serverとxinitをインストール
2. run xwin -multiwindow -listen tcp
3. DISPlAY=localhost:0.0;export DISPLAY
3. 確認のため、minttyとxtermで新たなwindowが立ち上がることを確認


TeXのインストールは、下記の通り
apt-cyg install texlive

texcountは下記からダウンロードして利用可能。実体は、perl script。
http://app.uio.no/ifi/texcount/


----------------------------------------------
その他
----------------------------------------------


route add 192.168.1.27 mask 255.255.255.255 192.168.11.46 metric 1
これにより、研究室NASにもアクセス可になる。

