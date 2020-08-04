## Html {docsify-ignore}

- `<head>`写法
```html
<head>
	<!-- <meta>标签提供关于此页面的元信息 -->
	<meta charset="utf-8" />
	<meta name="viewport" content="width=device-width, initial-scale=1" />
	<meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1" />
	<meta name="theme-color" content="<颜色值>" />
	<meta name="description" content="<网页描述>" />
	<meta name="keywords" content="<关键词>" />
	<!-- 引入外部文件 -->
	<link rel="shortcut icon" href="<icon链接>" />
	<link rel="stylesheet" href="<css链接>" />
	<script src="<js链接>"></script>
	<title>页面标题</title>
</head>
```

- 关于`<span>`的坑
	- `<span>`标签换行排版会导致元素之间存在空隙，所以尽可能将`<span>`标签写在同一行，其他行内元素亦然。如果必须将`<span>`等行内元素写在不同行，则可通过设置父级元素`font-size: 0`,再将子元素的字体大小调整回来，可解决此问题。此问题是由于浏览器会将连续的多个空格或换行渲染成一个空格所致。

---
