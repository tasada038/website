---
title: "starter-hugo-academic + Github Pagesでwebsiteを作るチップス"
date: 2023-11-04
draft: false
tags:
- Hugo
- GitHub Pages
- Open-Source
summary: ""

slides: ""
---

- [How to create the original website?](#hugo)
- [References](#references)

<br>

# How to create the original website?

ベースとして、[How to Create an Academic/Wowchemy GitHub Page With Hugo?](https://mickaellalande.github.io/post/tutorial/how-to-create-an-academic-github-page-with-hugo/)の手順で作成していきます。




- starter-hugo-academicをFork

[starter-hugo-academic](https://github.com/wowchemy/starter-hugo-academic)をForkします。

Forkしたリポジトリは`website`として名前を変更しており、これをローカルへクローンします。

- user_name.github.ioのリポジトリを作成

GitHub Pagesのリポジトリを作成し、`website`ディレクトリ下でsubmoduleとして追加します。

```sh: terminal
git submodule add -f -b master https://github.com/tasada038/tasada038.github.io.git public
```

- websiteの中身を修正

2023/11/04、Ubuntu 22.04にて動作確認したところ、hugoコマンドにてERRORが生じたため、以下ReferencesのGithubを参考に`theme.toml`、`netlify.toml`、`go.*`を修正し、必要不必要なフォルダを精査して作成します。

使用するライブラリ指定などがしっかりとできていれば`hugo`コマンドが通るので`website`ディレクトリ下で`hugo`コマンドを実行しましょう。

すると、public下に必要なパッケージが自動生成されるはずです。そしたら`hugo server`コマンドでwebsiteの出来を確認します。



# References

[hugo-academicでポートフォリオを作成する](https://qiita.com/junffy/items/3188671d02a771920fd7)

[Hugo Academic を使ってウェブサイトをアップデートしました](https://r9y9.github.io/blog/2022/01/18/hugo-academic/)

[Github: r9y9/website](https://github.com/r9y9/website)

[Hugo + GitHub Pages + GitHub Actions で独自ドメインのウェブサイトを構築する](https://zenn.dev/nikaera/articles/hugo-github-actions-for-github-pages)

[Hugo+Github Pagesでプロフィールページを作ってみた](https://zenn.dev/okaponta/articles/c302f58507febc)

[hugoを使って爆速でブログを作成する](https://zenn.dev/harachan/articles/a043e9a756cae4)