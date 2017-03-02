# 14 Must Know Dev Tools Tricks

## 使用Dom Breakpoint 找到修改屬性的Javascript
Chrome開發工具，頁面標籤，右鍵 → Break on → Attributes modifications。即可為元素添加斷點，屬性發生改變時，自動定位到頁面代碼的對應行。

## .log 的更多用法
* %s 字串
* %d 整數
* %f 浮點數
* %o Object
* %c 設定輸出樣式

## console 的更多用法
* 標示圖案及顏色改變
```js
// warning
console.warn("但黃色背景，三角驚嘆號")
// Error
console.error("紅背景，叉叉符號");
// Info
console.info("藍色驚嘆號");
```
* Dom元素 dir
不同的地方在於，log 輸出這個 DOM 的 HTML 標籤，而 dir 則會輸出這個 DOM 元素的屬性列表。
```js
const p = document.querySelector('p');
console.log(p);
console.dir(p);
```
* 清空console.log列表 clear
    * console.clear()
    * Ctrl ＋ L
* 測試 assert
```js
console.assert(1 === 1, "這句不會顯示");
console.assert(1 === 0, "這句會顯示");
console.assert(p.innerHTML.match("她"), "她沒有出現");
```
* 表格方式顯示 table
```js
console.table(dogs);
console.table(dogs, ["age"]); // 只顯示age這行
```
* 群組方式顯示 group
```js
dogs.forEach(dog => {
    console.group() // 可用groupCollapsed預設收合
    console.log(`woof i am ${dog.name}`)
    console.log(`${dog.name} is ${dog.age} years old`)
    console.groupEnd()
})
``` 
* 計次 count
對象是count輸出的內容，非全部console中的內容
* 計時 time
 time("name") 和 timeEnd("name")為起始點及結束點，name可自定義但需相同。
```js
console.time('fetching data')
fetch('https://api.github.com/users/wesbos')
 .then(data => data.json())
 .then(data => {
    console.timeEnd('fetching data')
    console.log(data)
})
```
