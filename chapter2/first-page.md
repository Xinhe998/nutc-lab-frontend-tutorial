# 第一個網頁

開始之前，要請大家先在VSCode安裝一些好用套件：

#### 1. **HTML Snippets**

提供一些常用的HTML片段程式碼。

![](/assets/html-plugin-1.png)

#### 2. Auto Close Tag

自動添加上閉合tag。

![](/assets/html-plugin-2.png)

---

安裝好上述套件後，在VSCode新增一html檔案，輸入html5並按下Enter

![](/assets/auto-html5.gif)

可以發現 **HTML Snippets** 套件自動完成了html5的template。

## head 頁面資訊

我們可以由剛剛產生的html5 template看到head區塊

`<title></title>`，

此標籤中的就是此網頁的標題，也就是您瀏覽器最左上面的標題，若沒設定則會顯示成此網頁的檔名。

---

`<meta charset="UTF-8">`

定義文件編碼。

---

`<meta name="viewport" content="width=device-width, initial-scale=1">`

W3C 在 HTML 制定了給手機網頁 Mobile Web 使用的 Viewport 螢幕解析度設定的語法。

viewport的作用是告訴瀏覽器，目前裝置有多寬\(或多高\)。

可以透過viewport來設定：

|  |  |
| :--- | :--- |
|  |  |
|  |  |
|  |  |

width：viewport寬度，通常設為device-width，用意是適應各家裝置的大小。

initial-scale：預設以多少倍的viewport來顯示

maximum-scale：定義頁面縮放的最高倍率

user-scalable：只有0與1兩個值，定義是否讓使用者自己調整viewport倍率

更多html `<meta>` Tag用法：[https://www.w3schools.com/tags/tag\_meta.asp](https://www.w3schools.com/tags/tag_meta.asp)

---

`<link href="css/style.css" rel="stylesheet">`

引入CSS樣式表。

## 認識 html Tags

| div | 用來標示一個網頁區塊到現在直接用來做網頁排版 |
| :--- | :--- |




