# 東海駭客社社課 Web Hacking Intro 0x01

## web security簡介

[bug bounty list](https://hackerone.com/bug-bounty-programs)

## OWASP TOP 10 2021
> 開放網路軟體安全計畫，簡稱OWASP （Open Web Application Security Project）

* A01 權限控制失效
* A02 加密機制失效
[hashcat](https://hashcat.net/wiki/doku.php?id=hashcat)
* A03 注入式攻擊
  * SQL injection
  * command injection
  * code injection
* A04 不安全設計
* A05 安全設定缺陷
* A06 危險或過舊的元件
* A07 認證及驗證機制失效
* A08 軟體及資料完整性失效
* A09 資安記錄及監控失效
* A10 伺服端請求偽造

## linux基礎指令認識+使用

- 一般指令
```gherkin=
#管理員權限
sudo
#顯示目前路徑
pwd
#list
ls
#進入資料夾
cd
#建立檔案、更改檔案時間戳
touch
#編輯檔案權限
chmod
#找檔案
find
#建立資料夾
mkdir
#查看檔案類型
file
#移動並重新命名
mv
#檢視檔案中的資料
cat
#linux的記事本
vim
#下載資料
wget
#刪除檔案
rm
``` 
    


- 跟web有關的指令
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

# verb
curl -X {verb} http://HOSTNAME/

# 重導向
curl -L http://HOSTNAME/

# cookie
curl http://HOSTNAME/ -b 'yes=123; you=cool'
```

[Lab網址](https://github.com/praetorian-inc/Hob0Rules/archive/refs/heads/master.zip)

> Lab說明:複製上面網址用指令下載、解壓縮unzip，之後開啟或檢視rockyou.txt

[Linux Curl Command 指令與基本操作入門教學](https://blog.techbridge.cc/2019/02/01/linux-curl-command-tutorial/)


## OSINT(Open Source INTelligence, 公開來源情報)

- [osint framework](https://osintframework.com/)

* 駭客愛用的瀏覽器: 
  - [shodan](https://www.shodan.io/)
- google hacking
  - 基本查詢
    - inurl
    - intext
    - intitle
    - index of
    - filetype
    - site
 * 開源情報工具
   - [phoneinfoga](https://github.com/sundowndev/phoneinfoga)
   - [sherlock](https://github.com/sherlock-project/sherlock)
   - [Osintgram](https://github.com/Datalux/Osintgram)
   - [spyse](https://spyse.com/)
   - [wayback machine](https://web.archive.org/)
   
**Lab1網址:**
https://docs.google.com/document/d/1LTTguhtfyCjPCUEl_qub81V7rZ7haG8KE0Da-EqKng4/edit?usp=sharing
> Lab1說明:利用一些工具試著看到我刪除的檔案吧~(解答格式:Flag{(字串)})

**Lab2:試著找到我的IG及臉書~~元宇宙~~吧~ 我各藏了一個Flag在那裡，去找吧~**
> Lab2說明:解答格式跟上面一樣，IG的Flag比較簡單
> 找到後把你找到的整串flag拿去做md5 hash，然後跟下面做比對

facebook flag md5 hash:
```gherkin=
f29819b3ffaaf0d92cf05d0877f86d4c
```

instagram flag md5 hash:
```gherkin=
1d7279db23740315861857b6a11d0f26
```
