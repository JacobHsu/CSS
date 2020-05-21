title: 外邊距重疊
---

當塊級元素（block）的上外邊距(margin-top)和下外邊距(margin-bottom)同時都有設定時**只會保留最大邊距**，這種行為稱為邊界摺疊（margin collapsing），有時也翻譯為外邊距重疊。

> 注意有設定`float`和`position=absolute`的元素不會產生外邊距重疊行為。

有三種情況會形成外邊距重疊：

## 同一層相鄰元素之間

當上下相鄰的兩個塊級元素相遇
相鄰的兩個元素之間的外邊距重疊，除非後一個元素加上`clear-fix`清除浮動。

```html
<style>   
p:nth-child(1){   
  margin-bottom: 13px; 
}   
p:nth-child(2){  
  margin-top: 87px;  
} 
</style>
 
<p>下邊界範圍會...</p>
<p>...會跟這個元素的上邊界範圍重疊。</p>
```

這個例子如果以為邊界會合併的話，理所當然會猜測上下2個元素會合併一個`100px`的邊界範圍，
但其實會發生邊界摺疊，只會挑選最大邊界範圍留下，所以這個例子的邊界範圍其實是`87px`。


解決方法：

儘量只給一個盒子添加margin值

## 沒有內容將父元素和後代元素分開

對於兩個嵌套關係的塊元素
出現父塊元素和其內後代塊元素外邊界重疊，重疊部分最終會溢出到父級塊元素外面。

```html
<style type="text/css">
    section    {
        margin-top: 13px;
        margin-bottom: 87px;
    }

    header {
        margin-top: 87px;
    }

    footer {
        margin-bottom: 13px;
    }
</style>

<section>
    <header>上邊界重疊 87</header>
    <main></main>
    <footer>下邊界重疊 87 不能再高了</footer>
</section>
```

解決辦法：

1. 給父元素定義上邊框
2. 給父元素定義上內邊距
3. 給父元素添加 overflow：hidden；
4. 添加浮動
5. 添加絕對定位

## 空的塊級元素

當一個塊元素上邊界margin-top 直接貼到元素下邊界margin-bottom時也會發生邊界摺疊。

```html
<style>
​​​​​​p {
  margin: 0;  
}
div {
  margin-top: 13px;
  margin-bottom: 87px;
}
</style>

<p>上邊界範圍是 87 ...</p>
<div></div>
<p>... 上邊界範圍是 87</p>
```

[CSS中如何解决外边距塌陷问题？](https://juejin.im/post/5eb82c2fe51d451ef5378f82?utm_source=gold_browser_extension)