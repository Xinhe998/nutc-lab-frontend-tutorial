# 取得DOM元素節點

## DOM簡介

DOM的核心概念是將HTML於元素轉換成一顆節點數，而每一個標籤就是一個一個節點（Nodes），以走訪的方式來存取HTML元素。

![DOM&#x7BC0;&#x9EDE;&#x6A39;](../.gitbook/assets/image%20%283%29.png)

## JavaScript取得HTML元素

JavaScript要拿到HTML元素，就是利用上述DOM的方式取得節點物件，  
JavaScript可以用getElementById\(\)、getElementByTagName\(\)、getElementByName\(\)的方式拿到DOM元素。

1. getElementById\(\)

```markup
<head>
    <script type="text/javascript">
        //alert元素id是title物件之標籤內的內容
        alert(document.getElementById("title").innerHTML())
    </script>
</head>
<body>
    <h1 id="title"> 我是Title </h1>
</body>
```

      2. getElementByTagName\(\)

```markup
<head>
    <script type="text/javascript">
        //alert元素標籤是h1的內容
        alert(document.getElementTagName("h1").innerHTML())
    </script>
</head>
<body>
    <h1 id="title"> 我是Title </h1>
</body>
```

     3. getElementByName\(\)  
         用法與getElementById\(\) 方法相似，但它是查詢元素的name 屬性，而不是id 屬性。

```markup
<head>
    <script type="text/javascript">
        //alert元素name是myInput的值
        alert(document.getElementName("myInput").value)
    </script>
</head>
<body>
    <input name="myInput" type="text" value="大家好" />
</body>
```



