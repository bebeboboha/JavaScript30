# Day18 - Adding Up Times with Reduce
## .querySelectorAll()
可使用屬性來尋找
```js
document.querySelectorAll('[data-time]')
//包含 data-time attribut
```

透過querySelectorAll尋找到的是NodeList非Array，所以當要使用到Array的Function時，需轉變為Array
```js
Array.from(document.querySelectorAll('[data-time]'))
```
## 解構賦值
解構賦值是一種 JavaScript 運算式，可以將陣列或物件中的資料取出成獨立變數。
```js
var a, b, rest;
[a, b] = [10, 20];
console.log(a); // 10
console.log(b); // 20

[a, b, ...rest] = [10, 20, 30, 40, 50];
console.log(a); // 10
console.log(b); // 20
console.log(rest); // [30, 40, 50]

({a, b} = {a: 10, b: 20});
console.log(a); // 10
console.log(b); // 20
```

## .split()
split出來的內容為string所以在要處理資料時需透過parseFloat轉變為數字
```js
time.split(":").map(parseFloat)
```

## Math.floor()取整數
Math.floor()方法會傳回小於或等於給定數值(輸入參數)的最大整數。
```js
Math.floor( 45.95); //  45
Math.floor( 45.05); //  45
Math.floor(  4   ); //   4
Math.floor(-45.05); // -46 
Math.floor(-45.95); // -46
```