# Three-Column Layout

## float佈局

```html
<div class="left"></div>
<div class="right"></div>
<div class="center">...</div>
```
```css
.layout.float .left{
  float: left;
  width: 300px;
  background: red;
}
```

<iframe height="265" style="width: 100%;" scrolling="no" title="三欄佈局 float " src="https://codepen.io/JacobHsu/embed/KKdRJOR?height=265&theme-id=light&default-tab=html" frameborder="no" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/JacobHsu/pen/KKdRJOR'>三欄佈局 float </a> by JacobHsu
  (<a href='https://codepen.io/JacobHsu'>@JacobHsu</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

## absolute佈局

```css
.layout.absolute .left{
  position: absolute;
  left: 0;
  width: 300px;
  background: red;
}
```

<iframe height="265" style="width: 100%;" scrolling="no" title="三欄佈局 absolute" src="https://codepen.io/JacobHsu/embed/gOazEaW?height=265&theme-id=light&default-tab=css" frameborder="no" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/JacobHsu/pen/gOazEaW'>三欄佈局 absolute</a> by JacobHsu
  (<a href='https://codepen.io/JacobHsu'>@JacobHsu</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

## flex佈局

```css
.layout.flex .wrapper{
    display: flex;
    width: 100%;
    min-height: 100px;
}
.layout.flex .left{
    width: 300px;
    background: red;
}
```

<iframe height="265" style="width: 100%;" scrolling="no" title="三欄佈局 flex" src="https://codepen.io/JacobHsu/embed/NWGMJpM?height=265&theme-id=light&default-tab=css" frameborder="no" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/JacobHsu/pen/NWGMJpM'>三欄佈局 flex</a> by JacobHsu
  (<a href='https://codepen.io/JacobHsu'>@JacobHsu</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

## table佈局

```css
.layout.table .wrapper{
  display: table;
  width: 100%;
  min-height: 100px;
}
.layout.table .left{
  display: table-cell;
  width: 300px;
  background: red;
}
```

<iframe height="265" style="width: 100%;" scrolling="no" title="三欄佈局 table" src="https://codepen.io/JacobHsu/embed/abvGMVO?height=265&theme-id=light&default-tab=css" frameborder="no" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/JacobHsu/pen/abvGMVO'>三欄佈局 table</a> by JacobHsu
  (<a href='https://codepen.io/JacobHsu'>@JacobHsu</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

## grid佈局

```css
.layout.grid .wrapper{
  display: grid;
  grid-template-columns: 300px auto 300px;
  grid-template-rows: 100px;
  width: 100%;
}
.layout.grid .left{
  background: red;
}
```

<iframe height="265" style="width: 100%;" scrolling="no" title="三欄佈局 grid" src="https://codepen.io/JacobHsu/embed/xxwjBpw?height=265&theme-id=light&default-tab=html" frameborder="no" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/JacobHsu/pen/xxwjBpw'>三欄佈局 grid</a> by JacobHsu
  (<a href='https://codepen.io/JacobHsu'>@JacobHsu</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

## 每種佈局的優缺點

### float 佈局

優點： 比較簡單，兼容性也比較好。只要清除浮動做的好，是沒有什麼問題的
缺點：浮動元素是`脫離文檔流`，要做清除浮動，這個處理不好的話，會帶來很多問題，比如高度塌陷等。

### absolute佈局

優點：很快捷，設置很方便，而且也不容易出問題
缺點：絕對定位是`脫離文檔流的`，意味著下面的所有子元素也會脫離文檔流，這就導致了這種方法的有效性和可使用性是比較差的。

### flex 佈局

優點：簡單快捷
缺點：不支持 IE8 及以下

###  table佈局

優點：實現簡單，代碼少
缺點：當其中一個單元格高度超出的時候，兩側的單元格也是會跟著一起變高的，而有時候這種效果不是我們想要的

### grid佈局

跟 flex 相似。  
缺點：不支持 IE8 及以下