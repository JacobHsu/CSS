title: SCSS
---

src/theme/main.scss  
```css
// grid-flex
@mixin grid-flex($direction:row, $justify:center, $align:center, $wrap:nowrap) {
  display: flex;
  flex-flow: $direction;
  flex-wrap: $wrap;
  justify-content: $justify;
  align-items: $align;
}
```

src/views/components
```js
<style lang="scss" module>
.header {
    @include grid-flex;
}        
```

SCSS 是 Sass 3 引入新的语法，其语法完全兼容 CSS3，并且继承了 Sass 的强大功能  
[sass mixin](http://www.ruanyifeng.com/blog/2012/06/sass.html)