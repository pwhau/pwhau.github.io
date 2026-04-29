---
title: Emoji 支持
date: 2023-02-01
author: Hugo Authors
description: 在 Hugo 中使用 Emoji 的指南
draft: true
tags:
    - emoji
---

在 Hugo 專案中有多種方式可以啟用 Emoji。

<!--more-->

可以在範本中直接呼叫 [`emojify`](https://gohugo.io/functions/emojify/) 函數，或使用 [Inline Shortcodes](https://gohugo.io/templates/shortcode-templates/#inline-shortcodes)。

若要全域啟用 Emoji，請在網站的 `hugo.toml` 中將 `enableEmoji` 設為 `true`。您可以直接在內容檔案中輸入 Emoji 的簡寫程式碼，例如：

`:see_no_evil:` :see_no_evil: `:hear_no_evil:` :hear_no_evil: `:speak_no_evil:` :speak_no_evil:

我 :heart: Hugo! 😁

[Emoji 速查表](http://www.emoji-cheat-sheet.com/) 是一個非常有用的 Emoji 簡寫程式碼參考。

---

**注意：** 上述步驟啟用了 Hugo 中的 Unicode 標準 Emoji 字元和序列，但這些字元的渲染效果取決於瀏覽器和平台。若要為 Emoji 設定樣式，您可以使用第三方 Emoji 字體或字體堆疊，例如：

{{< highlight css >}}
.emoji {
font-family: Apple Color Emoji, Segoe UI Emoji, NotoColorEmoji, Segoe UI Symbol, Android Emoji, EmojiSymbols;
}
{{< /highlight >}}

{{< css.inline >}}

<style>
.emojify {
  font-family: Apple Color Emoji, Segoe UI Emoji, NotoColorEmoji, Segoe UI Symbol, Android Emoji, EmojiSymbols;
  font-size: 2rem;
  vertical-align: middle;
}
@media screen and (max-width:650px) {
  .nowrap {
    display: block;
    margin: 25px 0;
  }
}
</style>

{{< /css.inline >}}
