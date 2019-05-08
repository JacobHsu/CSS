title: 垂直置中
---

## 使用 Flexbox

```css
    display:flex;   
    align-items:center;
    justify-content:center;
```

https://jsbin.com/ticuyivabi/edit?html,css,output
```css
.use-flexbox{
    display:flex;
    align-items:center;
    justify-content:center;
    width:200px;
    height:150px;
    border:1px solid #000;
}
.use-flexbox div{
    width:100px;
    height:50px;
    background:#099;
}
```

## 絕對定位

`position:absolute`
將上下左右的數值都設為 0，再搭配一個`margin:auto`  
其父元素的 position 必須要指定為 `relative` 


https://jsbin.com/dunejehako/1/edit?html,css,output

```css
.use-absolute{
    position: relative;
    width:200px;
    height:150px;
    border:1px solid #000;
}
.use-absolute div{
    position: absolute;
    width:100px;
    height:50px;
    top:0;
    right:0;
    bottom:0;
    left:0;
    margin:auto;
    background:#f60;
}
```

absolute + translate

此置中的定位物件不需要固定的寬跟高，
我們利用絕對定位時的left跟top設定物件的上方跟左方各都為50%，
再利用 `translate(-50%, -50%)` 位移置中物件自身寬與高的 50% 就能達成置中的目的了。

```css
.use-absolute div{
    position: absolute;
    top:50%;
    left: 50%;
    transform: translate(-50%, -50%);
}
```

### examples 

https://jsbin.com/yisulifovu/edit?html,css,output

#### Rerences

https://www.oxxostudio.tw/articles/201502/css-vertical-align-7methods.html
https://www.oxxostudio.tw/articles/201501/css-flexbox.html  
https://css-tricks.com/snippets/css/a-guide-to-flexbox/
http://csscoke.com/2018/08/21/css-vertical-align/
http://zh-tw.learnlayout.com/position.html
https://developer.mozilla.org/zh-CN/docs/Web/CSS/position