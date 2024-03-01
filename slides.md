---
theme: seriph
background: https://source.unsplash.com/collection/94734566/1920x1080
class: text-center
highlighter: shiki
lineNumbers: true
drawings:
  presenterOnly: true
  syncAll: false
transition: slide-left
title: Regex
titleTemplate: '%s - Regex'
colorSchema: dark
defaults:
  layout: default
layout: center
---

# Regex


---
layout: 'default'
---

# Regex

**Reg**ular **Ex**prssion
(正規表示式/正則表達式)  
用簡單字串來描述、符合文中全部符合指定格式的字串

## 核心功能: 在一段文字中搜尋特定部分

大部分功能都是以此為展開：
- <details>
    <summary> 文字的搜索與替換 </summary>
    例：

    <!-- 利用vim做演示 -->

    ```txt
    bau -> byau
    ceu -> cyeu
    diu -> dyiu
    fou -> fyou
    gau -> gyau
    ```
    vim cmd: `:%s/\(\w\)\(\w\w\)/\1y\2/g`
  </details>

- <details> 
    <summary> 驗證文字是否符合特定模式（如 Email, IP address, URL, ...）</summary>

    檢查合法 Email:
    `^((?!\.)[\w\-_.]*[^.])(@\w+)(\.\w+(\.\w+)?[^.\W])$`
  </details>


---
layout: 'default'
---

## 基本語法

一個正規表示法通常被稱為是一個模式 (pattern)，用來描述或匹配符合某個樣式規則的字串。  
pattern 一般由字符常量 (literal character constants) 和符號運算子 (operator symbols) 組成。  



- <details>
    <summary>字符：就是單純照字面意思</summary>
    如：<code>Dustin</code> 就是匹配<code>Dustin</code> 這個字串
  </details>

- <details>
    <summary>字符集合：用<code>[]</code>包起來的字符串，代表接受這些字符</summary>
    如：<code>[aiueo]</code>代表我要找<code>aiueo</code>中的其中一個字
    
    也有特殊用法如<code>[a-z]</code>代表所有小寫字母a到z  
    <code>\n</code> 代表新一行  
    <code>\w</code> 代表所有字母、數字、底線  
    <code>\d</code> 任何數字  
    <code>\s</code> 任何空白字元  
    <code>.</code> 代表任何字元  
    ... 等等等等
  </details>

- `|` OR 或

- <details>
    <summary>重複：用<code>{}</code>包起來的數字，代表重複次數</summary>
    如：<code>a{3}</code>代表<code>aaa</code><br/>
    <code>a{3,5}</code>代表<code>aaa</code>、<code>aaaa</code>或<code>aaaaa</code>

    也有特殊的符號來表示常用的次數限制：<br/>
    <code>a+</code>代表一個以上的a<br/>
    <code>a*</code>代表零個以上的a<br/>
    <code>a?</code>代表零個或一個a<br/>

  </details>

- <details>
    <summary>分組：用<code>()</code>包起來的部分，代表一個整體</summary>
    如：<code>(ab)+</code>代表<code>ab</code>、<code>abab</code>、<code>ababab</code>...等等

    在需要嵌套過濾選項常用
  </details>


<!--

open regex101
explain how to use regex101

On every step:
    1) the regex
    2) the test cases
    3) the explanation
    +) the process of how the regex be matched

-->

---
layout: 'default'
---

## 隨堂小測

Regex101: https://regex101.com/r/cHFpfp

一個IP地址的範圍爲0.0.0.0 到 255.255.255.255  

<details>
        <summary>請你用regex來檢查以下是否都是合法的IPv4地址</summary>
<table>
<tbody>

<tr>
<td>10.0.0.30</td>
<td>172.16.0.1</td>
<td>114.514.1919.810</td>
<td>155.255.255&255</td>
</tr>

<tr>
<td>256.0.0.1</td>
<td>192.168.1.1</td>
<td>10.0.0.1</td>
<td>300.200.100.50</td>
</tr>

<tr>
<td>127.0.0.1</td>
<td>8.8.8.8</td>
<td>1.2.3.4.5</td>
<td>192.168.1.</td>
</tr>

<tr>
<td>123.45.67.89</td>
<td>192.168.1.256</td>
<td>192.168.-1.1</td>
<td>192.168.1.1</td>
</tr>

<tr>
<td>203.0.113.0</td>
<td>192.168.1.abc</td>
<td>192.168.1.256</td>
<td>198.51.100.1</td>
</tr>

<tr>
<td>192.168.300.1</td>
<td>0.0.0.0</td>
</tr>

</tbody>
</table>
</details>
---
layout: 'default'
---
## 隨堂小測

Regex101: https://regex101.com/r/cHFpfp

<details>
   <summary>參考解答</summary>
   <code>^(25[0-5]|2[0-4]\d|1\d\d|[1-9]\d|\d)(\.(25[0-5]|2[0-4]\d|1\d\d|[1-9]\d|\d)){3}$</code>

   拆解：
    <ul>
    <li> <code>25[0-5]</code> 代表 250-255 </li>
    <li> <code>2[0-4]\d</code> 代表 200-249 </li>
    <li> <code>1\d\d</code> 代表 100-199 </li>
    <li> <code>[1-9]\d</code> 代表 10-99 </li>
    <li> <code>\d</code> 代表 0-9 </li>
    </ul>

    => (25[0-5]|2[0-4]\d|1\d\d|[1-9]\d|\d) 代表一個0-255的數字
    => (\.(25[0-5]|2[0-4]\d|1\d\d|[1-9]\d|\d)) 前面多了一個點：代表點後接一個0-255的數字
    => {3} 代表重複三次



