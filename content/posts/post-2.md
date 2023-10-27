+++
title = 'Creating new Hugo theme'
date = 2023-02-15T10:00:00-07:00
draft = false
tags = ["theme", "hugo_new"]
+++

Hugoにはテーマ機能があります。
無料で公開されているテーマも多数あるので、そこから探してみるのもよいでしょう。

今回はオリジナルテーマを作ってみたいと思います。
テーマ作成時に初期化コマンドもあります。

```console
$ cd サイト名
$ hugo new theme テーマ名
$ tree themes/テーマ名
themes/テーマ名
├── LICENSE
├── README.md
├── archetypes
│   └── default.md
├── assets
│   ├── css
│   │   └── main.css
│   └── js
│       └── main.js
├── data
├── hugo.toml
├── i18n
├── layouts
│   ├── _default
│   │   ├── baseof.html
│   │   ├── home.html
│   │   ├── list.html
│   │   └── single.html
│   └── partials
│       ├── footer.html
│       ├── head
│       │   ├── css.html
│       │   └── js.html
│       ├── head.html
│       ├── header.html
│       ├── menu.html
│       └── terms.html
├── static
│   └── favicon.ico
└── theme.toml
```

## テーマを設定する

テーマのスケルトンが作成できました。
サイト設定に追加します。

```diff
baseURL = 'https://example.org/'
languageCode = 'en-us'
+title = 'サイト名'
+theme = "テーマ名"
```

これでとりあえずウェブページを表示できるようになりました。