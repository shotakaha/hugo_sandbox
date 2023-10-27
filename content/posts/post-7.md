+++
title = 'Add .Title / .Subtitle'
date = 2023-10-15T12:00:00-07:00
draft = false
tags = ["theme", "baseof"]
+++

タイトル／サブタイトル用のクラスを追加します。

``/layouts/_default/single.html``

```diff
{{ define "main" }}
+  <h1 class="title">{{ .Title }}</h1>

  {{ $dateMachine := .Date | time.Format "2006-01-02T15:04:05-07:00" }}
  {{ $dateHuman := .Date | time.Format ":date_long" }}
  <time datetime="{{ $dateMachine }}">{{ $dateHuman }}</time>

  {{ .Content }}
  {{ partial "terms.html" (dict "taxonomy" "tags" "page" .) }}
{{ end }}
```

---

``/layouts/_default/list.html``

```diff
{{ define "main" }}
+  <h1 class="title">{{ .Title }}</h1>
  {{ .Content }}
  {{ range .Pages }}
    <h2><a href="{{ .RelPermalink }}">{{ .LinkTitle }}</a></h2>
    {{ .Summary }}
  {{ end }}
{{ end }}
```

---

``/layouts/partials/header.html``

```diff
+ <h1 class="title">{{ site.Title }}</h1>
{{ partial "menu.html" (dict "menuID" "main" "page" .) }}
```

タイトルの周りにマージンができて、これまた見やすくなりました。