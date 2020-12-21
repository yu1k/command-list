# command-list

## LinuxとかMacで使えるコマンドをまとめておくリストです

コマンドのオプションとかは必要な時に調べる<br>
だいたい コマンド --helpすれば表示される.<br>
シェルにコマンドやファイル名を入力するときは3文字くらい入力したら,タブ補完を使うと便利.

### $history
コマンド入力履歴が見れる<br>
### $ls
今いる階層の中身(？)が表示される<br>
オプション :<br>
-a > ドットファイルも表示する<br>
-l > 長いフォーマットで表示する<br>

-lh > ファイルなどのサイズを表示してくれる

### $cd hoge
ディレクトリ移動<br>
### $mkdir hoge
ディレクトリ作成<br>
### $cat hoge.hoge
ファイルを連結するためのコマンド.ファイルの内容を表示することができる

### $ less [ファイル名]

ターミナルを流さずに、ファイルの中身を表示させることができる。終了するときは Qキー 押す

### $touch hege.hoge
ファイルのタイムスタンプを更新, 指定したファイルがない場合は、サイズが0のファイルが作成される<br>
### $vim hoge.hoge
vimでファイルを編集できる<br>
### $rm -r hoge
ファイルやディレクトリを削除できる<br>
### $g++ -o hoge hoge.hoge
g++でコードをコンパイルするコマンド<br>

### $ man <関数名>

C言語の関数のなどの情報をリファレンスマニュアルから調べることができる。

### $./hoge
コンパイルしたコードを実行するコマンド<br>
### $exit 
プロセスを終了する.ログアウトする.<br>
### $pwd 
現在の作業ディレクトリを表示するコマンド, /home/vagrant/workspace/cpp-study cpp-studyで作業しているときはこんな感じで表示される.
### $mv hoge.c ../fuga/
hoge.cがいまhogeディレクトリにあるとする.このコマンドを使えばfugaディレクトリに移動できる.
### $clear 
シェルをクリア(？)して見やすくできる<br>
### $node hoge.js
hoge.cがいまhogeディレクトリにあるとする.このコマンドを使えばfugaディレクトリに移動できる.
NodeでJavaScriptのコードが実行できる.<br>
### $python hoge.py
Pythonで書いたコードが実行できる.<br>
### $ruby hoge.rb
Rubyのコードが実行できる

## コンピュータのリソースの確認など
sysstatをインストールする.
### $screenfetch
Linuxのディストリビューションのロゴをアスキーアートで表示.
### $top
OSで利用しているプロセスの数や状態、またOS全体のシステムリソース状況を確認できる.
### vmstat
メモリやCPU使用率を確認できる.
### mpstat
各CPUコアにCPU負荷が掛かっているかなどが確認できる.
### ps
現在利用しているプロセス， ストッドごとのCPUやメモリ使用率を確認できる.
### free
メモリに特化して詳細を表示したい場合に使用する.
### lsblk
利用できるブロックデバイスを確認できる.
### iostat
ブロックデバイスごとの負荷状況を確認できる.
### vnstat
ネットワークトラフィック状態を確認することができる. -l オプションをつけるとリアルタイムで確認できる.

### $iostat
I/Oデバイスの使用状況を表示する.


## grep
特手の文字を含む行を抽出する.
### $grep "検索したい文字列" ファイル名
ファイルの中から指定した文字列を抽出して出力する
### $grep "検索したい文字列" ファイル名 -w -2
ファイルの中から指定した文字列を前後2行とともに抽出して出力する.

### $grep -i "検索したい文字列" -n [ファイル名]

- -i : 大文字と小文字を区別しない

- -n : 行番号を表示する


## find

```
find [ファイル名 or ディレクトリ名]
```

ファイル名かディレクトリ名を指定し、そのファイルやディレクトリが存在するか確認できる。

- -empty : ファイル容量が0byteのファイルを対象とし、検索する

