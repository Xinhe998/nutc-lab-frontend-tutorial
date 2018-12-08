# JavaScript的函數＆物件

## JavaScript的函數

在JavaScript函數是把共用的一些程式碼獨立成為程式區塊，再用呼叫的方式來使用，而且能夠傳入參數和傳回執行結果。在JavaScript中分為內建函數及使用者自定義函數。

### 內建函數

在前面中其實我們不知不覺中已經使用過JavaScript的內建函數了，像是parseInt\(\)、getElementById\(\)等等，在後面還會再跟大家介紹更多內建函數。

### 自訂函數

JavaScript函數是由function關鍵字、函數名與程式碼所組成：

```javascript
function functionName(){
    console.log("hello");
}
```

呼叫函數時則如下：

```javascript
functionName();
```

但以上是沒有傳入參數的函數，在JavaScript中允許函數傳入多個參數（中間要用逗點,隔開），在呼叫時只需要傳入不同參數值就可產生不同執行結果。

```javascript
function functionName(num1, num2){
    console.log(num1 += num2);
}
functionName(1,2);
```

> 把預期的功能抽象化為一層一層相同的 function 串起來，讓彼此的差異只在於傳入的 value。  
>                                                                                                  ⏤⏤By 簡訊設計Chiunhau You

JavaScript函數還可以傳回執行結果，如下：

```javascript
function functionName(num1, num2){
    return (num1 += num2);
}
var result = functionName(1,2);
console.log(result);  //3
```

以上範例中若沒有return結果值的話，result會無法得到此函數的結果。

```javascript
function functionName(num1, num2){
    num1 += num2;
}
var result = functionName(1,2);
console.log(result);  //undefined
```



