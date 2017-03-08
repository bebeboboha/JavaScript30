# Custom HTML5 Video Player

## Conditional (ternary) Operator
```js
if(video.paused){
    video.play();
}else{
    video.pause();
}
```
```js
const method = video.paused ? 'play':'pause';
video[method]()
```
```js
video[video.paused ? 'play':'pause']();
```

## parseFloat(string)
將字串轉變為數字

## HTML Audio/Video DOM Property
```js
audio|video.currentTime // 正在播放的時間點
audio|video.duration // 影片的總播放時間
```

## Dom事件

timeupdate 監聽播放時間有改變
```js
video.addEventListener('timeupdate',handleProgress)
```

## offsetWidth
取得div的寬度，包含padding及border

