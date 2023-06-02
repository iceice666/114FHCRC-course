
# 一級標題

## 二級標題

### 三級標題

#### 四級標題

##### 五級標題

###### 六級標題

---

這是一個段落

這是另一個段落

如果有需要，可使用`<br/>`強制換行

---

*斜體*

**粗體**

***斜體+粗體=粗斜體***

<del> 刪除線 </del>

<u>底線</u>

---

這是一個鏈結

[link](http://example.com)

這個會被編譯成一個鏈結

http://example.com


這是一個圖片....?

![](https://picsum.photos/200/300)



---

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

---

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

---

- 要讓清單看起來更漂亮，可以使用縮排

- 愛情

  愛情就是死循環，一旦執行就陷進去了；
  愛上一個人，就是內存洩漏–你永遠釋放不了；
  真正愛上一個人的時候，那就是常量限定，永遠不會改變；
  女朋友就是私有變量，只有我這個類才能調用；
  情人就是指針，用的時候一定要注意，要不然就帶來巨大的災難。

- [ ] 列表和TODO一起食用效果更佳
- [x] 在TODO中使用x來標記這個TODO為完成

---

|foo|bar|
|---|---|
|abc|xyz|
|114514|1919810|

---

這是一個正常語句

`使用單個反引號包裹就會變成代碼塊`

使用三個反引號包裹的語句就會變成程式碼

```java
Gril gf = new Gril();
My.gf = gf;
```


---

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
