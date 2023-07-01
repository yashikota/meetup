# VSCodeのターミナルにc1-byodを追加する

1. VSCode上で`Ctrl + Shift + P` を押す
2. `settings` と入力する
3. `基本設定: ユーザー設定を開く (JSON)` を押す  
    <img src="/assets/images/vscode/01.png" alt="vscode-branch" width="50%"/>  
4. `terminal.integrated.profiles.windows` と書かれた場所を探す(Ctrl + F で検索できる)
5. 下記のコードを参考にコードをコピペして適切に貼り付け、pathの部分を適切に書き換える  
   ※ただし"path"の部分はc1-byodのインストール先によって異なるので自分で書き換えること  
   下のコードは`C:\Users\ユーザー名\env\`にc1-byodをインストールしている例  

   Cドライブ直下の場合は`"C:\\c1-byod\\msys64\\usr\\bin\\bash.exe"`になる  
   ユーザーフォルダーの場合は`"${env:USERPROFILE}\\c1-byod\\msys64\\usr\\bin\\bash.exe"`になる  
   ドキュメントフォルダーの場合は`"${env:USERPROFILE}\\Documents\\c1-byod\\msys64\\usr\\bin\\bash.exe"`になる  
   デスクトップフォルダーの場合は`"${env:USERPROFILE}\\Desktop\\c1-byod\\msys64\\usr\\bin\\bash.exe"`になる  
   ちなみに`${env:USERPROFILE}`は自動的に`C:\Users\ユーザー名`に変換されるため、そのままで良い。  

```json
"terminal.integrated.profiles.windows": {
    "c1-byod": { // ここから
        "path": [
            "${env:USERPROFILE}\\env\\c1-byod\\msys64\\usr\\bin\\bash.exe" // ここのpathを書き換える
        ],
        "args": [
            "--login"
        ],
        "env": {
            "MSYSTEM": "MINGW64",
            "CHERE_INVOKING": "1"
        }
    }, // ここまでをコピペする
},
```

VS Codeを再起動して`Ctrl + @`を入力してc1-byodが起動するか、ターミナルの右上にある`+ v`の`v`を押して、c1-byodがあれば設定完了  
<img src="/assets/images/vscode/02.png" alt="vscode-branch" width="50%"/>  
