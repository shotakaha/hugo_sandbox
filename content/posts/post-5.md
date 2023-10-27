+++
title = 'Add .Container'
date = 2023-10-15T10:00:00-07:00
draft = false
tags = ["theme", "baseof"]
+++

BulmaCSSの基本は縦レイアウトです。
とりあえずテンプレートの主要部分に``.container``を追加してみます。

```diff
<!DOCTYPE html>
<html lang="{{ or site.Language.LanguageCode site.Language.Lang }}" dir="{{ or site.Language.LanguageDirection `ltr` }}">
<head>
  {{ partial "head.html" . }}
</head>
+<body class="container">
  <header>
    {{ partial "header.html" . }}
  </header>
  <main>
    {{ block "main" . }}{{ end }}
  </main>
  <footer>
    {{ partial "footer.html" . }}
  </footer>
</body>
</html>
```

画面の両端に余白が生まれ、ちょっとだけ見やすくなりました。