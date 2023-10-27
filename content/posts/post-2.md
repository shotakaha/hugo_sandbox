+++
title = 'Creating new Hugo theme'
date = 2023-02-15T10:00:00-07:00
draft = false
tags = ['red','green']
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

Anim eiusmod irure incididunt sint cupidatat. Incididunt irure irure irure nisi ipsum do ut quis fugiat consectetur proident cupidatat incididunt cillum. Dolore voluptate occaecat qui mollit laborum ullamco et. Ipsum laboris officia anim laboris culpa eiusmod ex magna ex cupidatat anim ipsum aute. Mollit aliquip occaecat qui sunt velit ut cupidatat reprehenderit enim sunt laborum. Velit veniam in officia nulla adipisicing ut duis officia.

Exercitation voluptate irure in irure tempor mollit Lorem nostrud ad officia. Velit id fugiat occaecat do tempor. Sit officia Lorem aliquip eu deserunt consectetur. Aute proident deserunt in nulla aliquip dolore ipsum Lorem ut cupidatat consectetur sit sint laborum. Esse cupidatat sit sint sunt tempor exercitation deserunt. Labore dolor duis laborum est do nisi ut veniam dolor et nostrud nostrud.

```console
$ hugo new theme sandbox_theme
```