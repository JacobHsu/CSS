title: input html
---

# CSS `<input>`寬度不超過`<div>`

[CSS `<input>`寬度不超過`<div>`](https://matthung0807.blogspot.com/2017/11/css.html)  

input limit width  
```css
<style lang="scss">
@mixin input-style(
    $size: 1rem,
    $color: $black,
    $placeholder-color: $blueyGrey
) {
    font-size: $size;
    color: $color;
    caret-color: $color;

    input {
        color: $color;
        width: 100%; //<-
    }
```