# 熟悉 CSS

首先我們要先知道如何把CSS套用到網頁上。

1. Inline \(最不建議使用\)

   ```markup
   <div style="color: white; font-size: 20px;">...</div>
   ```

2. Embed

   ```markup
   <head>
      <style type="text/css">
         div {
            color: white;
         }
      </style>
   </head>

   <div>...</div>
   ```

3. External Link

   ```markup
   <head>
       <link rel="stylesheet" type="text/css" href="style.css">
   </head>
   ```

   > p.s.假如有多個外部連結，則越後面套入的CSS優先權越高。

在前面已經提到，CSS語法必須由一選擇器，來指定屬性樣式。

而選擇器主要有三種：

* 類型 \(Type\) 選擇器：HTML 標籤

  ```css
  h1 {
    color: red;
  }
  ```

* Class 選擇器：使用者自訂

  ```css
  .my-button {
    color: white;
  }
  ```

* ID 選擇器：使用者自訂

  ```css
  #container {
    background-color: blue;
  }
  ```

## 後代選擇器

但有時候css設定並沒有想像中這麼簡單。  
例如今天html如下這樣呈現時

```markup
<ul>
  <li>
    first
  </li>
  <li>
    second
  </li>
  <li>
    third
  </li>
</ul>
```

當想改變ul中li的字型顏色，難道要為每個li都加上class嗎？這樣豈不是太麻煩了？  
這時候CSS就可以這樣設定：

```css
ul li {
  color: red;
}
```

這樣頁面上所有在ul中的li都會套用到以上樣式。

## 子代選擇器

```markup
<div>
    <span>Blue</span>
    <p>
        <span>Black</span>
    </p>
</div>
```

CSS若使用子代選擇器，如下表示：

```css
div > span { 
  color: blue; 
}
```

  
只有div **下一層** 的span會套用樣式。因此p中的字樣並不會套用樣式。

![](../.gitbook/assets/css-child-selector.png)

若使用後代選擇器，如下表示：

```css
div span { 
  color: blue; 
}
```

則所有div下的span都會套用樣式。

## CSS Class 與 CSS ID

假若html如下這樣呈現：

```markup
<button id="first-btn">First</button>
<button id="second-btn">Second</button>
```

如果要分別更改兩個不同的button，則CSS可以這樣設定：

```css
button#first-btn {
  color: red;
}
button.second-btn {
  color: blue;
}
```

## 分組選擇器：多個元素同個CSS

承上例，如果要一次設定多個元素為同一個CSS樣式，可以這樣設定：

```css
button#first-btn ,button.second-btn {
  color: red;
}
```

## 同一元素多重Class

我們也可以在一個元素同時套用數個 class。

舉例來說，若我們有以下的 HTML，

```markup
<button class="large-btn red-btn">這是多重 Class 的例子。</button>
```

那麼CSS可以如下：

```css
.large-btn { 
  width: 150px;
  height: 50px;
  font-size:20px; 
}

.red-btn { 
  color: white; 
  background: red;
}
```

## 屬性選擇器

今天有一html如下：

```markup
<input type="text">
<input type="button" value="送出">
```

若只想更改input type是button的樣式，則CSS可以這樣設定：

```css
input[type="button"] {
  color: red;
}
```

## 偽類選擇器

偽類 \(pseudo class\) 就是在選已經存在的東西。

### 錨偽類

在支援 CSS 的瀏覽器中，連結的不同狀態都可以不同的方式顯示。

* :link  / _還沒訪問_ /
* :visited  / _已訪問_ /
* :hover  / _滑鼠移到上面_ /
* :active  / _已選定_ /

  ```css
  a:link {color: #FF0000}        
  a:visited {color: #00FF00}    
  a:hover {color: #FF00FF}    
  a:active {color: #0000FF}
  ```

### 第一個與最後一個

* :first-child
* :last-child

  ```css
  p:first-child {font-weight: bold;}
  p:last-child {font-weight: 300;}
  ```

### 第幾個：nth-child\(n\)

```css
p:nth-child(2) {color: red;}
p:nth-child(odd/even) {background: grey;}
```

### 允許鍵盤輸入的元素焦點：focus

```css
input:focus {border-color: blue;}
```