</details>

---
layout: cover
---

#  非常慢Regex来自Cloudflare,使整个公司癱瘓

---
layout: default
---


##  一個簡單的Regex卻導致全球數億網站無法訪問？

Cloudflare工程師在2019年7月2日進行的一些改進，以偵測跨網站腳本(XSS)攻擊並阻止這些惡意行為。   
惡意攻擊者可以在URL中加入腳本程式碼，當網站載入時自動執行。   
這可能會導致用戶的憑證被發送到駭客的電子郵件地址，從而導致重大損失。  
Cloudflare使用正規表示式來進行檢查可疑的URL。  
然而，他們提交的一個規則有問題，導致整個公司癱瘓。

<details>
<summary>XSS是什麼？</summary>
XSS（跨網站腳本）攻擊是一種網絡安全漏洞，它允許攻擊者將惡意腳本注入到網頁中的用戶端（通常是通過網頁應用程序）上。  
當受害者訪問帶有惡意腳本的網頁時，該腳本就會在他們的瀏覽器中運行，  
進而使攻擊者能夠竊取用戶的cookie、session token等敏感資訊，或者修改網頁上的內容

將這種惡意URL發送給毫無戒備的小白，boom!  
他的帳號就是你的了
</details>

---
layout: default
---
<style>
.small {
font-size: 10px;
}
</style>

##  一個簡單的Regex卻導致全球數億網站無法訪問？
作為內容分發網路(CDN)，CloudFlare在全球的各個地方部署了數千臺的伺服器  
用戶可以向離他們最近的伺服器發送請求  
這些伺服器可以在將請求轉發給源伺服器前進行驗證  
<br/>
在CloudFlare的方案中，安全檢查由他們的WAF(網絡應用安全防火牆)提供  
防火牆規則利用**Regex**來配置  
<details>
<summary>如何利用Regex來過濾惡意URL?</summary>
例
絕大部分的時候，一個正常的URL絕對不會包含SQL指令<br/>
<code>http://example.com/users?id=1; DROP TABLE users;</code><div class="small">(怎麽動不動就Drop別人Table啊</div>
可以使用以下Regex來偵測: <br/>
<code>('|b)(SELECT|INSERT|DROP|UPDATE|DELETE|UNION|EXEC|CREATE|INTO|FROM|WHERE)\b.*</code>
</details>

---
layout: default
---

## 一個簡單的Regex卻導致全球80%網站無法訪問？
所以，工程師只是加了一個檢測規則:  

```txt
?:(?:\"|'|\]|\}|\\|\d|(?:nan|infinity|true|false|null|undefined|symbol|math)|\`|\-|\+)+[)]*;
?((?:\s|-|~|!|{}|\|\||\+)*.*(?:.*=.*)))
```

- `(?:nan|infinity|true|false|null|undefined|symbol|math)` 是javascript的關鍵字
- `\"|'|\]|\}` 在嘗試尋找跳脫html或javascript的字元 (經典 'OR 1=1')


<!-- 可以看到，他在匹配一些javascript的關鍵字 -->
<!-- 以及一些可以跳脫html或javascript的字符，如引號和大括號 -->
<!-- 也可以看到他在匹配一些URL查詢字符串(`param=query_string`)，這是XSS常見切入點 -->

<br/>

然後就發了一個拉取請求到CloudFlare的代碼倉庫  
CI build了包並跑了所有測試，讓審查人員相信這些改動是安全的  
團隊的其他人員看了看表示看起來不錯就批准了並合併了修改  
在這後CI發佈了新的release，在經過管理員批准後會自動部署到伺服器上  


---
layout: default
---

<style>
.small {
font-size: 10px;
}
</style>
## 批准部署SOP的漏洞

一般來說，CloudFlare的所有改動應遵守以下流程
1. 自家員工的DOG節點
2. 非付費用戶的PIG節點
3. 多個客戶的Canary節點
4. 部屬到全世界

**BUT**  
WAF的部署是直接部署到全世界的，以迅速應對新的威脅  
而且一般來說，伺服器的升級是分批進行的<div class="small">你也不想你的服務突然同時下線吧</div>

**しかし**  
WAF會直接部屬到一個叫Quicksilver的伺服器  
這些請求不需要任何停機時間，使得WAF規則可以被直接部署到全球

---
layout: default
---

## 批准部署SOP的漏洞

所以這條爛透了的規則就直接被部屬到了CloudFlare全球的伺服器上

3分鐘後他們記錄到了WAF錯誤  
這代表  
全世界的WAF伺服器都炸了  
他們發現伺服器的的CPU以100%超負荷運行  
結果他們損失了80%的客戶流量

數億的網站都使用CloudFlare的CDN
意味著這些網站也掛了

最終他們關閉了WAF並回滾了那條糟糕的規則

---
layout: default
---

## 為什麼防火牆導致CPU使用率暴增？

問題在於表達試的後綴：`.*(?:.*=.*)`

<details>
<summary>非捕獲組(non-capturing group)是啥</summary>
他代表要匹配的內容但不包含在輸出中

input: `http://example.com/foo`  
regex: `(?:https?)://([\w]+)(/[\w/]*)`  
output: `example.com` `/foo`

</details>

<details>
<summary>所以regex引擎要匹配如下規則：</summary>

- `.*`: 任意數量的字元
- `.*`: 任意數量的字元
- `=` : 一個等號
- `.*`: 任意數量的字元

</details>
<!--切regex101做演示-->

---
layout: default
---

## 為什麼防火牆導致CPU使用率暴增？

![](https://blog.cloudflare.com/content/images/2019/07/failing-x-x.png)

---
layout: end
---
