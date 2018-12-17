# JavaScript的物件（Object）

我們可以把Object當作是一個盒子，裡面可以塞下各種型態的資料。

建立方式：

```javascript
var obj = new Object();
obj.name = "Xinhe";
obj.gender = "female";
obj.email = "test@gmail.com";
console.log(obj);
```

以上我們使用了new運算子建立物件，但其實也有種方式：

```javascript
var obj = {
    name : "Xinhe",
    gender: "female",
    email: "test@gmail.com"
}
console.log(obj);
```

![](../.gitbook/assets/image%20%2813%29.png)

當我們只要取得這個物件的其中一個屬性時，可以直接使用objName.propertyName的方式：

```javascript
console.log("姓名：", obj.name);
```

如此一來，我們就可以在HTML中寫入物件的資料：

```markup
<p>姓名：</p>
<p>性別：</p>
<p>E-mail：</p>
```

```javascript
var obj = {  
        name : "Xinhe",   
        gender: "female",   
        email: "test@gmail.com"
}
document.getElementsByTagName("p")[0].innerHTML += obj.name;
document.getElementsByTagName("p")[1].innerHTML += obj.gender;
document.getElementsByTagName("p")[2].innerHTML += obj.email;
```

![](../.gitbook/assets/image%20%2810%29.png)



