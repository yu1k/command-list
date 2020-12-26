# PostgreSQL のメモ

メモします。

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
