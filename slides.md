---
fonts:
  # 基础字体
  sans: 'Noto Sans Traditional Chinese '
  # 与 windicss 的 `font-serif` css 类一同使用
  serif: 'Noto Serif Traditional Chinese '
  # 用于代码块、内联代码等
  mono: 'Noto Sans Mono'
layout: intro
theme: default
drawings: 
  presenterOnly: true 
---

# 報告、筆記的好幫手
## Markdown <ri-markdown-fill />

---
layout: default
---

# 什麼是 Markdown 

#### Markdown 是一種輕量級的標記語言，通過使用簡單的符號和標記來表示文本的結構和樣式。它的語法簡潔明了，使得編寫和閱讀文本更加輕鬆自然。

Markdown 的優勢包括：

- 易學易用：Markdown 使用簡單的語法，不需要繁瑣的排版和格式設置，非常適合快速撰寫內容。
- 跨平台支持：Markdown 可以在任何文本編輯器中編寫，並且幾乎所有的瀏覽器和應用程序都支持 Markdown 的閱讀和展示。
- 清晰結構：Markdown 的標記語法直觀明確，使得文本的結構和內容易於理解和閱讀。
- 多格式轉換：Markdown 可以方便地轉換為其他格式，如 HTML、PDF、Word 等，使得文檔在不同平台和場景中的使用更加靈活。

 

### Try try see : [HackMD](https://hackmd.io/new)

<!--  易學易用： typora notion -->
---
layout: two-cols
---
# Markdown 語法


## 1. 標題


```md
# 一級標題

## 二級標題

### 三級標題

#### 四級標題

##### 五級標題

###### 六級標題
```
::right::
<br/>
<br/>
<br/>
<br/>
<br/>

# 一級標題

## 二級標題

### 三級標題

#### 四級標題

##### 五級標題

###### 六級標題

---
layout: two-cols
---
# Markdown 語法

## 2. 段落和換行

```md

這是一個段落

這是另一個段落

如果有需要，可使用<br/>強制換行

```

::right::

<br/>
<br/>
<br/>
<br/>
<br/>

這是一個段落

這是另一個段落

如果有需要，可使用`<br/>` <br/>強制換行

---
layout: two-cols
---
# Markdown 語法


## 3. 字體樣式
```md
*斜體*

**粗體**

***斜體+粗體=粗斜體***

<del> 刪除線 </del>

<u>底線</u>
```
::right::

<br/>
<br/>
<br/>
<br/>
<br/>


*斜體*

**粗體**

***斜體+粗體=粗斜體***

<del> 刪除線 </del>

<u>底線</u>

<!-- ~在hackmd中是刪除線 -->

---
layout: two-cols
---
# Markdown 語法

## 4. 鏈結

```md
這是一個鏈結
[link](http://example.com)

這個會被變成（編譯成) 一個鏈結
http://example.com
```
::right::

<br/>
<br/>
<br/>
<br/>
<br/>
這是一個鏈結

