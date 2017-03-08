# Key Sequence Detection

## 滿足長度後新增的內容，移除最前面的 splice
```js
const pressed = [];
const secretCode = 'peggy';
pressed.splice(-secretCode.length-1,pressed.length-secretCode.length);

// [p,e,g,g,y] 
// 輸入p
// [e,g,g,y,p] 
```

## 增加獨角獸 script
從Cornify.com加載js文件。使用 cornify_add() 時，會再頁面中新增p，並再DOM中插入一個圖案。
```js
<script type="text/javascript" src="http://www.cornify.com/js/cornify.js"></script>
```

## 判斷暗號 join + includes
將pressed中的內容拆出顯示，與secretCode一致。
```js
pressed.join('').includes(secretCode)
```