- -not : 条件に当てはまらないファイルやディレクトリを検索する


## Vagrantのコマンド
### $vagrant up
仮想環境を起動する<br>
### $vagrant status
仮想環境のステータスを確認する<br>
### $vagrant ssh
仮想環境にsshするコマンド.
### $vagrant halt
仮想環境のシステムを終了する.
### $vagrant reload
仮想環境のシステムを再起動できる.

## gitのコマンド
### $git clone https://github.com/hoge
リポジトリのクローン
### $git status
何を更新したか確認する
### $git add.
gitを予約(?
#### $git reset 
git addを取り消せる
### $git reset --hard HEAD^
直前のgit commitを取り消せる.
### $git commit -m "何を更新したか"
gitにコミット, 
### $git push origin master
gitにpushする.
### $git log
gitの履歴を表示. qを押して終了.
### git remote -v
リモートリポジトリ名が表示される.
### git remote show origin
Gitのリモートリポジトリの更新を確認できる.
実行結果の最終行に(up to date)と表示されていれば最新.(local out of date)と表示されていればローカルの方が古い.
### $git pull
リモートとローカルを同期する.
### $git revert HEAD
直前のcommitを取り消す.

## Gitのブランチ

### $ git branch

Gitのブランチを確認できる。-r オプションをつけると、リモートのブランチを確認できる。

### $ git checkout -b [任意のブランチ名]

新しいブランチを作成できる。

### $ git checkout -b yu1k-remote origin/yu1k-remote

git でリモートリポジトリにすでに存在している yu1k-remote というブランチに切り替えたい場合、 `$ git checkout -b yu1k-remote` では、すでにリモートに存在している yu1k-remote には切り替えられない。新しい、yu1k-remote というブランチがローカルに作成されてしまう。

しかし、上記のコマンドを使用すれば、gitのリモートリポジトリにすでに存在している yu1k-remote というブランチにローカルで切り替えられる。

### $ git checout [任意のブランチ名]

存在している、任意のブランチに変更できる

### $ git push origin [変更をpushしたいブランチ名]

コミットした差分を、任意のブランチにプッシュする。

### $ git commit
`git commit -m "コミットメッセージ"` のような形でもコミットできるけど、 `git commit` コマンドを使用するとエディタが起動し、コミットメッセージを入力できるので比較的長めのコミットメッセージを書きやすい


## gitに自分の情報を登録
### git config --global user.name "あなたの名前"
名前を登録.
### git config --global user.email あなたのメールアドレス
メールアドレスを登録.
### git config --global core.editor "vim"
エディタを登録.
### git config -l
登録内容を確認できる


# ネットワーク
### $ping IPアドレス　
pingした相手先のホストが生きてるか確認できる.<br>

### $ ping -c [	パケットを送信する回数] [ホスト名 or IPアドレス]

-c オプションをつけると、パケット送受信の回数を指定して、パケットを送信することができる。

### $ traceroute [IPアドレス or ホスト名]

操作中の端末から目的のサーバまでのネットワーク経路を調べることができる。

TODO: 途中の経路が米印にならない方法を見つけたい。しかし、ファイアウォールのあれだったら難しそう。

### $stat hoge
ファイルのタイムスタンプを表示<br>
### $nslookup ドメイン
IPアドレスを調べる<br>
### $nmap IPアドレス
ポートスキャンできる
### $netstat
ホストのネットワーク統計や状態を確認するコマンド.どこと通信しているのか,どのポートが空いているのかなどを確認できる.<br>
### $tcpdump
通信のパケットをキャプチャし、その結果を出力する<br>
### $tcpdump -nn port xxx
ポートを指定できる<br>
### $tcpdump -nn -x port xxx
-xをつけるとパケットの中身も表示<br>
### $ifconfig
ネットワークの設定が確認できる.IPアドレスを確認したいときによく使う.<br>
## iptables(パケットフィルタ)
iptablesはパケットを， 4つのテーブルに分けて， それぞれのタイミングで制御する.<br>
テーブルにはfilterテーブル， natテーブル， mangleテーブル， rawテーブルがある.<br>
filterテーブル : パケットの通過や遮断といった制御.<br>
#### $iptables -t filter -p tcp --dport 80 -j -DROP
natテーブル : NAT（ネットワークアドレス変換機能）， 送信先や送信元といったパケットの中身を書き換える際に利用.<br>
各通信をローカルネットワーク上のサーバへ振り分けるルーターとして機能させることができる.<br>
#### $[あとで書く]
mangleテーブル : TOS（Type Of Service)フィールド等の値を書き換える.TOSはパケット処理の優先度付けを行い、通信品質を制御する際に利用.<br>
また， 特定の通信マークを置き換える事もできる.<br>
#### $[あとで書く]
Rawテーブル : mangleテーブルのように特定のパケットにマークを付ける役割. Rawテーブルでは追跡を除外するようマークを付けられる.<br>
特定の通信をファイアウォールで処理せずに他へ通したりといった経路の制御をする場合に利用.<br>
テンプレート : https://www.atmarkit.co.jp/flinux/index/indexfiles/iptablesindex.html

