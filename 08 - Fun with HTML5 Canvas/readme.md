# Fun with HTML5 Canvas

## Canvas
一個HTML元素，可以利用程式腳本在這個元素上繪圖（通常是用 JavaScript）

* **渲染環境(rendering context)**
一開始canvas為空白，需要先存取渲染環境在上面繪圖，然後才會顯現影像。
<canvas> 有一個method叫getContext()，透過此方法可以取得渲染環境及其繪圖函數(function)；
getContext()輸入參數只有渲染環境類型一項，像2D繪圖，就是輸入”2d”。
```JS
const canvas = document.querySelector('#draw');
const ctx = canvas.getContext('2d');
```
* **width / height**
 ```JS
canvas.width = window.innerWidth; // 設定寬
canvas.height = window.innerHeight; // 設定高
```
* **style**
```JS
ctx.strokeStyle = '#BADA55'; 
// 設定勾勒圖形時用的顏色。
ctx.lineJoin = 'round'; 
// 設定線條和線條間接合處的樣式有 round | bevel | miter 圓交、斜交、斜接。
ctx.lineCap = 'round'; 
// 設定線條結尾的樣式有 round | butt | square 圓、平、方。
ctx.lineWidth = 100 
// 設定線條寬度
```
* **繪製路徑**
```JS
beginPath() // 開始一段路徑
moveTo(x,y) // 起始點
lineTo(x,y) // 結束點
stroke() // 實際繪出通過moveTo及lineTo的路徑，預設是黑色
```
## Javascript
* innerWidth / innerHeight
```JS
window.innerWidth 
```
Width (in pixels) of the browser window viewport
## Other
* **彩虹漸變**
H 色相，取值為 0~360。
S 飽和度，可以理解為參染進去的灰色值，取值為0~1
L 亮度，取值也是 0~1，或者百分比。
```JS
let hue = 0;
ctx.strokeStyle = `hsl(${ hue }, 100%, 50%)`;   
if(hue >= 360) hue = 0;
hue++;
```
* **Flag**
需要標記變數來紀錄滑鼠是否為按下的狀態
紀錄線的寬度是否再1~100間
* **[a,b] = [A,B]**
```JS
a=A;
b=B;

[a,b] = [A,B]
```