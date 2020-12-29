# PostgreSQL のメモ

メモします。

ソースコードでデータベースを扱う際は、typeを必ず指定する。

ポート 5432/tcp を使用。

## インストール

```
$ sudo apt install -y postgresql-10
```

PostgreSQL をインストールします。

## パスワードの設定

```
$ sudo su - postgres
```

`postgres` というユーザでログインします。

```
$ psql 
```

PostgreSQL のターミナル型フロントエンドを起動します。

```
$ alter role postgres with password 'ここにパスワードを入力';
```

パスワードを変更します。　`ALTER ROLE` と表示されれば成功です。

## データベースの作成

```
$ create database hoge;
```

このコマンドで、 `hoge` という名前のデータベースが作成されます。　`CREATE DATABASE` という表示がされれば、データベースの作成をすることができました。
