# JavaScript的變數＆運算子

## JavaScript變數

JavaScript 變數名稱有區分英文大小寫，所以item, Item, ITEM會是不同變數。

但變數名稱不能為保留字如下：

|  |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
| break | case | catch | continue | debugger |
| default | delete | do | else | false |
| finally | for | function | if | in |
| instanceof | new | null | return | switch |
| this | throw | true | try | typeof |
| var | void | while | with |  |

變數名稱一定要使用英文字母或「 \_ 」開頭，不可使用數字或其他符號，且變數中也不可有「 . 」。

### 變數宣告

JavaScript 是動態定型語言，所以變數宣告都不需要指定型態，在JacaScript中大部分會使用var來宣告變數。

```javascript
var a = 10;
a = "hello";
console.log(a);
```

因為使用var定義的變數本身不帶任何型態資訊，所以同一個變數可以指定不同型態的值！

> 但像是Java、C/C++等此類程式語言都必須先定義該變數的型態，稱之為靜態定型語言，好處就是在編譯時，可以由編譯器確認變數與實際的值是否符合，能夠在編譯時就檢查出型態指定不符的錯誤。

而當宣告了變數卻沒有給定值，或是根本沒有宣告此變數的時候，其對應的值都會呈現undefined。

```javascript
var b;
console.log(b);  //undefined
```

我們也可以利用 if statement 檢查變數是否存在：

```javascript
if (b) {
    console.log("變數存在", b);
} else {
    console.log("變數不存在", b);
}
```

而在ES6之後，出現了let和const這兩種定義變數的方式，主要是為了彌補 var 的一些缺陷而新設計出來的，那他們到底有什麼差別呢？

* 使用let宣告的變數，**只能在區域中做使用**，例如: 陳述句\(if、else\)、迴圈\(for\)！！（非常重要）

  ```javascript
  for (let i = 0; i < 10; i += 1) {
    console.log(i);
  }
  console.log(i); // ReferenceError: i is not defined
  ```

  有了let後，我們可以讓變數不會在其他地方被不小心使用或更改到。  

* 使用const宣告了變數及其值後，就不能再修改了。

  ```javascript
  const num = 10;
  num = 100;  //Uncaught TypeError: Assignment to constant variable.
  ```

## JavaScript資料型態

JavaScript 有很多種資料型態：

* 布林\(Boolean\)
* 數值\(Number\)
* 字串\(String\)
* 陣列\(Array\)
* 物件\(Object\)
* 空值\(null\)
* 未定義\(undefined\)
* 函式\(Function\)
* 符號\(Symbol\)

## JavaScript的運算子（Operator）

### 算術運算子

| 運算子（Operator） | 描述（Description） |
| :--- | :--- |
| + | 加 |
| - | 減 |
| \* | 乘 |
| / | 除 |
| % | 取餘數 |
| ++ | 遞增 |
| -- | 遞減 |

需要注意的是遞增（減）的運算可以放在變數前後，但兩者的差別是遞增（減）符號放在變數前，變數的值會立刻加或減一，放在變數後則會是在執行運算式後才改變。

```javascript
var a = 10, b, c;
b = ++a;
c = a++;
console.log(b);  //12
console.log(c);  //10
```

### 指定運算子

| 運算子（Operator） | 描述（Description） |
| :--- | :--- |
| = | 指定敘述，x = y也就是將y值指定到x上 |
| += | x +=y 等同於 x = x + y |
| -= | x -=y 等同於 x = x - y |
| \*= | x \*=y 等同於 x = x \* y |
| /= | x /=y 等同於 x = x / y |
| %= | x %=y 等同於 x = x % y |

### 比較運算子

| 運算子（Operator） | 描述（Description） |
| :--- | :--- |
| == | 等於 |
| === | **值和型態都等於** |
| != | 不等於 |
| !== | **值或型態不等於** |
| &gt; | 大於 |
| &gt;= | 大於等於 |
| &lt; | 小於 |
| &lt;= | 小於等於 |

### 邏輯運算子

| 運算子（Operator） | 描述（Description） |
| :--- | :--- |
| && | and |
| \|\| | or |
| ! | not |

### 三元運算子

**語法**

```text
test ? expression1 : expression2
```

**範例**

```javascript
var x = 10;
(x < 5) ? console.log("x < 5") : console.log("x > 5");   //x > 5
```

### typeof 運算子

印出變數的型態。

```javascript
typeof "Xinhe";  //string
typeof 10; //number
typeof true; //boolean
typeof [1,2,3,4];  //object
typeof function(){};  //function
```

## 資料型態轉換

### 強制轉型

因為運算式需要運算元是

| 運算式 | 處理方式 |
| :--- | :--- |
| number和string相加 | number會強制轉換成string |
| boolean和string相加 | boolean會強制轉換成string |
| boolean和number相加 | boolean會強制轉換成number（true為1，false為0） |

### 轉型函數

| 函數 | 說明 |
| :--- | :--- |
| parseInt\(\) | 將字串開頭是數值的轉換為整數 |
| parseFloat\(\) | 將字串開頭是浮點數的轉換為浮點數 |

要注意的是以上兩個方法都只接受開頭為整數或浮點數的字串做轉型！若要轉型的字串格式不符，則轉型結果會是NaN（不是數值的代表）。

```javascript
var a = "page 10";
console.log(parseInt(a));  //NaN
```



