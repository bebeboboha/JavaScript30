# Da19 - webcam fun

## .getUserMedia()
在使用getUserMedia()的api取得視訊鏡頭影像，須在安全連接的模式下才可以。
而安全模式主要有，HTTPS、localhost、wss、file、chrome-extension等...
其餘安全模式的內容，可以參考[這裡](https://www.chromium.org/Home/chromium-security/prefer-secure-origins-for-powerful-new-features)


## package.json
在這次的例子中，選擇用localhost來達到安全連接。

```js
{
  "name": "gum",
  "version": "1.0.0",
  "description": "",
  "main": "scripts.js",
  "scripts": {
    "start" : "browser-sync start --server --files '*.css, *.html, *.js'"
  },
  "author": "",
  "license": "ISC",
  "devDependencies": {
    "browser-sync": "^2.12.5"
  }
}
```
在package.json，會找到browser-sync，可透過npm install安裝後，創建一個本地的localhost，執行npm start就可開啟localhost，並且在文件修改時會自動更新。

```shell
$ npm install
$ npm start
```

## navigator.mediaDevices.getUserMedia()

提示用戶允許使用視頻或音頻輸入設備，例如相機、螢幕、或麥克風等。如果使用者許可，就返回Promise。

**用法：**
```js
navigator.mediaDevices.getUserMedia(constraints)
.then(function(mediaStream) { ... })
.catch(function(error) { ... })
```

```js
function getVideo() {
  navigator.mediaDevices.getUserMedia({ video: true, audio: false })
    .then(localMediaStream => {
      console.log(localMediaStream);
      video.src = window.URL.createObjectURL(localMediaStream);
      video.play();
    })
    .catch(err => {
      console.error(`OH NO!!!`, err);
    });
}

```

## URL.createObjectURL()

創建一個DomString，其中包含URL。這URL表示指定的File物件或Blob物件。

**用法：**
```js
objectURL = URL.createObjectURL(blob);
```

```js
video.src = window.URL.createObjectURL(localMediaStream);
```