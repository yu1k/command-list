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
$ nvm install v12.18.2
```

```
$ nvm use v12.18.2
```

上二つのコマンドを実行する。今回は v12.18.2をインストールします。

```
$ node -v
```

Node.jsのバージョンが表示されたらインストールが完了です。
