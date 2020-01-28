# command-list

## LinuxとかMacで使えるコマンドをまとめておくリストです

コマンドのオプションとかは必要な時に調べる<br>
だいたい コマンド --helpすれば表示される.<br>
シェルにコマンドやファイル名を入力するときは3文字くらい入力したら,タブ補完を使うと便利.

### $history
コマンド入力履歴が見れる<br>
### $ls
今いる階層の中身(？)が表示される<br>
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
### vagrant up
仮想環境を起動する<br>
### vagrant status
仮想環境のステータスを確認する<br>
### vagrant ssh
仮想環境にsshするコマンド
### vagrant halt
仮想環境のシステムを終了する

# ネットワーク
### $ping IPアドレス　
pingした相手先のホストが生きてるか確認できる.<br>
### stat hoge
ファイルのタイムスタンプを表示<br>
### nslookup ドメイン
IPアドレスを調べる<br>
### nmap IPアドレス
ポートスキャンできる
### netstat
ホストのネットワーク統計や状態を確認するコマンド<br>
### tcpdump
通信のパケットをキャプチャし、その結果を出力する<br>
### tcpdump -nn port xxx
ポートを指定できる<br>
### tcpdump -nn -x port xxx
-xをつけるとパケットの中身も表示<br>
###
