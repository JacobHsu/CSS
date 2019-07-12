title: QA
---

網頁文字單位，px、em、rem、% 的差別

哪一個是絕對單位？哪一個是相對單位？
px 是絕對單位；
em 是相對單位，其文字大小是相對於父元素 (parent element)；
rem 是相對單位，其文字大小是相對於根元素 (root element)，根元素就是 <html> 標籤

## [保持正圓或正方形的圖片](https://zoneless.blog/2017/06/17/css-responsive-circle-or-square-image/)  

```css
.img-circle>img{    
    width: 100% !important;		
    height: 100% !important;		
    object-fit: cover;	
}
```


## [html img圖片不變形等比例縮放,兼容ie6](https://blog.csdn.net/Lpandeng/article/details/72520631)

需要設置好寬度限制,如`max-width:300px`  
然後對父級使用`overflow:hidden`隱藏溢出圖片  

```css
.divcss{ border:1px solid #000; width:300px; height:100px; overflow:hidden} 
.divcss img{max-width:300px;}
```

## radio
[CSS: how to make label appear right of the radio?](https://stackoverflow.com/questions/10022363/css-how-to-make-label-appear-right-of-the-radio)  
[Hide radio button while keeping its functionality](https://stackoverflow.com/questions/29346385/hide-radio-button-while-keeping-its-functionality)  