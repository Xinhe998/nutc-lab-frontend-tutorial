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

