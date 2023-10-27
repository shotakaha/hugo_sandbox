+++
title = 'Add Bulma CSS'
date = 2023-02-15T10:00:00-07:00
draft = false
tags = ['red','green']
+++

ウェブページを表示できるようになったのですが、見た目がいまいちです。
デフォルトでは``main.css``が適用されています。
コメントアウトしましょう。

```diff
+{{/*
{{- with resources.Get "css/main.css" }}
  {{- if eq hugo.Environment "development" }}
    <link rel="stylesheet" href="{{ .RelPermalink }}">
  {{- else }}
    {{- with . | minify | fingerprint }}
      <link rel="stylesheet" href="{{ .RelPermalink }}" integrity="{{ .Data.Integrity }}" crossorigin="anonymous">
    {{- end }}
  {{- end }}
{{- end }}
+*/}}
```

そしてBulmaCSSを追加します。

```diff
{{/*
{{- with resources.Get "css/main.css" }}
  {{- if eq hugo.Environment "development" }}
    <link rel="stylesheet" href="{{ .RelPermalink }}">
  {{- else }}
    {{- with . | minify | fingerprint }}
      <link rel="stylesheet" href="{{ .RelPermalink }}" integrity="{{ .Data.Integrity }}" crossorigin="anonymous">
    {{- end }}
  {{- end }}
{{- end }}
*/}}
+<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bulma@0.9.4/css/bulma.min.css">
```

・・・ますます表示が崩れた気がしますが、これから頑張って直します。