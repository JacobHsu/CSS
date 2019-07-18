title: Position
---


## static

`static（靜態定位）`：默認值。沒有定位，元素出現在正常的流中（忽略 top, bottom, left, right 或者 z-index 聲明）。

static 是預設值。任何套用 position: static; 的元素「不會被特別定位」在頁面上特定位置，而是照著瀏覽器預設的配置自動排版在頁面上，所有其他的屬性值都代表該元素會被定位在頁面上。

## relative

`relative（相對定位）` 生成相對定位的元素，通過`top,right,bottom,left`的設置相對於其正常（原先本身）位置進行定位。可通過`z-index`進行層次分級。　

定位為relative的元素脫離正常的文本流中，但其在**文本流中的位置依然存在**。  

1)如果沒有TRBL，以父級的左上角，在沒有父級的時候，他是參照瀏覽器左上角(到這裡和absolute一樣)，如果在沒有父級元素的情況下，存在文本，則以文本的底部為原始點進行定位並將文字斷開(和absolute不同)。

2)如果設定TRBL，並且父級沒有設定position屬性，仍舊以父級的左上角為原點進行定位(和absolute不同)。

3)如果設定TRBL，並且父級設定position屬性(無論是absolute還是relative)，則以父級的左上角為原點進行定位，位置 由TRBL決定(前半段和absolute一樣)。如果父級有Padding屬性，那麼就以**內容區域的左上角**為原點，進行定位(後半段和absolute不同)

總結，無論父級存在不存在，無論有沒有TRBL(`top,right,bottom,left`)，均是**以父級的左上角**進行定位，但是父級的Padding屬性會對其影響。　

## fixed

`fixed（固定定位）`的元素會相對於**瀏覽器視窗**來定位，這意味著即便頁面捲動，它還是會固定在相同的位置。和 relative 一樣，我們會使用`top,right,bottom,left`屬性來定位。

應用 可用於 banner關閉按鈕

## absolute

`absolute（絕對定位）`：生成絕對定位的元素，相對於 **static 定位以外的第一個父元素**進行定位。元素的位置通過`top,bottom,left,right`屬性進行規定。可通過`z-index`進行層次分級。

`絕對定位（position: absolute）`元素的定位是在他所處上層容器的相對位置。如果這個套用 `position: absolute` 的元素，其上層容器並沒有「可以被定位」的元素的話，那麼這個元素的定位就是相對於該網頁所有內容（也就是 <body> 元素）最左上角的絕對位置，看起來就是這張網頁的絕對位置一樣，所以當你的畫面在捲動時，該元素還是會隨著頁面捲動。  

> 請記得，只有套用 `position: static` 的元素屬於「不會被特別定位」的元素，套用 `static`以外的屬性值都算是「可以被定位」的元素。

定位為absolute的層脫離正常文本流，但與relative的區別是其在**正常流中的位置不再存在** 

1)如果沒有TRBL(top、right、bottom、left)，以父級的左上角，在沒有父級的時候，他是參照瀏覽器左上角,如果在沒有父級元素的情況下，存在文本，則以它前面的最後一個文字的右上角為原點進行定位但是不斷開文字，覆蓋於上方。

2)如果設定TRBL，並且父級沒有設定position屬性，那麼當前的absolute則以**瀏覽器左上角**為原始點進行定位，位置將由TRBL決定。

3)如果設定TRBL，並且父級設定position屬性(無論是absolute還是relative)，則**以父級的左上角**為原點進行定位，位置由 TRBL決定。即使父級有Padding屬性，對其也不起作用，說簡單點就是：它只堅持一點，就以父級左上角為原點進行定位，父級的padding對其根本沒有影響。 

以上三點可以總結出，若想把一個定位屬性為absolute的元素定位於其父級元素內，只有滿足兩個條件：

> 第一：設定TRBL(`top,right,bottom,left`) 第二：父級設定`Position`屬性

上面的這個總結非常重要，可以保證你在用absolue佈局頁面的時候，不會錯位，並且隨著瀏覽器的大小或者顯示器分辨率的大小，而不發生改變。
只要有一點不滿足，元素就會以**瀏覽器左上角為原點**，這就是初學者容易犯錯的一點，已經定位好的板塊，當瀏覽器的大小改變，父級元素會隨之改變，但是設定Position屬性為absolute的板塊和父級元素的位置發生改變，錯位了，這就是因為此時元素以瀏覽器的右上角為原點的原因。


`position:static`  
元素的 position 屬性默認值為:static，即該元素出現在文檔的常規位置，不會重新定位。

通常此屬性值可以不設置，除非是要覆蓋之前的定義。

`position:relative`  
設置了 position:relative，便可以結合`top 、 bottom、 left 、 right` 的屬性來偏移其文檔的常規位置。

`position:absolute`  
設置了 position:absolute，即絕對定位，便可以將元素放在文檔中任何想放的位置。

`position:relative + position:absolute` 

設置div-1的位置為 relative ， div-1中元素的定位都將相對於div-1。現將div-1a的position設為:absolute，可以實現將其置於div-1的右上角：

```css
#div-1 {
 position:relative;
}
#div-1a {
 position:absolute;
 top:0;
 right:0;
 width:200px;
}
```

`float(浮動)`   

針對高度不定的情況，絕對定位不好用。
可以盡量使用向左或向右浮動來實現文字環繞，特別是環繞圖片。

多列浮動後清除浮動

將元素浮動後，再使用"clear" 清除浮動，後面內容拉向下。

```css
#div-1a {
 float:left;
 width:190px;
}
#div-1b {
 float:left;
 width:190px;
}
#div-1c {
 clear:both;
}
```

[學習 CSS 版面配置](http://zh-tw.learnlayout.com/position.html)  
[10步掌握CSS定位](http://www.see-design.com.tw/i/css_position.html)  