# 動態CSS

我們可以使用JavaScript來得到和變動指定物件的CSS屬性，藉以來建立動態的顯示效果。

## style物件屬性

利用JavaScript中的style語法，我們就可以拿到和更改物件的**inline-style**。

```javascript
document.getElementById("box").style.color;
document.getElementById("box").style.color = "#ffffff";
```

{% hint style="warning" %}
以上方法是存取HTML物件的inline-style，但若想要拿到定義在CSS檔裡面的style，必須使用getComputedStyle\(element\) 的方法才行。

```javascript
getComputedStyle(document.getElementById("box")).color;
```
{% endhint %}



