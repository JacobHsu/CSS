title: Footer
---

[利用 CSS View Height (vh) 製作置底 Footer](https://myapollo.com.tw/zh-tw/css-viewport-height/)

```css
body {
  margin: 0;
}

#head {
  background-color: #dfdfdf;
  height: 2rem;
}

#content {
  min-height: calc(100vh - 4rem);
  background-color: #676767;
}

#footer {
  background-color: #dfdfdf;
  height: 2rem;
}
```

## References

[fun-viewport-units](https://css-tricks.com/fun-viewport-units/)