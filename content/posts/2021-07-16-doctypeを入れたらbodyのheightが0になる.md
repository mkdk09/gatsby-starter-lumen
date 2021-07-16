---
template: post
title: DOCTYPEを入れたらbodyのheightが0になる
slug: HTML
socialImage: /media/cpu.svg
draft: false
date: 2021-07-16T06:15:47.166Z
description: DOCTYPEを入れたらbodyのheightが0になる問題
category: HTML
tags:
  - HTML
  - ""
---
## 問題点

```html
<html>
<head>
    <style>
        body {
            height: 100%;
        }
    </style>
</head>

<body>
    <div style="display: none;">foo</div>
</body>

</html>
```
この書き方をすると高さ100%を指定することができます。

しかし、
```html
<!DOCTYPE html>
<html>
<head>
    <style>
        body {
            height: 100%;
        }
    </style>
</head>

<body>
    <div style="display: none;">foo</div>
</body>

</html>
```
`<!DOCTYPE html>`を入れると`<body>`の高さが0になってしまいました。

## 解決策
```html
<!DOCTYPE html>
<html>
<head>
    <style>
        html {
            height: 100%;
        }
        body {
            height: 100%;
        }
    </style>
</head>

<body>
    <div style="display: none;">foo</div>
</body>

</html>
```
`<html>`に対してもheight: 100%;と指定する必要がありました。

今回の場合、`<div>`の高さを100%にしたい時には、親要素の全てに対してheight: 100%を適用しなければなりません。

そうしないと、子要素を収容する最小限の高さにまで下げらてしまうためです。