# Ajax

在JavaScript中的「互動」除了是使用者跟瀏覽器的互動以外，別忘了還有 Client 端跟 Server 端的互動，也就是必須要學會從瀏覽器用 JavaScript 跟後端 Server 拿資料，否則我們的網頁資料都只會是寫死的。

要讓網頁的資料可以持續更新改變，就必須從 Server 那邊拿資料回來，接著在前端處理後顯示。

## 什麼是API？

API是Application Programming Interface的縮寫，中文為應用程式介面，也就是提供一個**接口**，讓程式可以去取得需要的資料。

![](../.gitbook/assets/image%20%2814%29.png)

## 如何測試API：Postman

請先下載Postman：[https://www.getpostman.com/apps](https://www.getpostman.com/apps)

![](../.gitbook/assets/image%20%285%29.png)

## 如何串接API：AJAX

要在瀏覽器上面發送 Request，必須應用到一種技術叫做 Ajax，全名是「Asynchronous JavaScript and XML」，重點在於`Asynchronous`這個單字，非同步。

```javascript
$.ajax({
    url: '/sendData',
    data: $('#form1').serialize(),
    type:"POST",
    dataType:'text',

    success: function(msg){
        alert(msg);
    },

     error:function(xhr, ajaxOptions, thrownError){ 
        alert(xhr.status); 
        alert(thrownError); 
     }
});
```

jQuery AJAX當中的參數：

* **dataType：**預期Server傳回的資料類型，**如果沒指定，jQuery會根據HTTP MIME Type自動選擇以responseXML或responseText傳入你的success callback**。可選的資料類型有：                   xml：傳回可用jQuery處理的XML                   html：傳回HTML，包含jQuery會自動幫你處理的script tags。                   script：傳回可執行的JavaScript。\(script不會被自動cache，除非cache設為true\)                   json：傳回JSON                   jsonp：在URL加上?callback=?參數，並在Server端配合送回此jsonp callback。                   text：傳回純文字字串。



* **type：**請求方式，POST/GET。

\*\*\*\*

* **success：**請求成功時執行函式。                 `function (data, textStatus) {        // data 可以是 xmlDoc, jsonObj, html, text, 但還是要參考datatype  }` 

\*\*\*\*

* **error：**請求失敗時執行函式。            `function (xhr, ajaxOptions, thrownError) {            //通常ajaxOptions或thrownError只有一個有值 }` 

其他可能比較會用的參數：

* **complete：**請求完成時執行的函式\(不論結果是success或error\)。                  `function (XMLHttpRequest, textStatus) {          // the options for this ajax request  }`



* **beforeSend：**發送請求之前可在此修改XMLHttpRequest物件，如添加header等，你可以在此函式中return flase取消Ajax request。                     `function (XMLHttpRequest) {           // the options for this ajax request  }`



