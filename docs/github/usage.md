# Githubの使い方

## リポジトリの作成

1. [github.new](https://github.new)に移動するかGithub.comで右上の**＋**マークを押すとNew repositoryとあるのでそれをクリック
2. **Repository name**に適当な名前を  
**PublicかPrivate**でリポジトリの公開状態を選択し、  
緑色の**Create repository**を押すとリポジトリが作成される。

## cloneのやり方

1. リポジトリに移動し、右上の緑の**Code**をクリックして下のような画面にする  
   <img src="/assets/images/github-clone.png" alt="github-clone" width="50%" />
2. HTTPS SSH Github CLIのところで**SSH**を選択してその下のURLをコピーする(右のボタンを押すとコピーできる)  
3. PowerShellを開いて適当なディレクトリに移動した後、下のコマンドを打つ

```bash
git clone コピーしたURL
```

## issueの立て方

1. リポジトリに移動し、**Issues**と書かれたタブをクリックする  
2. 緑の**New issue**ボタンを押す  
3. **Title**にissueのタイトルを(必須)、**Leave a comment**に詳細な内容を(必須ではない)を記入する
4. 緑の**Submit new issue**をクリックすればissueが立てられる

## pull requestのやり方

1. リポジトリに移動し、**Pull requests**と書かれたタブをクリックする  
2. 緑の**New pull request**ボタンを押す  
3. ブランチを選択する(写真はdevブランチからgh-pagesブランチにプルリクを投げている様子)  
    <img src="/assets/images/github-pr.png" alt="github-pr" width="50%"/>  
4. 緑の**Merge pull request**ボタンを押す
