# Gitの導入方法

**予めGithubアカウントを作成してください。[参考リンク](https://meetup.yashikota.com/github/setup/)**

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
