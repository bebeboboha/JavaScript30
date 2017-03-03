# Hold Shift to Check Multiple Checkboxes

## 找到checkbox
```js
input[type="checkbox"]
```

## 監聽按住shift鍵
```js
event.shiftKey
```

## Flag使用技巧
不要單單設定true、false
可使用反面
```js
inBetween = !inBetween;
```