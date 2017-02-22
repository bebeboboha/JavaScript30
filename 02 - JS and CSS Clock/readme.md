# Day 2 - JS and CSS Clock

## CSS

* **transform-origin :** Set a rotated element's base placement

## JavaScript

* **setInterval(code,millisec[,"lang"]) :** 可按照指定的周期（以毫秒來記）來設定函數會計算表達式。

## Clock

```js
const secondsDegrees = ((seconds / 60) * 360 + 90)
// +90 為當初預設CSS
```
```js
const minsDegrees = ((mins / 60) * 360) + ((seconds / 60) * 6) + 90;
// seconds/60*6 為秒針影響分針的些微差距
```
```js
const hourDegrees = ((hour / 12) * 360) + ((mins / 60) * 30) + 90;
// mins/90*30 為分針影響時針的些微差距
```
