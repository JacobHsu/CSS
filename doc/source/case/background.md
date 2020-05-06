title: background
---

[使用 CSS 多重背景](https://developer.mozilla.org/zh-TW/docs/Web/CSS/CSS_Background_and_Borders/Using_CSS_multiple_backgrounds)

藉由 CSS3 我們可以對元素使用 多重背景。每個設定的背景被一個個分層，第一個背景在最上面，最後一個背景是在最下面一層。 記得只有最後一個背景可以設定 `background-color`。

簡易的表達方式:

```css
.myclass {
  background:
      background 1, //第一層
      background 2,
      ...,
      background N;  //最後一層
}
```

[background-color](https://developer.mozilla.org/zh-TW/docs/Web/CSS/background-color)