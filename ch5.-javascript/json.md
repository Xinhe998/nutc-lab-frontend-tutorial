# JSON

JSON（**J**ava**S**cript **O**bject **N**otation） 是個以純文字為基底去儲存和傳送簡單結構資料，  
可以透過特定的格式去儲存任何資料（字串, 數字, 陣列, 物件）。

我們可以將 JSON 資料傳到server（或從server拿取JSON資料到網頁前端），

```javascript
{
  "orderID": 12345,
  "shopperName": "John Smith",
  "shopperEmail": "johnsmith@example.com",
  "contents": [
    {
      "productID": 34,
      "productName": "SuperWidget",
      "quantity": 1
    },
    {
      "productID": 56,
      "productName": "WonderWidget",
      "quantity": 3
    }
  ],
  "orderCompleted": true
}
```

## JSON.parse\(\)

將JSON格式資料轉換為Object

```javascript
var obj = JSON.parse('{ "name":"John", "age":30, "city":"New York"}');
```

## JSON.stringify\(\)

將JavaScript Object轉換為JSON

```javascript
var obj = { name: "John", age: 30, city: "New York" };
var myJSON = JSON.stringify(obj);
```

```javascript
var arr = [ "John", "Peter", "Sally", "Jane" ];
var myJSON = JSON.stringify(arr);
```