[link](http://example.com)

這個會被編譯成一個鏈結

http://example.com
---
layout: two-cols
---
# Markdown 語法

## 4. 鏈結
```md
這是一個圖片
![](https://example/image.jpg)
```

<del> sensei 總力戰別凹了來hardcore擺爛吧 </del>

::right::

這是一個圖片....?

![](/sensei.gif)

<!-- https://picsum.photos -->

---
layout: two-cols
---
# Markdown 語法
## 5. 引言 (quote)

```md

> 這是一個單行引言

> 這是
一個
多行
引言

> 多個單行引言
> 合併起來
> 就變成了多行引言

> 引言裡也可以嵌套引言
> 引言裡也可以包含其他語法
> # 這是一個標題
> ## 這是一個次標題
> 這是內文
> > 這是一個嵌套的引言
> bra bra bra ...

```

::right::

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

> 這是一個單行引言

> 這是
一個
多行
引言

> 多個單行引言
> 合併起來
> 就變成了多行引言

> 引言裡也可以嵌套引言
> 引言裡也可以包含其他語法

> # 這是一個標題
> ## 這是一個次標題
> 這是內文
> > 這是一個嵌套的引言
> bra bra bra ...

<!-- 換行會變成空格 -->
---
layout: two-cols
---
# Markdown 語法
## 6. 列表
```md
- 可以使用減號
+ 加號也可以
* 星號也能

1. 使用數字後面加一個英文句點
2. 就可以創造一個有序列表

114. 當然如果你要亂序排列
514. 也是可行的

項目清單很可能會不小心產生，像是下面這樣的寫法

1986. What a great season.

以上的結果並不是我們希望的
要避免的話，我們可以加上反斜線


1986\. What a great season.

```
::right::
<br/>
<br/>
<br/>
<br/>

- 可以使用減號
+ 加號也可以
* 星號也能

1. 使用數字後面加一個英文句點
2. 就可以創造一個有序列表

114. 當然如果你要<del>塞私貨</del>亂序排列
514. 也是可行的

項目清單很可能會不小心產生，像是下面這樣的寫法
1986. What a great season.

以上的結果並不是我們希望的，要避免的話，我們可以加上反斜線

1986\. What a great season.

---
layout: two-cols
---
# Markdown 語法
## 6. 列表

```md
- 要讓清單看起來更漂亮，可以使用縮排

- 愛情

  愛情就是死循環，一旦執行就陷進去了；
  愛上一個人，就是內存洩漏–你永遠釋放不了；
  真正愛上一個人的時候，那就是常量限定，永遠不會改變；
  女朋友就是私有變量，只有我這個類才能調用；
  情人就是指針，用的時候一定要注意，要不然就帶來巨大的災難。

- [ ] 列表和TODO一起食用效果更佳
- [x] 在TODO中使用x來標記這個TODO為完成

```
::right::

<br/>
<br/>
<br/>
<br/>
<br/>

- 要讓清單看起來更漂亮，可以使用縮排

- 愛情

  愛情就是死循環，一旦執行就陷進去了；
  愛上一個人，就是內存洩漏–你永遠釋放不了；
  真正愛上一個人的時候，那就是常量限定，永遠不會改變；
  女朋友就是私有變量，只有我這個類才能調用；
  情人就是指針，用的時候一定要注意，要不然就帶來巨大的災難。

- [ ] 列表和TODO一起食用效果更佳
- [x] 在TODO中使用`x`來標記這個TODO為完成

---
layout: two-cols
---
# Markdown 語法
## 7. 表格


```md
利用`|` 和 `-` 來創建表格
|foo|bar|
|---|---|
|abc|xyz|
|114514|1919810|
```
::right::
<br/>
<br/>
<br/>
<br/>
<br/>

|foo|bar|
|---|---|
|abc|xyz|
|114514|1919810|

---
layout: two-cols
---
# Markdown 語法
## 8. 代碼塊 & 程式碼

```md
這是一個正常語句

`使用單個反引號包裹就會變成代碼塊`

使用三個反引號包裹的語句就會變成程式碼

\```java
Gril gf = new Gril();
My.gf = gf;

\```

```

::right::

<br/>
<br/>
<br/>
<br/>
<br/>

這是一個正常語句

`使用單個反引號包裹就會變成代碼塊`

使用三個反引號包裹的語句就會變成程式碼

```java
Gril gf = new Gril();
My.gf = gf;
```


---
layout: default
---
# 用Markdown做簡報？泰褲啦！

### Slidev

Slidev 旨在為開發者提供靈活性和交互性，通過使用他們已經熟悉的工具和技術，使他們的演示文稿更加有趣、更具表現力和吸引力。

當使用所見即所得的編輯器時，人們很容易被樣式選項所干擾。
Slidev 通過分離內容和視覺效果來彌補這一點。

這使你能夠一次專注於一件事，同時也能夠重複使用社區中的主題。
Slidev並不尋求完全取代其他幻燈片製作工具。
相反，它專注於迎合開發者社區的需求。

[Slidev Doc](https://cn.sli.dev/guide/why.html)

<small> 這個PPT也是利用Slidev製作的 </small>


---
layout: default
---
# Markdown 進階

## 編譯是什麼？能吃嗎？

Markdown 可以變成我們所看到的樣子，是因為有一個叫做編譯器的東西，這個東西會把 Markdown 語法轉換成 HTML 語法，讓瀏覽器能夠正確顯示出來。

所以，Markdown 語法其實就是一種標記語言，和 HTML 一樣，只是比 HTML 簡單很多。

也因為他是被編譯成 HTML 的，所以他可以和 HTML 混用，這樣就可以做出更多更複雜的東西了。


---
layout: default
---
# Markdown 進階

## 有序列表的編譯

這裡有一個索引不連續的有序列表

```md

1. foo
1. bar
4. halo
5. nihao
1. mian
4. return o


```

---
layout: two-cols
---
# Markdown 進階

## 有序列表的編譯

他會被編譯成：
```md
<ol>
    <li> foo </li>
    <li> bar </li>
    <li> halo </li>
    <li> nihao </li>
    <li> mian </li>
    <li> return o </li>
</ol>

```
::right::


<br/>
<br/>
<br/>
<br/>
<br/>

也就是：

<ol>
    <li> foo </li>
    <li> bar </li>
    <li> halo </li>
    <li> nihao </li>
    <li> mian </li>
    <li> return o </li>
</ol>

這就能解釋爲什麼索引會自動排序

因爲HTML幫你排好了 :D

---
layout:  two-cols
---
# Markdown 進階

## 更大、更強的table

<style>
code {
    font-size:13px;
}
</style>

<table>
  <caption>Sample Table</caption>
  <thead>
    <tr>
      <th>Header 1</th>
      <th>Header 2</th>
      <th>Header 3</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Row 1, Cell 1</td>
      <td>Row 1, Cell 2</td>
      <td>Row 1, Cell 3</td>
    </tr>
    <tr>
      <td>Row 2, Cell 1</td>
      <td>Row 2, Cell 2</td>
      <td>Row 2, Cell 3</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <td colspan="3">Footer Content</td>
    </tr>
  </tfoot>
</table>

HTML \<table\> 教學
[W3S Table](https://www.w3schools.com/html/html_tables.asp)

::right::

```md
<table>
  <caption>Sample Table</caption>
  <thead>
    <tr>
      <th>Header 1</th>
      <th>Header 2</th>
      <th>Header 3</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Row 1, Cell 1</td>
      <td>Row 1, Cell 2</td>
      <td>Row 1, Cell 3</td>
    </tr>
    <tr>
      <td>Row 2, Cell 1</td>
      <td>Row 2, Cell 2</td>
      <td>Row 2, Cell 3</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <td colspan="3">Footer Content</td>
    </tr>
  </tfoot>
</table>
```

---
layout: default
---
# Markdown 進階

## \<iframe\> ：強力外部支援！

<iframe width="560" height="315" src="https://www.youtube.com/embed/t9N5Msr_Ftg" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

<del><small>這部我搬的，誒嘿嘿</small></del>

---
layout: two-cols
---
# Markdown 進階

## 連結路徑問題

這裡有一些文件和資料夾

``` txt
/ (Root)
  ├───Folder A
  │   ├───File A1
  │   └───File A2
  ├───Folder B
  │   ├───Subfolder B1
  │   │   ├───File B11
  │   │   └───File B12
  │   ├───File B2
  │   └───Current file.md
  ├───File C1
  └───File C2


```

::right::

現在我們的檔案在 `/Folder B/Current file.md`

> 臨時抱佛腳
> - `.` 是當前目錄，也就是 `/Folder B/`
> - `..` 是上一層目錄，也就是 `/`

- 要連結到 `File B2`，我們可以這樣寫：<br/>`./File B2` 或 `File B2`

- 要連結到 `File B1`，我們可以這樣寫：<br/>`./Subfolder B1/File B1` 或 `Subfolder B1/File B1`

- 要連結到 `File C1`，我們可以這樣寫：<br/>`../File C1`

- 要連結到 `File A1`，我們可以這樣寫：<br/>`../Folder A/File A1`
