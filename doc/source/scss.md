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


# checked

[Working with '+', checked and Sass](https://codepen.io/manumorante/pen/NgqVZa)[CSS Radio Buttons and Checkboxes: Custom icon](https://codepen.io/JacobHsu/pen/YoVjVm)  
[fontawesome 5 font-family not work](https://stackoverflow.com/questions/47788847/fontawesome-5-font-family-not-work)
[CSS 偽元素 ( before 與 after )](https://www.oxxostudio.tw/articles/201706/pseudo-element-1.html)
[<i class="fas fa-check"></i>](https://fontawesome.com/icons/check?style=solid)

vue
```html
<div :class="[$style.select__radio]" v-for="(opt, index) in opts"
    :key="index">
    <label>  
      <i class="fas fa-university"></i> 
      <input name="radio-group" type="radio" v-model="optsSelected"  :value="opt.value"> 
      <span v-text="opt.text"></span>
    </label>
</div>
```

```scss
.select {
  &__radio {
    input {
      opacity: 0;
    }
    input:checked {
      + span:after {
        content: "\f00c";
        font-family: 'Font Awesome\ 5 Free';
        color: green;
        font-weight: 900;
      }
    }
  }
```

## mixin

[@mixin and @include](https://sass-lang.com/documentation/at-rules/mixin)

```css
@mixin reset-list {
  margin: 0;
  padding: 0;
  list-style: none;
}

@mixin horizontal-list {
  @include reset-list;

  li {
    display: inline-block;
    margin: {
      left: -2px;
      right: 2em;
    }
  }
}

nav ul {
  @include horizontal-list;
}
```
