# 更多JavaScript內建函數

## String

### HTML 標籤格式排版方法

| Function | Description |
| :--- | :--- |
| anchor\(name\) | 傳回&lt;a name="name"&gt;string&lt;/a&gt; |
| bold\(\) | 傳回&lt;b&gt;string&lt;/b&gt; |
| italics\(\) | 傳回&lt;i&gt;string&lt;/i&gt; |
| link\(url\) | 傳回&lt;a href="url"&gt;string&lt;/a&gt; |

```javascript
var str = "hello";
console.log(str.anchor("myStr"));   //<a name="myStr">hello</a>
console.log(str.bold("myStr"));   //<b>hello</b>
console.log(str.italics("myStr"));   //<i>hello</i>
console.log(str.link("#"));   //<a href="#">hello</a>
```

### 字串長度＆大小寫

| Function | Description |
| :--- | :--- |
| length | 取得字串長度 |
| toLowerCase\(\) | 把字串轉為全部小寫 |
| toUpperCase\(\) | 把字串轉為全部大寫 |

### 取得字串指定字元

| Function | Description |
| :--- | :--- |
| charAt\(index\) | 取得字串中index位置的字元 |
| charCodeAt\(index\) | 取得字串中index位置的字元的Unicode |

### 搜尋字串

| Function | Description |
| :--- | :--- |
| indexOf\(string, index\) | 搜尋string在指定字串中的索引位置，若沒有找到則回傳-1 |
| lastIndexOf\(string\) | 搜尋string在指定字串中的索引位置，但是從尾反方向搜尋 |
| match\(string\) | 如同indexOf\(\)，不過回傳的是找到的字串，沒找到則回傳null |
| search\(string\) | 與indexOf\(\)功能相似 |

![match\(\) &#x7D50;&#x679C;&#x7BC4;&#x4F8B;](../.gitbook/assets/image%20%288%29.png)

### 取代、分割、取出字串

| Function | Description |
| :--- | :--- |
| replace\(string1, string2\) | 將字串中找到的string1取代為string2 |
| split\(string\) | 利用參數string將指定字串分割並傳回Array |
| substr\(index, length\) | 從index開始取出length個字元 |
| substring\(index1, index2\) | 取出index1到index2中間的字串 |
| concat\(string\) | 將string參數新增到指定字串後 |

![split\(\) &#x7D50;&#x679C;&#x7BC4;&#x4F8B;](../.gitbook/assets/image%20%282%29.png)

```javascript
str3 = str1.concat(str2);
```

以上的範例相當於 `str3 = str1 + str2`

## Array

### 新增一維陣列

```javascript
var user = new Array(3);
user[0] = "Cindy";
user[1] = "John";
user[2] = "Monkey";
```

等同於：

```javascript
var user = new Array("Cindy", "John", "Monkey");
```

### 新增二維/多維陣列

```javascript
var user = new Array(3);
for(var i = 0; i < 3; i++){
    user[i] = new Array(2);
}
user[0][0] = "Cindy";
user[0][1] = "1310788088";
user[1][0] = "John";
user[1][1] = "1310788087";
```

意思是先建立有3個元素的陣列user\[\]，再利用for迴圈分別建立有2個元素的陣列，即變成5\*2的二維陣列。

### 常見方法

| Function | Description |
| :--- | :--- |
| length | 取得陣列元素數量，即陣列的長度 |
| join\(\) | 將陣列的元素使用字串來顯示，並使用,逗點分隔 |
| sort\(\) | 將陣列元素進行排序 |
| concat\(array\) | 將參數中的array合併到指定陣列中 |

## Date

建立物件為系統的日期和時間：

```javascript
var today = new Date();
```

建立了上述的Date物件後，我們就可以使用這些方法來取得時間日期資料：

| Function | Description |
| :--- | :--- |
| getDate\(\) | 傳回日期值1-31 |
| getDay\(\) | 傳回星期值0-6（星期日到星期六） |
| getMonth\(\) | 傳回月份值0-11 |
| getFullYear\(\) | 傳回完整年份 |
| getYear\(\) | 傳回年份，西元1900-1999之間傳回後兩碼，否則傳回完整年份 |
| getHours\(\) | 傳回小時值0-23 |
| getMinutes\(\) | 傳回分鐘值0-59 |
| getSeconds\(\) | 傳回秒數值0-59 |
| getMillseconds\(\) | 傳回毫秒值0-999 |

當然也可以設置時間日期：

| Function | Description |
| :--- | :--- |
| setDate\(\) | 設定日期值1-31 |
| setMonth\(\) | 設定月份值0-11 |
| setFullYear\(\) | 設定完整年份 |
| setYear\(\) | 設定年份，西元1900-1999之間傳回後兩碼，否則傳回完整年份 |
| setHours\(\) | 設定小時值0-23 |
| setMinutes\(\) | 設定分鐘值0-59 |
| setSeconds\(\) | 設定秒數值0-59 |
| setMillseconds\(\) | 設定毫秒值0-999 |

## Math

### 常數

| 常數 | 說明 |
| :--- | :--- |
| PI | 圓周率：3.141592653589793 |
| E | 自然數：2.718281828459045 |

### 亂數、最大和最小值

| Function | Description |
| :--- | :--- |
| max\(val1, val2\) | 取得兩個參數中的最大值 |
| min\(val1, val2\) | 取得兩個參數中的最小值 |
| random\(\) | 傳回亂數值 |
| round\(value\) | 將參數四捨五入 |

### 數學方法

| Function | Description |
| :--- | :--- |
| abs\(\) | 取得絕對值 |
| ceil\(\) | 傳回大於或等於參數的最小整數（天花板值） |
| floor\(\) | 傳回小於或等於參數的最大整數（地板值） |
| pow\(\) | 次方 |
| sqrt\(\) | 平方根 |

其中要注意的是random\(\)方法只會產出0-1之間的數字（不包含0 和1），  
所以假設要取得1-10之間的整數，則要將random\(\)乘以10後加1，並取地板值。

```javascript
var num = Math.floor((Math.random * 10) + 1);
```



