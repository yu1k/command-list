# VSCodeについて

環境は主に macOS です。

VSCode は日本語に設定しています。

### ターミナルから VSCode を起動できない場合

ターミナルから VSCode を起動する場合 `$ code .` などのコマンドで起動する。

できない場合はパスが通っていないと考えられます。

- 以下の手順でパスを通します

1. VSCode を起動し、`Shiftキー` + `Commandキー` + `Pキー` を選択しパレットを表示する
2. パレットの入力欄に `shell` と入力する
3. 出てきた `Shell Command: Install "Code" command in PATH` を選択 
4. 3の操作をしたあとに、 `シェル コマンド 'code' が PATH に正常にインストールされました。` という alert（） の実行が表示されたら設定完了
