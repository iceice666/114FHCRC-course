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
title: 'Regex'
titleTemplate: '%s - Regex'
colorSchema: dark
defaults:
  layout: 'default'
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
    <summary>文字的搜索與替換</summary>
    例：

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
    <summary>驗證文字是否符合特定模式（如Email, IP address, URL, ...）</summary>

    檢查合法IP address:
    `^((25[0-5]|(2[0-4]|1\d|[1-9]|)\d)\.?\b){4}$`
  </details>


---
layout: 'default'
---

## 如何使用
