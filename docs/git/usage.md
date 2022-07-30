# Gitの使い方

## ローカルのファイルをGithubにアップロードする方法

Gitを使用するための準備

```bash
git init
```

現在あるファイルを**全て**(. = 全てという意味)ステージに追加

```bash
git add .
```

コミットメッセージを記入

```bash
git commit -m "first commit"
```

mainブランチに切り替え

```bash
git branch -M main
```

アップロード先(ここではGithub)の存在を教える

```bash
git remote add origin git@github.com:yashikota/test.git
```

Githubにアップロード

```bash
git push -u origin main
```

## ブランチの作成

1. 左下を押してブランチ作成画面を開く  
    <img src="/assets/images/vscode-branch.png" alt="vscode-branch" width="50%"/>  
2. 新しい分岐の作成(一番上)を選択  
    <img src="/assets/images/vscode-branch-dialog.png" alt="vscode-branch-dialog" width="50%"/>  
3. ブランチ名(ここでは```gh-pages```)を入力し、Enterキーを押す  
    <img src="/assets/images/vscode-branch-dialog-name.png" alt="vscode-branch-dialog-name" width="50%"/>  
4. これでブランチの作成は完了  

## upstreamに追従する
