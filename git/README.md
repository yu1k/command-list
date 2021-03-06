# Gitについて

## 目次

- [ブランチ削除](https://github.com/yu1k/note/blob/master/git/README.md#%E3%83%96%E3%83%A9%E3%83%B3%E3%83%81%E5%89%8A%E9%99%A4)
- [開発用ブランチにデフォルトブランチの最新バージョンを取り込む](https://github.com/yu1k/note/blob/master/git/README.md#%E9%96%8B%E7%99%BA%E7%94%A8%E3%83%96%E3%83%A9%E3%83%B3%E3%83%81%E3%81%AB%E3%83%87%E3%83%95%E3%82%A9%E3%83%AB%E3%83%88%E3%83%96%E3%83%A9%E3%83%B3%E3%83%81%E3%81%AE%E6%9C%80%E6%96%B0%E3%83%90%E3%83%BC%E3%82%B8%E3%83%A7%E3%83%B3%E3%82%92%E5%8F%96%E3%82%8A%E3%81%93%E3%82%80)

### デフォルトブランチを変えた場合

ローカルに変更前の clone がある場合は、次のコマンドを実行して更新する。

```
$ git branch -m main master
$ git fetch origin
$ git branch -u origin/master master
```

### ローカルにあるディレクトリを Git 管理し、GitHubに push するまで

前提：Git管理する予定のディレクトリ以下のPATHにいることを前提とする

```
$ git init
$ git add .
$ git commit -m "Initial commit"
```

ここで GitHub で Git管理する予定のディレクトリ名と同じリポジトリ名の 空リポジトリを作成する。

```
$ git remote add [リポジトリ名] git@github.com:username/[リポジトリ名].git
$ git push -u [リポジトリ名] [ブランチ名]
```

以上で GitHub で管理できるようになる。

### ブランチ削除

```
$ git branch
```

ローカルにあるブランチの確認

```
$ git branch -D [branch]
```

ローカルブランチの削除

### 開発用ブランチにデフォルトブランチの最新バージョンを取りこむ

mainをデフォルトブランチとする

development を開発用ブランチとする

1. $ git checkout main
2. $ git pull origin main

mainブランチへ移動し、 `git pull` でリモートの最新バージョンをローカルに持ってくる

3. $ git checkout development

developmentブランチへ移動

4. $ git merge origin main

main ブランチの内容を development ブランチへ取り込む

