---
author: Hugo Authors
title: 數學排版 - 在部落格文章中使用數學符號
date: 2023-04-01
description: KaTeX 設定簡要指南
math: true
draft: true
---

在 Hugo 專案中，可以透過使用 [第三方 JavaScript 函式庫](https://github.com/hugo-sid/hugo-blog-awesome/blob/main/layouts/partials/helpers/katex.html) 來啟用數學符號。

<!--more-->

在本範例中，我們將使用 [KaTeX](https://katex.org/)。

- 若要全域啟用 KaTeX，請在專案的設定檔中將參數 `math` 設為 `true`，如下所示。 
- `hugo.toml`
 ```toml
 [params]
 math = true
 ```
 - `hugo.yaml`
 ```yaml
 params:
 math: true
 ```
- 若要在每頁基礎上啟用 KaTeX，請在 Markdown 內容檔案的 Front Matter 中包含參數 `math: true`，如下所示。 

```
 ---
 math: true
 ---
 ```

**注意：** [支援的 TeX 函數](https://katex.org/docs/supported.html) 線上參考是一個有用的資源。

### 範例

- 區塊級數學公式：

 $$
 \varphi = 1+\frac{1} {1+\frac{1} {1+\frac{1} {1+\cdots} } }
 $$

- 行內數學公式：

 這是一個行內多項式：$5x^2 + 2y -7$。