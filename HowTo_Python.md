# Python Usage memo

ここでは、Pysonでのprogrammingのtipsを記載する。
現時点では、python 2.7をベースに記述するものとする。

# Pythonのインストールに関するメモ

まずは、pyenvをインストール。  
http://qiita.com/hiroseabook/items/e883e562fb7fddcfeec9  
上記を参考にして実施。但し、exec $SHELLはうまくいかなかったため、sourceコマンドを使って直接設定ファイルを読んだ。
  ```source ~/.bash_profile```


pyenvインストールの動作確認は下記のコマンドが良い  
  ```pyenv install --list```

実際に、インストールしたいバージョンを選んで、pythonをインストール  
  ```pyenv install 3.4.6```



# Windowsへのインストールメモ

Python 2.7.13が入っている状態から、Python 3.6.5をインストールした。
参考にしたURLは下記の通り。  
https://web.plus-idea.net/2017/02/python2-3-venv-virtualenv/  
結果、pyコマンドを利用して切り替え可能となった。

ページを読み込んで吐き出す際に、文字化けが生じる現象については、下記リンクを見て対応  
https://kanji.hatenablog.jp/entry/python-requests-beautifulsoup-encoding

Jupyterをインストールしようとしているときに、Anacondaの存在を知る。Anacondaは多くのパッケージを事前にセットアップしてくれているPythonの環境らしい。

# 必要なlibraryのインストール

pandasなど、必要なlibraryをインストールする際には、pipを活用。下記のリンクが参考になる。

https://qiita.com/mojaie/items/241eb7006978e6962d05

但し、pyを利用している際には、

```py -3 -m pip install pandas```

のようになる点に注意。
また、環境によっては管理者権限を持たせて実行しないとエラーとなる。
