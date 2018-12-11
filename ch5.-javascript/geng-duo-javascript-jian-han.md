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



