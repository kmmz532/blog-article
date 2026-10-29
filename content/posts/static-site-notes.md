---
title: "静的サイトの組み立てメモ"
date: 2026-10-12T20:30:00+09:00
categories: ["devlog"]
tags: ["hugo", "github-pages"]
summary: "Hugo で静的サイトを組み立てたときの手順を、架空の例でまとめた記事です。"
---

> **テスト記事**: 本番公開前に削除または書き換えます。

Hugo のテンプレートは `layouts/_default/` に置くと、ほぼすべてのページで使われます。

```go-html-template
{{ define "main" }}
  {{ range .Pages }}
    {{ partial "post-card.html" . }}
  {{ end }}
{{ end }}
```

コードブロックは Chroma でハイライトされます。
