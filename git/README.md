## Gitについて

### デフォルトブランチを変えた場合

ローカルに変更前の clone がある場合は、次のコマンドを実行して更新する。

```
$ git branch -m main master
$ git fetch origin
$ git branch -u origin/master master
```
