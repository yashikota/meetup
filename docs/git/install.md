# Gitの導入方法、使い方

## Gitの導入&初期設定

**予めGithubアカウントを作成してください。[参考リンク](https://github.com/yashikota/meetup/blob/master/etc/github.md)**

1. [Git公式サイト](https://git-scm.com/download/win)に行き、**Standalone Installerの64-bit Git for Windows Setup**をクリック
2. 全てNextを押してインストールする
3. インストール完了後、Windowsキーを押し、Git bashを起動して

名前と

```bash
git config --global user.name "名前を入力"
```

[こちら](https://github.com/settings/emails)のページのPrimary email addressの下の文章内にある
**数字＋ユーザーネーム@users.noreply.github.com**のメールアドレスを登録する

```bash
git config --global user.email "username@example.com"
```

**この2つの情報は外部にも公開されるので取り扱いには注意しましょう**

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
    <img src="../mini/../../../assets/images/vscode-branch.png" alt="vscode-branch" width="50%"/>  
2. 新しい分岐の作成(一番上)を選択  
    <img src="../mini/../../../assets/images/vscode-branch-dialog.png" alt="vscode-branch-dialog" width="50%"/>  
3. ブランチ名(ここでは```gh-pages```)を入力し、Enterキーを押す  
    <img src="../mini/../../../assets/images/vscode-branch-dialog-name.png" alt="vscode-branch-dialog-name" width="50%"/>  
4. これでブランチの作成は完了  

## upstreamに追従する
