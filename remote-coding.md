# VPSやリモートサーバ、仮想マシン などの開発環境に対してSSHで接続して、VSCodeでコードを書けるようにします

## 環境

クライアントマシン : macOS

リモートマシン : Ubuntu18.04 LTS

この [設定](https://github.com/yu1k/note/blob/master/ssh-config.md) を完了してある。

## VSCodeでの設定方法

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
