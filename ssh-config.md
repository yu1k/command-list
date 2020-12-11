# SSHの設定

## 環境

Ubuntu18.04

bashシェル

SSHで使用したいポートは開放しておく

## はじめに

```
$ ssh-keygen
```

でクライアント側で公開鍵キーペアを作成する。

# リモート側

```
$ mkdir ~/.ssh
```

し、

```
chmod 700 ~/.ssh
```

で権限を渡す。

```
cd ~/.ssh
```

先ほど作成した、~/.ssh にはいる。

```
touch .ssh/authorized_keys
```

.ssh/authorized_keys を作成し、リモート側に公開鍵を移したあと、

```
chmod 600 ~/.ssh/authorized_keys
```

その後、

```
$ sudo su -
```

で root でログインする。

```
$ vim /etc/ssh/sshd_config
```

で sshd_config を開く。

ちなみに vi で開いたら、編集できませんでした...。

以下の設定をする。

### SSHで使用するポートを変更する

```
#Port 22
```

から、

```
Port [任意のポート番号]
```

に変更する

### パスワード認証をオフにする

```
PasswordAuthentication yes
```

から

```
PasswordAuthentication no
```

に変更する。

### 公開鍵認証を設定する
```
#PubkeyAuthentication yes
```

から

```
PubkeyAuthentication yes
```

に変更する。

### ssh

```
$ /etc/init.d/ssh restart
```

上のコマンドで sshd のサービスを再起動させる。

SSHで使うポート、rootユーザでのSSH接続の設定は必要に応じて変える。

### TODO

- root でログインできないようにする

- 設定を自動化させたい
