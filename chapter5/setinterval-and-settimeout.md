# setInterval\(\) & setTimeout\(\)

## setInterval\(\)

指定一段程式碼定時在多少毫秒\(ms\)執行一次，並回傳此定時器的編號。

```javascript
//1秒鐘印出一次目前時間
setInterval(function(){
    console.log(new Date());
}, 1000);
```

可以透過 `clearInterval()` 取消程式碼的執行。

```javascript
//1秒鐘印出一次目前時間，印出10次後就停止
var count = 0;
setInterval(function(){
    if(count < 10){
        console.log(new Date());
        count++;
    } else {
        clearInterval();
    }
}, 1000)
```

## setTimeout\(\)

指定一段程式碼定時延遲多少毫秒\(ms\)後執行，並回傳此定時器的編號。

```javascript
//3秒鐘後印出時間
setTimeout(function(){
    console.log(new Date());
}, 3000);
```

可以透過 `clearTimeout()` 取消程式碼的執行。

範例參考：[https://www.w3schools.com/jsref/tryit.asp?filename=tryjsref\_win\_cleartimeout](https://www.w3schools.com/jsref/tryit.asp?filename=tryjsref_win_cleartimeout)

