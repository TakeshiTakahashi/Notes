
----------------------------------------------
Virtualbox�̊�{����
----------------------------------------------

Host�L�[�Ƃ��āA�f�t�H���g�ł͉ECtrl�L�[�����蓖�Ă���B���̃L�[���������ƂŁAVirtual Box�̒��ƊO���s�����ł���B

----------------------------------------------
����
----------------------------------------------

�t�H���_���̃t�@�C�����̃J�E���g: ls -Ul|wc -l

nohup  .... &    �Ƃ��Ď��s����΁A���O�A�E�g����R���s���[�^�̏����͌p�������B

----------------------------------------------
CentOS��
----------------------------------------------

CentOS�̃C���X�g�[���E�����ݒ�
CentOS��Virtual Box��Guest OS�Ƃ��ăC���X�g�[������ۂɂ́A�ꏏ��"Guest Additions"�Ƃ������W���[�����C���X�g�[�������ق����g���₷���B�}�E�X��integrate�����B�܂��AGuest OS�̉𑜓x���œK�������B(http://qiita.com/SUZUKI_Masaya/items/ac0c9e8eb060f84f25a3)
�V���[�g�J�b�g�̐ݒ�́A����������Ă�����̂������̂ŁA���������K�v
���{����͂̐ݒ�: gnome��ɃC���v�b�g���\�b�h���I���ł��Ȃ��`�ɂȂ��Ă���ۂɂ́AIbus��Anthy�����p�����`�ɂȂ��Ă��邩�A�m�F���K�v
�����o�Ȃ��ۂɂ́Ahypervisor���̐ݒ���������B
�l�b�g���[�N�ڑ������܂������Ȃ��Ƃ��ɂ́A/etc/sysconfig/network-scripts/ifcfg-xxx�t�@�C���̒��ŁANM_CONTROLLED="no"�Ƃ��āANetwork Manager�𖳌��ɂ���ƁA�킩��₷���Ȃ邱�Ƃ�����B

yum�̐ݒ�
�z�X�g���̃E�B���X�΍�\�t�g�̐ݒ肪�K�v�ȏꍇ������
���ʂ�ping���ʂ�Abrowser������Ă��Ayum���ʂ�Ȃ��ꍇ����
proxy�̐ݒ�̃P�[�X�����邪�A����ł����܂������Ȃ��P�[�X����
symantec endpoint protection�ł́A�u�l�b�g���[�N���Жh�~�v�̍��ڂ��C�����Ă��܂��������B
�܂��Ayum install��yum update���s�O�ɁAyum clean all������ƁA���܂��������Ƃ�����B
�K�v�ɉ����āA���|�W�g����ǉ����ė��p����
yum -y install epel-release

iptables�̐ݒ�
�@�@"getenforce"�Ō��݂�iptables�̉ғ��󋵂�������A"setenforce 0"��iptables���~�߂邱�Ƃ��ł���

selinux�̐ݒ�
    /etc/selinux�̃t�@�C�����ɁAselinux disabled���L�ڂ��邱�ƂŁAselinux�𖳌����ł���

firewall�̐ݒ�
   "systemctl stop firewalld.service"�ŁAfirewalld���ꎞ�I�Ɏ~�߂邱�Ƃ��ł���B�i���I�Ɏ~�߂�ꍇ�ɂ́Astop�̑����disable��t����B

terminal�̐F�ݒ�
    terminal���N��������A�u�ݒ�v���N���b�N���āA���̒���profile���쐬����B����profile�̒��ŐF�ݒ�������OK

[�}�E���g]
���L�t�H���_�̃}�E���g
mount -t vboxsf LinuxShare WinShare
vboxsf stands for virtual box shared file

CDROM�̃}�E���g
    mount -t iso9660 -o loop [iso �C���[�W�t�@�C����] /mnt/iso

Webdav�t�H���_�̃}�E���g
    davfs2��apt-get�ɂ��C���X�g�[���B���̌�A���L�̂Ƃ����mount�����{
    mount -t davfs https://dav.box.com/dav webdav_box
    ���Awebdav_box�́A�C�ӂ̃f�B���N�g���ō\��Ȃ��B

nfs�t�H���_�̃}�E���g
    Centos 7�ł́A�p�b�P�[�W���K�v�B
    yum -y install nfs-utils
    mount -t nfs [target host]:[target dir] [local dir]

smb�t�H���_�̃}�E���g (������NAS�̃}�E���g)
    yum install samba-client samba-winbind cifs-utils
    mount.cifs //usl-5p.develop.net/disk1 /mnt/usl-5pm/ -o user=take,pass=xxxxxxxx
    mount.cifs //192.168.0.12/homes/take /mnt/nas -o user=take,pass=password,vers=3.0

    vers=3.0���Ȃ��K�v���͂悭�킩���Ă��Ȃ����A���܂������Ȃ��Ƃ��͂����t����Ƃ��܂�����

[�}�E���g�󋵂̊m�F]
cat /etc/mtab

[�}�E���g�̉���]
umount /dev/cdrom

[�l�b�g���[�N�̊m�F]
�E�g���t�B�b�N�̊m�F
     syntax:   tcpdump -nni [interface name]
     e.g.:        tcpdump -nni eth1

�E���[�e�B���O�e�[�u���̊m�F
    netstat -rn

�E���[�e�B���O�e�[�u���̕ύX (static�ȕύX)
   /etc/sysconfig/network-scripts/route-eth1
   �ύX������A/etc/init.d/network restart��Y�ꂸ�Ɏ��{
   ���̍ۂɁAifcfg-eth1�ɁAHWADDR���w�肳��Ă��Ȃ��ƁArestart�����܂������Ȃ����Ƃ�����̂Œ���

�ENIC�ݒ�̊m�F
    /etc/udev/rules.d/70-persistent-net.rules


[�n�[�h�E�F�A���̊m�F]

�������e�ʂ̊m�F
cat /proc/meminfo

[OpenVPN]
�C���X�g�[����yum�ɂĎ��{�B�A���Aepel (enterprise linux)���|�W�g����ǂݍ��߂�悤�ɂ��Ă����K�v�L
�N���́A���L�̒ʂ�B�A���A�����̐ݒ�t�@�C�����ŁA�ؖ����Ȃ�3��ނ̎w�肪�K�v�B
/usr/sbin/openvpn /etc/openvpn/client.ovpn &

[browser install]
Chrome�́A���L�ɏ]���C���X�g�[���B�A���A���ɏd���B
http://www.tecmint.com/install-google-chrome-on-redhat-centos-fedora-linux/


[audio player]
Banshee Media Player���܂��͎g���Ă݂�B

[���p����\�t�g]
  PDF viewer: evince

[�����I��]
ps aux | grep �v���O������
kill �v���Z�XID

kill�ł��܂��v���Z�X���~�ł��Ȃ��ꍇ�ɂ́Akill -9 �v���Z�XID�Ƃ���ƁA�����I���ł���B


[MSV]
Schema validator.

yum install msv-xmlgen

Example:
msv -verbose iodef_schema.xsd

msv -verbose iodef-sci.xsd iodef-sci-MTIexample.xml


----------------------------------------------
Kali Linux��
----------------------------------------------


[Kali Linux�̃C���X�g�[��]
Virtualbox�ł́ADebian 64 bit�Ƃ��ăC���X�g�[��

[vboxsf�^�C�v�̃}�E���g]
apt-get�ɂāAvirtualbox-guest-utils���C���X�g�[������K�v�L�B

[Snort�̃C���X�g�[��]
Kali Linux�ɂăC���X�g�[�������{�����ۂ̃����B
�܂��̓C���X�g�[��: apt-get install snort
�Ǝ��̃��[�����쐬����t�@�C��custom.rules���쐬
alert icmp any any -> any any (msg:"Test Rule";sid:10001;rev:1;)   ����ɂ��Aicmp packet�����ׂ�alert�Ƃ��ċL�^�����B
snort.conf��ҏW���Acustom.rules��include����
snort�����s: /usr/local/bin/snort -Dd -A full -c /etc/snort/snort.conf -u snort -g snort

Snort���O��͂̉����c�[���ł���Base�ɂ��ẮA���݃C���X�g�[�����B���L�̃T�C�g���Q�l�ɂȂ�B
https://www.howtoforge.com/intrusion-detection-with-snort-mysql-apache2-on-ubuntu-7.10#-get-base-basic-analysis-and-security-engine


----------------------------------------------
Cygwin��
----------------------------------------------

X�𗘗p���邽�߂̎葱��
1. apt-cyg�ɂ�xorg-server��xinit���C���X�g�[��
2. run xwin -multiwindow -listen tcp
3. DISPlAY=localhost:0.0;export DISPLAY
3. �m�F�̂��߁Amintty��xterm�ŐV����window�������オ�邱�Ƃ��m�F


TeX�̃C���X�g�[���́A���L�̒ʂ�
apt-cyg install texlive

texcount�͉��L����_�E�����[�h���ė��p�\�B���̂́Aperl script�B
http://app.uio.no/ifi/texcount/


----------------------------------------------
���̑�
----------------------------------------------


route add 192.168.1.27 mask 255.255.255.255 192.168.11.46 metric 1
����ɂ��A������NAS�ɂ��A�N�Z�X�ɂȂ�B

