## nvmをインストールする

```
$ curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.34.0/install.sh | bash
```

サーバ上で取得したプログラムをパイプを使ってシェルで実行する

```
$ source ~/.bashrc
```

.bashrc をいますぐ読み込む

```
$ nvm 
```

nvmと入力し、使い方が表示されたらOK。

## nvmでNode.jsのインストール

```
$ nvm install v10.14.2
```

```
$ nvm use v10.14.2
```

上二つのコマンドを実行する。今回は v12.18.2をインストールします。

```
$ node -v
```

Node.jsのバージョンが表示されたらインストールが完了です。

# yarn のインストール

続いて、Node.js のパッケージマネージャ yarn のインストール をします。

yarn については各自調べる。

```
$ curl -o- -L https://yarnpkg.com/install.sh | bash -s -- --version 1.21.1
```

上のコマンドで yarn をインストールします。

```
$ source ~/.bashrc
```

インストールが終わったら、上のコマンドで設定を再読み込みします。

```
$ yarn --help
```

上のコマンドで yarn の使い方が表示されます。

以上で yarn のインストールが完了しました。