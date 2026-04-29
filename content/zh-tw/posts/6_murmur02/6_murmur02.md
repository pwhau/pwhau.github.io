---
title: "學習筆記01"
date: 2020-11-09T00:01:17+08:00
draft: false

# post thumb
image: ""

# meta description
description: "待業筆記02"

# taxonomies
categories: 
  - "Blog"
 


tags:
  - "Mac"
  - "Python"
  - "Anaconda"
  - "xampp"
  - "PHP"

# post type
type: "post"
---

首先我的作業系統是MAC，而課堂上沒有詳細介紹如何安裝xmapp，但是我找到了一個非常好的教學。

#### Install XAMPP Mac OS X

{{< youtube EK_AUTzV7OI >}}



##### 這裡備註幾點 

###### 1. 教學五分鐘的時候 如果卡關在終端機裡面輸入 cd /..

###### 2. 修改config.inc.php 裡面的

```ruby
$cfg['Servers'][$i]['auth_type'] = 'config';
$cfg['Servers'][$i]['user'] = 'root';
$cfg['Servers'][$i]['password'] = '';
```

```ruby
$cfg['Servers'][$i]['auth_type'] = 'cookie';
$cfg['Servers'][$i]['user'] = '';
$cfg['Servers'][$i]['password'] = '';
```

###### 3. xmapp資料庫裡的使用者 Host name = ％ 有登入疑慮,建議創好Admin之後刪除

###### 4. localhost/phpmyadmin 有時候會無法登入

* 可能原因
* * 瀏覽器快取壞壞 //可以下載MySQL Workbench以訪問資料庫
* * 本地端埠點壞壞 //重開本地埠點連線

------

#### HTTP

![image](https://upload.wikimedia.org/wikipedia/commons/8/82/LAMP_software_bundle.svg)
雖然是LAMP的圖片，但是原理是差不多的 from [wikipedia](https://zh.wikipedia.org/wiki/%E7%B6%B2%E9%A0%81%E4%BC%BA%E6%9C%8D%E5%99%A8#/media/File:LAMP_software_bundle.svg)

##### HTTP請求 透過 Apache HTTP/WEB Server 回覆給請求者


CGI的工作方式，從Web伺服器的角度看，是在特定的位置。定義了可以執行CGI程式。當收到一個匹配URL的請求，相應的程式就會被呼叫，並將客戶端傳送的資料作為輸入。程式的輸出會由Web伺服器收集，並加上合適的檔頭，再傳送回客戶端。


##### 用PHP 撰寫 CGI程式 配合 MySQL


#### 總之xampp就是一個捆包幫大家準備好了所有的東西


-----

#### 資料視覺化

因為要透過網站視覺化資料庫，需要了解資料庫SQL、PHP。

這邊補充一個[PHP鐵人賽文章](https://ithelp.ithome.com.tw/users/20107394/ironman/1332)


我覺得講解得非常好，但是關於PHP又有**套件**需要使用——**composer**。

對於我來說PHP是一個新的語言，加上現在我的開發環境有點太雜了，PHP先暫告一段落。

-----

主線還是要在python身上啦，(是要學習成為時間管理大師!?)

目前我的網頁前端是用Bootstrap5_alpha 後端是XAMPP佐PHP和MariaDB

為什麼我已經在嘗試最新版呢？因為我不想面對jQuery。**謝謝jQuery，再見**

    ！您有一則新訊息：程式債 JS 已經在線等待 (還有React正在排隊中)

套版花了一些時間，主要是不熟悉PHP，但目前狀況運行良好。

以前實習前端還有自學網頁發揮了一些用處。

PHP以後想用python來吃掉，用django或是SQLAlchemy

SQLlite請你排隊好嗎？明明我不太喜歡後端，為什麼走著走著變成全端了？

可能是因為python是膠水把所有東西連在一起了，是三七仔語言嗎？ 總之

之後要把python把整理好的資料下載到資料庫裡面，然後透過網站視覺化呈現出來。

------
#### 閒話 anaconda

anaconda 是巨蚺的意思，我自己簡稱它為森蚺。

python 是蟒蛇的意思，我自己簡稱它為樹蟒。

但是我覺得台灣特有種的蛇——金絲蛇，比很多蛇好看。

大家可以去找看看圖片，重點牠是台灣特有種！

    這篇不是技術文章？怎麼直接變成動物野生頻道？

話說安裝anaconda在MAC上真的是想死。

安裝三次然後又刪掉，最後終於成功安裝起環境。

但是我不喜歡它每次開機都會自動開啟，而且我的環境也被它綁走。

* 我的MAC basic python2 install python3

* * basic python2 透過virtualenv 虛擬環境出一個 myEnv (python3)

* * anaconda3

* * * 透過 conda create --name condaEnv python=3.x 虛擬環境出一個 myEnv (python3.x)

恩，我覺得你們很煩。

**謝謝，virtualenv**

忘了說還有pip 跟 shell 也要了解一下。

希望大家掙脫他們蛇類的綑綁。了解自己在什麼森林。

    哭阿！

------
------
------
------
------
------
    最後是廢文日記
可以聊天的人越來越少，尤其是在剛畢業的人群！我不知道約整個班唱歌，是什麼想法？有事？可能是我老了..不懂現在的青春


最近比較有聊的是從加拿大畢業的同學，談了很多外國差異。大概我們都混過一個人吃飯的時間，所以一起吃飯，一起找地方吃，一起等還沒買好飯的人⋯對於走去學餐，買飯，互等，找地方吃，走回教室。不如我自己快速就地吃完，還可以買杯咖啡坐著慢慢喝再悠閒回教室。只是這中間就沒什麼time zone 剛好的人可以大聊天，可惜。我不覺得這樣算是邊緣人吧？哈哈哈


太久沒聽到有人跟我講英文，以致於我蛤了一聲。對方解釋祝你有一個美好的週末。好的，隨著時間課程要結束了，還是想念國外環境，但是也有點定心了。只是因為台灣已經沒什麼探索樂趣了，只好進修跟工作了。


待過台灣島跟塔斯島之後，島是什麼樣子不重要，重要的是你的生活環境，你身邊的人。但是台灣就是少了什麼，無論如何，就只圖個安身立命。一起努力，加油吧。

    學習/待業日記待續

 


