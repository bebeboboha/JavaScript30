# Mouse Move Shadow
## contenteditable
```js
<h1 contenteditable="true">這是一段可以編輯的段落</h1>
```

## ES6
```jsx
const width = hero.offsetWidth;
const height = hero.offsetHeight;
```
在ES6可以編寫成
```jsx
const { offsetWidth: width, offsetHeight: height } = hero;
```

## this vs event.target
this 回傳你正在監聽的元素
target 回傳哪個DOM元素觸發該事件


```jsx
<div class="hero">
    <h1 contenteditable>🔥WOAH!</h1>
</div>
```
```js
hero.addEventListener('mousemove', shadow);
function shadow(e){
 console.log(this,e.target)
}
```
所以在例子中，當滑鼠滑經過h1所在的區塊時，this會回傳
```js
<div class="hero">
    <h1 contenteditable>🔥WOAH!</h1>
</div>
```
而target則會回傳
```js
<h1 contenteditable>🔥WOAH!</h1>
```