---
title: "學習筆記02"
date: 2020-11-10T23:51:17+08:00
draft: false

# post thumb
image: ""

# meta description
description: "其實是卡關日記"

# taxonomies
categories: 
  - "Blog"
 


tags:
  - "Mac"
  - "Python"
  - "Anaconda"
  - "xampp"
  - "PHP"
  - "MySQL"
  - "sqlite3"
  - "VScode"


# post type
type: "post"
---

今天是想把蒐集到的資料，映射到資料表。

但是想當然事情不會發展得這麼順利。

import pyMySQL 之後

不知道為什麼執行後

無法讀取xampp的MySQL

```ruby
顯示 2013, 'Lost connection to MySQL server during query'
```

感覺的問題在於timeout

但是我設置了2000卻也沒辦法成功，是因為原生xampp的mySQL太肥大嗎？

附註[參考來源](https://dev.mysql.com/doc/refman/5.7/en/error-lost-connection.html)


```SQL
show variables like '%timeout%'; --顯示有關timeout的變數
SET GLOBAL net_read_timeout=10; --設定變數時間
SET GLOBAL connect_timeout=10; --設定變數時間
--如果還是錯誤是情況需要更改 max_allowed_packet
```
也可以用python這樣改寫(不用更改MySQL變數)

```python
import mysql.connector
cnx = mysql.connector.connect(user='user_name',
                          password='password',
                          host='localhost',
                          database='database_name',
                          connect_timeout=500)
cnx.close()
```
> #### 但是我都失敗謝謝

---------
---------
---------

最後只好參考書籍做法了

但是書籍教學的是原生套件中的**輕量型資料庫sqlite**

>  可以不要這樣嗎？

---------
---------
---------


對了，另外一個參考資料

[Using Python environments in VS Code](https://code.visualstudio.com/docs/python/environments)

或是按下command + shift + p

可以更改要執行的python來源

-------

適用於在有很多隻python的森林中的我

原生一隻2.7，另外抓一隻python3

原生虛擬出一個python3的myEnv

原生anaconda3

原生anaconda3虛擬出condaEnv

> 我想都賣去華西街，謝謝


     回不去單純只需要Excel資料表改改函數和公式的日子了嗎？


-------

今天的新聞是Mac要改用ARM架構。

有沒有連查維基百科都還不知道的東西？

**ARM架構**簡單來講可以是x32 x64的那種東西嗎？

啃不下，太硬體了．．．

-------

然後是UX的方面，負責商業模式，業務，行銷部門果然才是公司裡的風向啊。

要當個喊水會結凍的人就去發展這三個方向吧！

我的網站開發目前有點卡關

存不到資料庫裡的資料是要怎樣？

明天開始要暴力解看看了，虛擬環境靠你了。
