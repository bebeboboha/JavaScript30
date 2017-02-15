# Day 1 - JavaScript Drum Kit

## html tag

1. **<kbd>** : keyboard input 
2. **<audio>** : sound MP3、Wav、Ogg
3. data-key : 
    1. **data-* :**
        1. 用於存儲頁面的自定義數據 
        2. 賦予我們在所有html元素上遷入自定義data屬性的能力
        3. 數據能被JavaScript應用
    2. **data-* 屬性包括兩部分：**
        1. 屬性名不應該包含任何大寫字母，並且再前綴 "data-" 之後必須有至少一個字符
        2. 屬性值可以是任意字符串


## JavaScript

1. .querySelectorAll('....') : Get all elements in the document with class="..."
2. .querySelector('....') : Get the first element in the document with class="..."
3. .play()、.pause() : Play audio
4. .currentTime() : 播放時間
5. classList.add() = addClass() // in jquery

## ES6
1. https://github.com/addyosmani/es6-equivalents-in-es5
2. let : 使用 let 宣告以區塊為活動範圍的變數。
    1. let 禁止在宣告變數之前就使用它。
    2. let 禁止在同一活動範圍中再次宣告相同名稱的變數。
3. const : 內容僅能在定義時設定初值，之後不允許再改變。這就是常數了。
    1.const 的語法限制和 let 相同，不允許重複宣告、不允許宣告前使用。
4. var : 僅限活動範圍內可用，外部看不到。
    1.沒有用 var 或在函數外宣告的變數，就屬於全域範圍了。
