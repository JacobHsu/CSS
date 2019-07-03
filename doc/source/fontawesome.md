title: Font Awesome
---

[Font Awesome](https://fontawesome.com/)  


過去只有 fa 而在 FontAwesome 5 [將圖示分成了 4 大類](https://pjchender.blogspot.com/2017/12/5-fontawesome-5.html) 前綴分別代表   
`fas` Solid , `far` Regular, `fal` Light 和 `fab` Brands 


[fontawesome 5 font-family not work](https://stackoverflow.com/questions/47788847/fontawesome-5-font-family-not-work/47789198)

```css
a::after {
  content: "\f007";
  font-family: 'Font Awesome\ 5 Free';
  font-weight: 900;
}
```