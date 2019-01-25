# SEO專案規畫與實作 day 2

[Search Metrix](https://www.searchmetrics.com/)
[示範帳戶](https://support.google.com/analytics/answer/6367342?hl=zh-Hant)

## 改善網頁下載速度

[GTmetrix](https://gtmetrix.com/)
[Google PageSpeed Insight](https://developers.google.com/speed/pagespeed/insights/?hl=zh-TW)
[HTTP/2 Test](https://tools.keycdn.com/http2-test)

[Leverage browser caching](https://gtmetrix.com/leverage-browser-caching.html)

可在此設定 .htaccess，不能超過一年

建議會動到程式碼的可以最後再做

先載入 CSS, then JS

CSS sprites

## 網頁安全

YMYL: 購物、醫療，與生命財產有關或嚴肅議題

EX: [魏则西事件](https://zh.wikipedia.org/wiki/%E9%AD%8F%E5%88%99%E8%A5%BF%E4%BA%8B%E4%BB%B6)

## 重複性內容(duplicated content)

url 大小寫不同，但內容相似

1. 站外

盜文
內容授權:

* 授權前(7d)先讓自己內容給 searh engine 抓
* 被授權者(ex: 博客來、誠品)求異

2. 站內

友善列印
大型公版網站，較少內容
title meta 相似

## 標準網址: 網址規劃不當所造成(Canonical Issue)

選定網址版本，作轉址
大小寫

EX: https://www.104.com.tw, https://104.com.tw

sample: https://www.facebook.com, https://twmotel.com
smaple: benq display

處理方式
* 阻擋
  * robots.txt: google 不建議
  * robots meta tag: no index(不要建索引)
  * google search console: 網址參數
* 宣告
  * 偏好網域
  * alernative(optional), canonical
  * A canonical A, google 可接受

https:

1. 另開網站管理工具
1. 重新提交 sitemap
1. 結構化資料重新註釋
1. 舊站不拔要 301 轉址
1. 內外連結要改 https

m.xxx

1. 另開網站管理工具
1. 重新提交 sitemap
1. 結構化資料重新註釋
1. 交互註釋
1. robots.txt 沒有檔 m.xxx

## 社交分享按鈕

social signal
smo: 提供社交傳播機制，讓內容更容易被分享
facebook open graph markup

## 站內搜尋

[principle of mobile site design](https://www.thinkwithgoogle.com/marketing-resources/experience-design/principles-mobile-site-design-delight-users-drive-conversions/)

![](https://i.imgur.com/MXzvAE2.png)

[sidelink searchbox](https://developers.google.com/search/docs/data-types/sitelinks-searchbox): 首頁埋結構化資料(JSON-LD)

## 網站提交

網站剛成立時可以使用提交

search engine 經常造訪的網頁

site:tutor.104.com.tw
![](https://i.imgur.com/jx55hgJ.png)

### sitemap

HTML 給人看, XML 給機器看
max: 50k, 超過的話要切分檔案
file size: 10MB(解壓縮以後)

[簡化多個 Sitemap 的管理作業](https://support.google.com/webmasters/answer/75712?hl=zh-Hant)

[sitemap](https://www.sitemaps.org/zh_TW/protocol.html)

EX: [nexcom](http://www.nexcom.com/robots.txt), [settour](http://www.settour.com.tw/robots.txt)

#### 產生 sitemap

* 少量時可手寫
* 少於 500 頁，可用線上工具 xml: [sitemap generator](https://www.xml-sitemaps.com/), screaming frog
* 大於 500 頁，少於 5k: 付費版 screaming frog
* 大於 5k: 工程開發(serverside xml sitemap)
* CMS 外掛

sitemap 要放在最高階層資料夾

#### 通知 search engine

網址上下線時

* google search console: 檢索 > sitemap，務必先測試再提交
* robots.txt: 一定要放在跟目錄，比 GSC 好用
* ping(CMS 會利用此方法): `xml sitemap ping`, [HOW TO SUBMIT AN XML SITEMAP TO GOOGLE AND BING](http://www.dummies.com/web-design-development/search-engine-optimization/how-to-submit-an-xml-sitemap-to-google-and-bing/)

## Content

![](https://i.imgur.com/xHZaFR3.png)

文法、拼字、字體大小、排版

重點在 65 字以內寫完

品牌名建議放後面: `site:www.s3.com.tw`(已改善)

yes2100.com: 猛塞關鍵字

使用者評論 UGC

規劃站外連結，連結到權威網站: ex: wiki

## 關鍵字

文案比 title tag 還重要

1. 挖掘(海選): 相關、符合主題

    競爭對手:
    * moz bar 搜尋 關鍵字 + site
    * scream frog: internal(HTML) > export

    關鍵詞建議:
    * [Ubersuggest](https://ubersuggest.io/): csv
    * [Keyword Tool](https://keywordtool.io/): excel
    * [Twinword](https://www.twinword.com/)
    * [google keyword planner](https://adwords.google.com/home/tools/keyword-planner/)
    * bing web master
    * [google trend](https://trends.google.com.tw/trends/): 長期、熱搜

2. 產出(拓展): 品牌、功效、用途、種類
3. 挑選(篩選): 相關度、熱門度、競爭度 seo 5a

    * 前期: 導覽式、交易式
    * 後期: 資訊式

    * 競爭度: `intitle:keyword`，搜尋結果必含 `keyword`

4. 分詞、分組(規劃): 單元、內容

keyword effectiveness index: 關鍵字投報比

全網: `keyword`
站內: `keyword site:xxxx`
產生頁面: 找不到時

5. 布局(匹配): landing page

## 網站排名優化

.edu, .gov 歷史悠久

nofollow: comment spam

dofollow blog list

連結分析
E.A.T. Expert, Authority, Trustworthy

Deep Link Ratio(首頁以外): 不要低於 30%
Link Diversity: 要經營不同 domain 的反向連結

```txt
hand tool SK hand tool
link:www.skhandtool.com
www.skhandtool.com
inanchor:hand tool
inurl:hand tool
inurl:canada wood machine dealer
```

## 結果顯式優化