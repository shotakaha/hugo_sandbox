+++
title = 'Creating new Hugo site'
date = 2023-01-15T09:00:00-07:00
draft = false
tags = ["red", "hugo", "hugo_new"]
+++

Hugoを使ってウェブサイトを作成してみます。
ゼロからサイトを構築するのは大変ですが、Hugoには``hugo new site``コマンドという初期化コマンドがあります。

任意のディレクトリで実行すると、次のようなスケルトンが生成されます。

```console
$ hugo new site サイト名
$ tree サイト名
サイト名
├── archetypes
│   └── default.md
├── assets
├── content
├── data
├── hugo.toml
├── i18n
├── layouts
├── static
└── themes
```

この段階でプレビューしても何も表示されません。

```console
$ hugo server
$ open http://localhost:1313
```

これはコンテンツを表示するためのテンプレートファイルが作成されていないためです。
テンプレートファイルは``/layouts/``の中に作成します。
必要なファイルをひとつずつ作成することもできますが、テーマを作成してみましょう。
