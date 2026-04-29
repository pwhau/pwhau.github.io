---
title: 目錄
date: 2023-05-02
description: 在 Hugo 部落格 awesome 主題中設定目錄
draft: true
---

## 目錄

本主題支援在部落格文章中顯示目錄（ToC）。

## 參數

您可以透過兩個參數管理目錄：

- 全域 `toc` 參數；
- 文章的 `toc` 參數。

文章的 `toc` 參數優先權高於全域 `toc` 參數。

## 在所有文章中啟用目錄

若要在所有文章（全域）中啟用目錄，請在 `hugo.toml` 中將參數 `toc` 設為 `true`。

```toml
[params]
 toc = true
```

若要全域停用目錄，只需忽略 `toc` 參數或將其設為 `false`。

## 在特定文章中啟用目錄

若要在特定文章中啟用目錄，請在文章設定中將參數 `toc` 設定為 `true`。

```yaml
---
title: 如何啟用目錄
date: 2023-05-02
toc: true
---
```

## 在特定文章中停用目錄

要在特定文章中停用目錄，您需要遵循兩個步驟。

注意：文章中的 `.Params.toc` 會覆蓋 `.Site.Params.toc`。完成這些步驟後，文章中的 `toc` 參數將為 `false`。

1. 在 `hugo.toml` 中將參數 `toc` 設為 `true`。 

```toml
 [params]
 toc = true
 ```

2. 在希望停用目錄的文章的 front matter 中加入 `toc = false`。 

```yaml
 ---
 title: 如何啟用目錄
 date: 2023-05-02
 toc: false
 ---
 ```

## 預設開啟目錄

預設情況下，目錄是關閉的。要預設開啟它，請在 `hugo.toml` 中將參數 `tocOpen` 設為 `true`。

```toml
[params]
 tocOpen = true
```

或直接在文章的 front matter 中加入 `tocOpen` 參數。

```yaml
---
title: 如何啟用目錄
date: 2023-05-02
tocOpen: true
---
```