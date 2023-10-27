+++
title = 'Add .Content'
date = 2023-10-15T11:00:00-07:00
draft = false
tags = ["theme", "baseof"]
+++

CSSクラスを細かく記述できないブロックには``.content``を追加します。
Markdownで作成するコンテンツ部分には最適です。

```diff
<!DOCTYPE html>
<html lang="{{ or site.Language.LanguageCode site.Language.Lang }}" dir="{{ or site.Language.LanguageDirection `ltr` }}">
<head>
  {{ partial "head.html" . }}
</head>
<body class="container">
  <header>
    {{ partial "header.html" . }}
  </header>
+  <main class="content">
    {{ block "main" . }}{{ end }}
  </main>
  <footer>
    {{ partial "footer.html" . }}
  </footer>
</body>
</html>
```

見出しが大きくなり、かなり見やすくなりました。
