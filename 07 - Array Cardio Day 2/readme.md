# Array Cardio Day 2

## Array method
method of Array object that accept a callback function as its parameter
* **some() :** 任一可以通過function即true
* **every() :** 所有通過function即true
* **find() :** 回傳array中找到的第一個值，否則回傳undefine
* **findIndex() :** 回傳array中找到的第一個值的位置，否則回傳-1
* **slice() :** 複製指定段落的Array
```js
var fruits = ['Banana', 'Orange', 'Lemon', 'Apple', 'Mango'];
var citrus = fruits.slice(1, 3);
// fruits contains ['Banana', 'Orange', 'Lemon', 'Apple', 'Mango']
// citrus contains ['Orange','Lemon']
```
* **splice() :** 移除Array中的指定位置
```js
var myFish = ['angel', 'clown', 'mandarin', 'sturgeon'];
var removed = myFish.splice(2, 0, 'drum');
// myFish is ["angel", "clown", "drum", "mandarin", "sturgeon"] 
// removed is [], no elements removed
```
