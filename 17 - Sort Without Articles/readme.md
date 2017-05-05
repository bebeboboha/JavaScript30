# Sort Without Articles
## .trim()
String.trim()方法用來去除字串前後的空白<br>此方法並不會改變原來的字串，而是傳回一個新的字串。


```jsx=
<script type="text/javascript">
 var str="    我是   字串嗨嗨   ";
 console.log(str.trim());
</script>
```
會輸出
```js
我是   字串嗨嗨
```

## .join()
join()方法用來把Array中的所有元素放入一個字串中。<br>元素是通過指定的分隔符號進行分隔。
```jsx=
<script type="text/javascript">

var arr = new Array(3)
arr[0] = "George"
arr[1] = "John"
arr[2] = "Thomas"

console.log(arr.join())

</script>
```
會輸出
```js
George,John,Thomas
```
而如果使用.join('')，則會輸出
```js
GeorgeJohnThomas
```