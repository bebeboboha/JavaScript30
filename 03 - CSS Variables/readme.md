# Day 3 - Playing with CSS Variables and JS

## HTML

* **input type :** https://www.w3schools.com/tags/att_input_type.asp 
range、color

## CSS

* **:root :** 全域用來搭配CSS變數
* **var(--xxx)：** CSS 變數（CSS Variables） like $ in jquery
* **img filter :** https://developer.mozilla.org/zh-CN/docs/Web/CSS/filter

## JavaScript

可按照指定的周期（以毫秒來記）來設定函數會計算表達式。
```js
	setInterval(code,millisec[,"lang"])
```

## Clock

* **addEventListener :** 
	* **DOM事件 :** http://www.runoob.com/jsref/dom-obj-event.html
* **dataset :** html自定義屬性取值
* **改變CSS值 :** 
```js
	document.documentElement //文檔根元素
	document.documentElement.style.setProperty('--base', '#fff');
```
