title: display 
---


## display : none

把 HTML 元件的 display 設為 none 就是不顯示這個東西。 

`display : none` 和 `visibility : hidden` 的差別是 

`display : none` 這個東西就不見了，不佔空間， 
`visibility : hidden` 只是隱形看不見，還是有佔空間。

## display : inline

`<a> 、 <span> 、 <b> 、 <i> 、 <img> 、 <iframe>` ... 
這幾個 HTML 元素預設的 display 屬性是 inline ，

用最簡單的講法解釋 `display : inline` 
就是兩個 `display : inline` 的**元素連在一起會在同一行，不會換行**。

附帶一提，`display : inline` 元素不該包住 `display : block`元素。

## display : block

<div> 、 <p> 、 <h1> 、 <h2> ... 
這幾種 HTML 元素預設的 display 屬性是 block，

簡單講就是不管 `display : block` 元素的前面後面是什麼，
碰到 `display : block` 元素就是**會換行**，而 `display : block` 元素的寬度預設會撐到最大。

要將 display : block 元素水平置中，方法是在此元素加上 `margin: 0 auto;


## display : inline-block

inline-block顧名思義就是兩種性質都來一點。
它的外在是 inline 內在是 block，

外在像`inline`不會換行且會自適應大小，
內在像`block`可以設定`width、height、margin、background-img`…等參數。

用 CSS 讓連結用圖片顯示就是 `inline-block` 常見的應用。
