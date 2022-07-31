東海駭客社社課 web入門 0x02
===
# 網頁概述

## 前端基礎

### 前端是什麼?
簡單來說，我們瀏覽的所有網站，不分大小，使用者(Client)端肉眼可見的全都稱為"前端"。
前端設計需要兼顧美感與實用，隨著近年來行動裝置的竄起，如何相容於不同裝置也成為一個重要課題。
優秀的前端工程師寫的程式通常會相容於各大瀏覽器以及行動裝置，並同時兼顧美感和實用。

### 前端語言有哪些??
* javascript(讓網頁動起來)
[popcat](https://popcat.click/)
[外掛程式](https://gist.github.com/DaWe35/0febd8b058e4476967d12675a622c989)

* html(網頁程式碼的骨架)

* css(美化整個架構、調整間距......等)

pico{}

### 前端怎麼送出表單??
* GET
```gherkin=
<form action="view.php" method="GET">
    <input type="text" name="id">
    <input type="submit" value="送出">
</form>
```
* POST
```gherkin=
<form action="login.php" method="POST">
    <input type="text" name="username">
    <input type="password" name="password">
    <input type=submit value="Login">
</form>
```
> Read more about mermaid here: [前端工程(Front-End)簡介](https://blog.davidh83110.com/%E6%8A%80%E8%A1%93%E7%B0%A1%E4%BB%8B/%E5%89%8D%E7%AB%AF%E5%B7%A5%E7%A8%8B/2016/12/05/web-intro-1.html)

後端基礎
---
### 什麼是後端?

後端主要著重在功能與資料儲存。比方說註冊會員、登入，在電商網站下單購物也是後端的工作，那什麼又是資料儲存呢？前面所講的這些功能做完之後會產生很多資料，就要把它儲存下來，就像註冊完會員之後會產生帳號密碼，下單購物之後就會有訂單資料，這些都是必須儲存起來的資料。

### 後端語言有哪些??
* python:資料探勘的、分析數據, ex:Instagram
* php:目前使用者最多的後端語言，有安全性問題, ex:Facebook
* Ruby:開發快速, ex:twitter
* Node.js: 速度快，前後端可以一起使用, ex:Yahoo
* Go: 效能好，速度快, ex:Google、youtube

### 後端怎麼處理你的請求??
* 根目錄預設的路徑
  * index.php
    * 將請求丟給web server，web server解析完丟給php
    * php透過特殊變數存取請求
  * index.html


> Read more about  here:[不可不知：常用網頁程式語言比較](https://gremlinworks.com.tw/webdev/dev-languages)

## 資料庫
* mySQL
* MSSQL
* microsoft access
* PostgreSQL

## 編碼方式
[編碼工具](https://dencode.com/)
* hash
* Unicode、UTF-8
* URL encode
* 進位制編碼
* ASCII

### Lab 0x03
```gherkin=
🐽👃🐸🐾👲👮🐪👙👖👪👜👚👬👩🐨👫👰👖🐨👪👖🐽👌👅👅👅👅🐘🐘🐘👴
```

## cookie
## session

## 網路概述
## HTTP/HTTPS概述
## General查看
  * Chrome>F12>network>ctrl+R>抓左邊最上面的看
  * request URL
  * Request Method
  * status code
### HTTP request
  * HTTP request header
### HTTP respond
  * HTTP respond header
### 補充HTTP版本

* HTTP/0.9
客戶端傳送的訊息有限
* HTTP/1.0
仍被廣泛採用；每次請求都要建立一次連線，完成後斷開
* HTTP/1.1
持久連接，以管道的方式能同時傳送多個請求，提高傳輸速度
* HTTP/2
全球約 4 成的網站支援此版本

跟web有關的指令
---

```gherkin=
# 建立 TCP 連線
nc IP PORT

# 監聽 TCP port
nc -l PORT

# 下載東西
wget https://hello.world.com/image.jpg
wget https://hello.world.com/image.jpg -O cool.jpg

# HTTP request
# GET
curl http://example.com
curl http://example.com -v   # 顯示 request 跟 respose 更詳細的資訊
curl 'http://HOSTNAME/?id=123&name=123'

# HEAD
curl -X HEAD http://HOSTNAME/
curl -I http://HOSTNAME/

# POST
curl http://HOSTNAME/login -d 'username=123&password=123'
curl -X POST http://HOSTNAME/ -d 'username=123&password=123'
curl http://HOSTNAME/ -F file=@/path/to/file # 上傳

# OPTIONS
curl -X OPTIONS http://HOSTNAME/
# 用任何 verb
curl -X 隨便啥都可以 http://HOSTNAME/
# 跟著重導向
curl -L http://HOSTNAME/
# 帶上 cookie
curl http://HOSTNAME/ -b 'yes=123; you=cool'
```
> Read more about mermaid here:[從瀏覽器認識 HTTP 協定](https://ithelp.ithome.com.tw/articles/10195016)