## SSHを使ってファイル転送

### $ sftp user@hostname
最初にリモート側で公開鍵の登録をする。
セッションが開始したあと、
### $ get hoge.txt
sftpセッションが開始したあと、このコマンドを実行すると、hoge.txtというファイルをダウンロードできる。

### $ put hoge.txt
sftpセッションが開始したあと、このコマンドを実行すると、hoge.txtというファイルをアップロードできる。

### $ exit
sftpセッションを終了できる。

## 通信量

### $ iftop 
個別のソケットで、受信/送信パケットを確認できる。iftopをインストールして使用。
どのホストとの通信で、どのくらいの帯域を使用しているか確認するときに使用。

## ネットワーク回線速度

### $ speedtest --server xxxx
speedtest-cliをインストールしたあと、使用できる。

xxxxの部分にサーバーのIDの番号を入力する。

### $ speedtest --list
サーバー一覧を表示させることができる。

### $ speedtest --list | grep Japan
日本のサーバーの一覧を確認できる。

## ファイル

### $ mkfile xx hoge.txt 
指定したサイズの空のファイルを作成できる。

xxの部分にファイルのサイズを入力する。

### 単位 

>  b

Byte

> k

KB

> m

MB
> g

GB

## ARP
#### $arp -a
ARPテーブルの表示

## ファイアウォール
### $sudo ufw status
ファイアウォールが設定されているか. 表示 : active || inactive
### $sudo ufw allow [任意のポート番号]
ポートを開放できる.
### $sudo ufw deny [任意のポート番号]
### $sudo ufw reload
ファイアウォールを再起動できる.
### $sudo ufw enable
システムでファイアーウォールを有効にする.
### $sudo ufw disable
システムでファイアーウォールを無効にする.
### $sudo ufw default DENY
すべてのポートを閉じる.
### $sudo ufw default ALLOW
すべてのポートを開く.
## ファイアウォール開放手順
#### $sudo ufw allow [任意のポート]
#### $sudo ufw reload
#### $sudo ufw status


## Ubuntu初期設定
### $sudo locale-gen ja_JP.UTF-8
日本語環境を作成.

### $echo export LANG=ja_JP.UTF-8 >> ~/.profile
マシンを起動に日本語環境で起動する設定.

### $source ~/.profile
反映させる.

### $sudo timedatectl set-timezone Asia/Tokyo
タイムゾーンを初期設定のUTCからAsia/Tokyoに変更.

### $cat /etc/group | grep sudo
権限の確認

## パスワード変更
### $passwd
自分自身のパスワードを変更できる.

### $passwd username
指定したユーザーのパスワードを変更できる. このコマンドはrootユーザーのみ実行できる.

### $passwd -S
パスワードの状態を表示する.

