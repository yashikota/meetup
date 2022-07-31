# VSCodeのターミナルにc1-byodを追加する

1. VSCode上で```Ctrl + Shift + P``` を押す
2. ```settings``` と入力する
3. ```基本設定: 設定(JSON)を開く``` を押す
4. ```terminal.integrated.profiles.windows``` と書かれた場所を探す(Ctrl + F で検索できる)
5. ```"terminal.integrated.profiles.windows": {``` の括弧の右で改行して下のコードをコピペする  
   ※ただし"path"の部分はc1-byodのインストール先によって異なるので自分で書き換えること  
   下のコードは```C:\Users\ユーザー名\env\```にc1-byodをインストールしている例  
   ユーザーディレクトリの場合は```"${env:USERPROFILE}\\c1-byod\\msys64\\usr\\bin\\bash.exe"```になる  
   ドキュメントディレクトリの場合は```"${env:USERPROFILE}\\Documents\\c1-byod\\msys64\\usr\\bin\\bash.exe"```になる  

```json
"c1-byod": {
 "path": [
   "${env:USERPROFILE}\\env\\c1-byod\\msys64\\usr\\bin\\bash.exe"
 ],
 "args": [
   "--login"
 ],
 "env": {
   "MSYSTEM": "MINGW64",
   "CHERE_INVOKING": "1"
 }
},
```

VSCodeを再起動して```Ctrl + @```を入力してc1-byodが起動するか、```+ ˅```の```˅```を押して、c1-byodがあれば設定完了
