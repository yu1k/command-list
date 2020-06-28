# クライアントマシンから、VPSや仮想マシンの開発環境にSSHで接続して、VSCodeでコードを書けるようにします

## 環境

クライアントマシン : macOS

リモートマシン : Ubuntu18.04 LTS

### 認証

SSHキーペアは作成してある。

公開鍵は、リモートマシンの ~/.ssh/においてある。

### パーミッション設定

クライアントマシンの秘密鍵が入ったファイルに700の権限を渡してある。

リモートマシンの公開鍵のファイルに600の権限を渡してある。

# つぎ

パスワード認証を禁止してある

### $sudo su

上のコマンドで、rootではいれる。

### vim /etc/ssh/sshd_config

で、sshd_configを開く。

ssdd_configの、

```PasswordAuthentication yes```

から、

```PasswordAuthentication no```

に書き換える。

SSHで使うポート、rootユーザでのSSH接続の設定は必要に応じて変える。


## はじめに

VSCodeでRemote Development拡張をインストールします。

Commandキー + Shiftキー + Pキー を押し、

Remote-SSH: Open Configuration File...

を押し、/User/home/.ssh/config を選択。

```
# Read more about SSH config files: https://linux.die.net/man/5/ssh_config
Host my-machine
    HostName [IPアドレス]
    Port [ポート番号]
    User username
    IdentityFile /Users/username/.ssh/id_rsa
```

こんな感じにします。

IdentityFileには公開鍵認証で使う、秘密鍵のパスを書きます。

## 接続

Commandキー + Shiftキー + Pキーを押し、

``` 
Remote-SSH: Connect to Host...
```

を選択し、接続したいホストを選ぶと接続できる。
