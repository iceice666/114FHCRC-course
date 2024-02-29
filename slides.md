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
        <summary>請你用regex來檢查以下是否都是合法的IP地址</summary>
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
layout: end
---
