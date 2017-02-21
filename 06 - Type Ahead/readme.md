# Ajax Type Ahead

## Fetch
HTML5的API
```js
fetch('http://abc.com/', {method: 'get'})
.then(function(response) {
    // 直接轉成JSON格式
    return response.json()
}).catch(function(err) {
    // Error :(
})
```

## Spread syntax
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Spread_operator
```js
// 將arr2中的所有元素添加到arr1中
// ES5
var arr1 = [0, 1, 2];
var arr2 = [3, 4, 5];
Array.prototype.push.apply(arr1, arr2);
// ES6
var arr1 = [0, 1, 2];
var arr2 = [3, 4, 5];
arr1.push(...arr2);
```
