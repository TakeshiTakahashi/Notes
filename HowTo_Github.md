# Git Usage Memo

ローカルにリポジトリを作成し、それをgithubにupするというユースケースと、すでにgithubに存在するコードをローカルに落としてきて作業するというユースケースがあるが、ここでは前者について説明する。

## Gitをまずは個人で利用してみる

### まずはgit自体の設定

git config --global user.email tt2@rc5.so-net.ne.jp
git config --global user.name "Takeshi Takahashi"

### リモートのアドレスをoriginに設定

git remote add origin リモートアドレス
ex. git remote add origin https://github.com/TakeshiTakahashi/AcronymGenerator.git

尚、将来的にこのアドレスを変更したい場合には、addの代わりにset-urlを利用する。


### ローカルにリポジトリを作成

git init
git add *
(git add file.pyなどでもok)
git status (状況確認)
git commit -m "initial commit"     

### githubに更新をpush

git push origin master

これは、originというレポジトリの場所にあるmasterというブランチに、pushするという意味である。
但し、上記のoriginについては上述の手順に従い、事前に設定をしておく必要有。

### remoteからローカルに最新版をダウンロード

git pull

ローカルにリポジトリがなく、remoteリポジトリをごっそり持ってくる際には、下記のcloneコマンドを実施

git clone  <uri>
e.g.,  git clone https://github.com/TakeshiTakahashi/AcronymGenerator.git


## 他の人との共同作業

他の人が既にサーバ上のファイルを編集済みであると、pushをした際に、下記のようなエラーが出る。

error: failed to push some refs to 'https://github.com/milewg/draft-ietf-mile-joniodef.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

pullしてからpushする必要がある。

## 複数githubアカウント利用時の注意

### githubの利用アカウントを変更

Windowsでは、資格情報マネージャーというものがあり、ここで古いgithubのログイン情報を削除すればok

