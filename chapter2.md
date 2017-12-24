# HTML是什麼?

HTML超文件**標記語言**\(HyperText Markup Language\)，由W3C維護，用來製作網頁檔案。

> HTML不是程式語言，而是標記語言。

# HTML文件結構

HTML文件是由標籤組成\(如下圖\)，除了`<!DOCTYPE>` 外大部分都是成對標籤，最外層由 `<html></html>` 包圍，裡頭包含兩個成對標籤 `<head></head>` 與 `<body></body>` 。

![](/assets/html結構.png)

其中，`<html></html>` 用來定義html文件，`<head></head>` 用來定義各種頁面資訊(e.g. 網站的Logo、大標題)，`<body></body>` 用來定義網頁內容本文。

# CSS是什麼?

CSS樣式表(Cascading Style Sheets)，有了 CSS，我們就可以將資料層及顯示層分開：

HTML 文件就只包括資料，而 CSS 則是告訴瀏覽器這些資料應該要如何顯現出來。

#CSS 語法通則

```
選擇器 { 
  屬性：設定值； 
}
```
在一個選擇器 (Selector) 中，可以設定的屬性數目沒有限制。

