# JavaScript事件

JavaScript 是一個事件驅動 \(Event-driven\) 的程式語言，當瀏覽器載入網頁開始讀取後，會馬上讀取 JavaScript 事件相關的程式碼，但是必須等到「事件」被觸發\(如使用者點擊、按下鍵盤等\)後，才會再進行對應程式的執行。

## 常用事件

click – 滑鼠點擊物件時  
change – 內容改變時  
focus – 文字區域被點擊時  
load – 網頁或圖片下載完成時  
mousedown – 按下滑鼠按鍵時  
mouseover – 滑鼠游標移過某個物件時  
submit – 表單送出時  
unload – 離開網頁時  
keypress – 某個按鍵被敲擊時

## 事件監聽

我們可以透過 `addEventListener()` 這個方法來綁定事件：

```javascript
document.getElementById("box").addEventListener('click', function () {
  alert('this is a box');
});
```

## on-event（HTML屬性）

除了上述方法可以綁定事件外，我們也可以利用DOM API 提供的「on-event 處理器」\(on-event handler\) 來處理事件。

```markup
<button id="btn" onclick="console.log('HI');">Click</button>
```

## on-event 處理器 \(非 HTML 屬性\)

像是 `window` 或 `document` 此類沒有實體元素的情況，我們一樣可以利用 on-event 處理器。

```javascript
window.onload = function(){
  document.write("Hello world!");
};
```

實體物件也可以利用這樣的方式：

```javascript
document.getElementById("box").onclick = function(){
  console.log("click");
};
```

若想解除事件的話，則重新指定 `on-event hendler` 為 `null` 即可：

```javascript
document.getElementById("box").onclick = null;
```

