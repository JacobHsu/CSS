title: 居中
---

### 水平居中對齊

要水平居中對齊一個元素, 可以使用 `margin: auto;`

```css
#main {
  width: 600px;
  max-width: 600px;
  margin: 0 auto; 
}
```

設定區塊元素的 width 屬性，可以避免該元素從左到右撐滿容器，然後你可以設定左右外邊距（`margin-left` 與 `margin-right`）為 auto 來使其水平居中。元素在顯示的時候，只會顯示到你所指定的寬度，然後剩餘的寬度平均的散落在左右兩邊的邊距上。

唯一的問題是，當瀏覽器視窗寬度比元素的寬度還要窄時，瀏覽器就會出現水平捲軸。
使用 `max-width` 替代 width 可以更完美的處理當瀏覽器視窗小於元素寬度的情況。

### 垂直置中

[CSS 垂直置中的七個方法](https://www.oxxostudio.tw/articles/201502/css-vertical-align-7methods.html) 

####　transform

transform 是 CSS3 的新屬性，主要掌管元素的變形、旋轉和位移，利用 transform 裏頭的 translateY ( 改變垂直的位移　）
需要注意的地方是，子元素必須要加上`position:relative`　不然就會沒有效果

```css
.use-transform div{
    position: relative;
    width:100px;
    height:50px;
    top:50%;
    transform:translateY(-50%);
    background:#095;
}
```

### References

[CSS 佈局 - 水平 & 垂直對齊](http://www.runoob.com/css/css-align.html)  
學習 CSS 版面配置 [margin-auto](http://zh-tw.learnlayout.com/margin-auto.html)  
