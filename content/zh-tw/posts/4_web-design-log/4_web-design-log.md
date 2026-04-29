---
title: "網站設計紀錄"
date: 2020-09-29T23:23:17+08:00
draft: false

# post thumb
image: "images/post/4-wdlog-1.jpg"

# meta description
description: "感覺Automator可以用來做很多事情？"

# taxonomies
categories: 
  - "Hugo"
 


tags:
  - "Blog"
  - "Hugo"
  - "Test"
  - "Markdown"
  - "VS code"
  - "Mac"
  - "Automator"


# post type
type: "post"
---

印象中可以把重複的程序寫成exe讓電腦執行

但是Mac好像不能產生exe?內建的python應該可以吧？

		意外發現Mac的Automator是按鍵精靈?Autohotkey?巨集?
		然後AppleScript又是什麼？它可以寫巨集。那跟Swift一樣嗎？
		照著圖片設定就可以一鍵搬運發文前的所有內容
		再用GitHub Desktop就可以上傳了～


* 想用函數自動抓發文時間


---


* 拿掉Social link icon，但是發現Logo歪掉，但是改好了。

(透過mr-auto)



* 響應式視窗，設計了兩個。

一個是視窗超過(desktop)992px，顯示About me

一個是視窗小於(mobile)575px，顯示Tag

(讓觀眾比較好選擇想看的文章標籤?)


* Added a gallery layout in navigation bar.

(我是用Contact去試一個新的layout)
```
1.在config.toml裡面
	新增
		[[menu.main]]
	 	name = "Gallery"
  		URL = "gallery"
  		weight = 4

2.在layouts資料夾裡面
	新增gallery資料夾
	新增list.html
		{{ define "main" }}  (html最開頭)
			(程式碼)
		{{ end }}  (html最結尾)

後來發現還要
3.在content資料夾裡面
	新增gallery資料夾
	新增 _index.md
		自訂裡面的md文件
(回到layouts/gallery/list.html裡面，就可以取_index.md相關的值)

```

* 想要在navigation bar有下拉式選單

還要研究一下navigation bar 的button

或是hover之類的語法

* 連結repo的網頁


