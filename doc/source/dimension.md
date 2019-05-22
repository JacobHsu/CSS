title: CSS 尺寸属性（Dimension）
---

# CSS3新單位－－vh vw

vh、vw在使用上與百分比%很相似，
`vh`代表`view height`，指的是螢幕可視範圍高度的百分比，
`vw`代表`view width` ，指的是指螢幕可視範圍寬度的百分比。


[CSS width](http://www.w3school.com.cn/cssref/pr_dim_width.asp)  

寬度值    | 語法           | 說明
---------|:--------------:|------------------------
auto     | width:auto;    | 自動判斷網頁元素的寬度。
長度     | width:數字+單位 |  可接受的單位有 px, em, cm 等網頁標準單位。
%        | width:數字%    |  利用百分比設定網頁元素寬度，需要有比較的參考。
inherit  | width:inherit; | 繼承自父層的寬度屬性值。


```css
iframe {
    width: inherit;
}
```