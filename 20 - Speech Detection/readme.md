# Day20 - Speech Detection
利用瀏覽器內建google語音api，將自己說出來的話顯示在頁面上。


## SpeechRecognition

```js
const recognition = new SpeechRecognition();
// 建造語音識別的物件
```
### SpeechRecognition.lang
取得和設定當前 SpeechRecognition 使用的語言。若沒有特別指定，預設會使用lang 的設定值，或是使用者裝置設定的語言。
### SpeechRecognition.continuous
控制每個 recognition 會傳連續的結果還是只回傳單一結果。預設為回傳單一結果 (false.)
### SpeechRecognition.interimResults
控制臨時結果是否回傳。 true 回傳，false 不回傳。臨時結果指的是所有非最終 (Final) 結果的結果。 (例如 : SpeechRecognitionResult.isFinal 特性為 false.)
### SpeechRecognition.start()
.start()方法是開啟語音識別的服務，偵測輸入的語音。

其他相關的使用方法 [點此](https://developer.mozilla.org/zh-TW/docs/Web/API/SpeechRecognition)

```js
recognition.interimResults = true;
// 返回即時語音 即SpeechRecognitionResult.isFinal 為否時的內容
```