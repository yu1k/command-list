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
### $cd hoge
ディレクトリ移動<br>
### $mkdir hoge
ディレクトリ作成<br>
### $cat hoge.hoge
ファイルを連結するためのコマンド.ファイルの内容を表示することができる.<br>
### $touch hege.hoge
ファイルのタイムスタンプを更新, 指定したファイルがない場合は、サイズが0のファイルが作成される<br>
### $vim hoge.hoge
vimでファイルを編集できる<br>
### $rm -r hoge
ファイルやディレクトリを削除できる<br>
### $g++ -o hoge hoge.hoge
gccでコードをコンパイルするコマンド<br>
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
Rubyのコードが実行できる<br>

## Vagrantのコマンド
### $vagrant up
仮想環境を起動する<br>
### $vagrant status
仮想環境のステータスを確認する<br>
### $vagrant ssh
仮想環境にsshするコマンド
### $vagrant halt
仮想環境のシステムを終了する

## gitのコマンド
### $git clone https://github.com/hoge
リポジトリのクローン
### $git status
何を更新したか確認する
### $git add.
gitを予約(?
#### $git reset 
git addを取り消せる
### $git commit -m "何を更新したか"
gitにコミット, 
### $git push origin master
gitにpushする.

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
### $ipconfig
ネットワークの設定が確認できる.IPアドレスを確認したいときによく使う.<br>

## tmux
### $tmux 
tmuxを起動
<br>
ctrl + b を押した後にdを押すと終了できる.
### $tmux a
アタッチ, 接続する.さっき抜けたtmuxの仮想端末に戻れる.
