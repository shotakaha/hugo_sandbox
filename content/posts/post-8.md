+++
title = 'Add .Footer'
date = 2023-10-17T09:00:00+09:00
draft = false
tags = ["theme", "baseof"]
+++

フッターを追加した

``/layouts/_default/baseof.html``

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
  <main class="content">
    {{ block "main" . }}{{ end }}
  </main>
+  <footer class="footer">
    {{ partial "footer.html" . }}
  </footer>
</body>
</html>

```

---

``/layouts/partials/footer.html``

```diff
<div class="content has-text-centered">
    <p>&copy; {{ now.Year }} Shota Takahashi</p>
</div>
```

ページ下のフッター領域がいい感じになりました。