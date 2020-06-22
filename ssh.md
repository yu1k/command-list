# ssh接続でサーバーなどへ接続するとき

## パスワード認証でssh接続をする

ToDo : あとでかく

## 公開鍵認証でssh接続をする

公開鍵認証をする場合、接続する側のマシン(リモコン側)で公開鍵と秘密鍵 (ssh-keygenなどで) を作成し、

公開鍵を 接続される側(サーバー側)のホームディレクトリの下の階層である ~/.ssh に設置する必要がある。 .ssh がない場合は新しく作成する。

ファイル転送

```
$ scp -P 22 ~/.ssh/id_rsa.pub user@hostname:.ssh/authorized_keys
```

接続する側(リモコン側)で作成した公開鍵を、サーバー側に authorized_keys ファイルを作成し、そこに書き込む。

### $ chmod 600 ~/.ssh/authorized_keys

コマンドで公開鍵ファイルに、権限を与えておく。

### クライアント側

/home/user/.ssh/ は700

### リモート側

/home/user.ssh/authorized_keys は600

となるような権限にしておく。

## 接続

### $ ssh -i ~/.ssh/{秘密鍵のファイル} -p {ssh接続で使用するポート} user@hostname
このコマンドでリモート側にssh接続をする
