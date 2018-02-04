jQuery 最基本的中心思想就是以「選取 DOM 元素為開始」，接著就是對它們作一些事。


## 選擇元素

只要記得在CSS學過的選擇器，jQuery就超級簡單哦 ^_^

```
  $(selectors);
```

例如：
```
  $("#menu");
  $("ul li");
```
## jQuery事件

1. $(document).ready() 

有些時候，我們必須在網頁下載完成之後立即執行一些程式，可能是想要馬上顯示一些歡迎訊息等等。
```
  $(document).ready(function() {  
    alert('您好，歡迎光臨');  
  }); 
```

2. click() 滑鼠點擊物件時

```
  $("button").ready(function() {  
    alert('您好');  
  }); 
```

3. dblclick() 滑鼠連點二下物件時
4. mouseenter() 滑鼠進入時
5. mouseleave() 滑鼠移開時
6. mousedown()  按下滑鼠時
7. mouseup()  按下滑鼠並放開時
8. hover()
9. focus()  
10. change()  元素內容改變時，e.g.input中輸入了文字。

## 常用jQuery方法

1. show() / hide()

將指定元素顯示/消失。

```
  $("#A").show();
  $("#B").hide();
```

2. css()

加入或改變 css style的內容。

```
  $("#Demo").css("color", "red");
```

若要改變多項css style則必須使用以下的方法。

```
  $("#Demo").css({
    "color":"block",
    "text-align":"center"
  });
```

3. addClass() / removeClass()

將指定元素的Html加入/移除class。

```
  $("div").addClass("important");
```

4. append()

在指定元素之後插入元素

```
  $("p").append("Some appended text.");
  $("p").append("<a href="#">hello</a>");
```

5. attr()

此方法乃是 jQuery 對於 Html Tag 屬性的操作。

例如有個Html為：

```
  <a href="/test" title="測試">測試</a>
```

則可以使用jQuery拿到與更改其屬性值。

```
  $("a").attr("href");   //拿到"/test"
  $("a").attr("href","/admin") //更改此元素的href為"/admin"
```

6. 遍歷

| 函數 | 說明 | 
| -------- | -------- | 
| parent()     | 得到指定元素的上一層父元素     | 
| children()     | 得到指定元素的**下一層**子元素     | 
| next()     | 得到指定元素的同層級的下一元素     | 
| first()     | 得到的所有元素中的第一個元素     | 
| last()     | 得到的所有元素中的最後一個元素     | 
| eq(n)     | 得到的所有元素中的第n個元素     | 
| find()     | 得到指定元素的**所有**子元素     | 

7. val()

用來取得或改變元素的值。
```
 $("input").val()  //取得input的值
 $("input").val("hello")  //改變input的值
```

8. text()

用來取得或改變元素的文字。
```
  $("span").text()  //取得span的值
  $("span").text("hello")  //改變span的值
```

## 使用 $(this) 簡化程式碼複雜度

$(this) 是把當前指定的元素轉換為jQuery對象。

例如：
```
  $("input").click(function () {
    var text = $(this).val();
  })
```

## e.x. 練習

![](/assets/jquery_tab.gif)

