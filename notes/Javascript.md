## Javascript {docsify-ignore}

### 原生JS

- 定义函数
```js
function MyFunction() {
  //code
  }
```

- 显示文本
```js
window.alert();
document.write();
.innerHTML="";
console.log();
```

- 判断设备是否为电脑或手机
```js
!function() {
  	var width = window.outerWidth;
  	if (width > 900) { //根据设备宽度来判断
		var head = document.head;  //响应式添加css和js
		var css = document.createElement("link");
		var js = document.createElement("script";
    	css.setAttribute("rel","stylesheet");
    	css.setAttribute("href","/static/css/index.css");
		js.setAttribute("src","/static/js/index.js");
		head.appendChild(css);
		head.appendChild(js);
	}
}()
```

---

### Jquery

- 入口函数
```js
//在文档没有完全加载之前就运行函数，操作可能失败。
$(document).ready(function(){
  //code
  });
```

- 自定义jQuery的简写方式，替换常规的"$"符号，避免某些时候的命名冲突。
```js
var jq = jQuery.noConflict();
```

- `$("#one")`只会选择第一个id为one的元素，`$("[id=one]")`则可以选择所有id为one的元素，class等属性并不存在此限制。

---
