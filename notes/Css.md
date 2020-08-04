## Css {docsify-ignore}

- 初始化css
```css
 * {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
html,body {
  width: 100%;
  height: 100%;
}
```

- 二维居中
	- 元素自身居中
```css
.center {
  position: absolute;
  margin: auto;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
}
```
	- 子元素居中
```css
.childCenter {
  display: flex;
  justify-content: center;
  align-items: center;
}
```

---  

