---
title: Markdown 文法指南
date: 2023-02-11
author: Hugo Authors
description: 展示基本 Markdown 語法和 HTML 元素格式化的範例文章。
isStarred: true
---

本文提供了 Hugo 內容檔案中可以使用的 Markdown 語法範例，同時展示了 Hugo 主題中是否對基本 HTML 元素進行了 CSS 裝飾。
<!--more-->

## 標題

以下 HTML `<h1>`—`<h6>` 元素表示六個層級的標題。 `<h1>` 是最高等級的標題，而 `<h6>` 是最低等級的標題。

# H1

## H2

### H3

#### H4

##### H5

###### H6

## 段落

Xerum, quo qui aut unt expliquam qui dolut labo. Aque venitatiusda cum, voluptionse latur sitiae dolessi aut parist aut dollo enim qui voluptate ma dolestendit peritin reges autal incs qui voluptate ma dolestendit peritin replis sl ar​​stal s硬骨 inc yque sthr. tectur, offic to cor sequas etum rerum idem sintibus eiur? Quianimin porecus evelectur, cum que nis nust voloribus ratem aut omnimi, sitatur? Quiatem. Nam, omnis sum am face conecerem erum fuga. Ri 迪

Itatur? Quiatae cullecum rem ent aut odis in re eossequodi nonsequ idebis ne sapicia is sinveli squiatum, core et que aut hariosam ex eat.

## 圖片

您可以使用以下語法來包含圖片。圖片的路徑應相對於 `index.md` 檔案。

```markdown
![Landscape](1.jpg)
```

![Landscape](1.jpg)

您也可以包含來自外部來源的圖片。

```markdown
![Image](https://source.unsplash.com/random/600x400/?tech)
```

![Image](https://source.unsplash.com/random/600x400/?tech)

## 引用

引用元素表示從其他來源引用的內容，可以選擇包含引用來源，引用來源必須位於 `footer` 或 `cite` 元素中，也可以選擇包含註解和縮寫等內嵌變更。

### 無來源的引用

> 您可以在引用中使用 Markdown 語法，例如 **bold**, _italics_, [links](https://gohugo.io/), `code`。

### 帶來源的引用

> Don't communicate by sharing memory, share memory by communicating.<br>
> — <cite>Rob Pike[^1]</cite>

[^1]: 上述引文摘自 Rob Pike 在 2015 年 11 月 18 日 Gopherfest 上的[演講](https://www.youtube.com/watch?v=PAAkCSZUG1c)。

## 表格

表格不是 Markdown 核心規範的一部分，但 Hugo 原生支持它們。 

Name | Age
--------|------
 Bob | 27
 愛麗絲 | 23

### 表格中的 Markdown

| Italics | Bold | Code |
| -------- | -------- | ------ |
| *italics* | **bold** | `code` |

## 程式碼區塊

### 使用反引號的程式碼區塊

```html
<!doctype html>
<html lang="en">
<head>
 <meta charset="utf-8">
 <title>Example HTML5 Document</title>
</head>
<body>
 <p>Test</p>
</body>
</html>
```

### 縮排四個空格的程式碼區塊

 <!doctype html>
 <html lang="en">
 <head>
 <meta charset="utf-8">
 <title>Example HTML5 Document</title>
 </head>
 <body>
 <p>Test</p>
 </body>
 </html>

### 使用 Hugo 內建高亮短代碼的程式碼區塊

{{< highlight html >}}
<!doctype html>
<html lang="en">
<head>
 <meta charset="utf-8">
 <title>Example HTML5 Document</title>
</head>
<body>
 <p>Test</p>
</body>
</html>
{{< /highlight >}}

### 內聯程式碼

使用反引號在句子中引用 `variable`。

## 清單類型

### 有序列表

1. First item
2. Second item with some `code` in it
3. Third item

### 無序列表

* List item
* Another item with some `code` in it
* And another item

### 嵌套列表

* Fruit
 * Apple
 * Orange
 * Banana
* Dairy
 * Milk
 * Cheese

## 其他元素 — abbr, sub, sup, kbd, mark

<abbr title="Graphics Interchange Format">GIF</abbr> 是一種點陣圖影像格式。

H<sub>2</sub>O

X<sup>n</sup> + Y<sup>n</sup> = Z<sup>n</sup>

按下 <kbd>CTRL</kbd>+<kbd>ALT</kbd>+<kbd>Delete</kbd> 結束會話。

大多數 <mark>蠑螈</mark> 是夜行性動物，捕食昆蟲、蠕蟲和其他小生物。