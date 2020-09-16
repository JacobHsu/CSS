title: QA
---

圖片格式

前端的圖片分類格式,其實是性能優化的很大部分。選擇好圖片的類型，對前端的性能影響非常大

| 圖片類型 | 介紹                                                            | 使用場景                                                           |
|----------|-----------------------------------------------------------------|--------------------------------------------------------------------|
| png      | 適合顏色簡單，但是對圖片質量比較高。日常用的png8，此外還有png32 | 適合logo體積太大一般不用                                           |
| jpeg     | 不影響圖片質量的情況有損壓縮，banner圖。適合大圖。              | 壓縮後大小可省略很多，一般大圖使用                                 |
| svg      | 對性能有損耗，體積小，壓縮性搶。可在質量不下降的過程被放大      | 部分瀏覽器兼容性不太好                                             |
| webp     | 只針對谷歌，兼容性不好。圖片大小能壓縮30~40%。                  | 谷歌瀏覽器用，如有非常注重性能的產品，可判斷瀏覽器加載不同類型圖片 |
| base64   | 壓縮成字符流，實際大小是變大了，但是好處就是減少了http請求      | 一般也針對小圖標                                                   |


## 網頁文字單位，px、em、rem、% 的差別

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