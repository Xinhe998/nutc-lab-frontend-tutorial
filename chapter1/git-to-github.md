# Git 推上 Github 雲端儲存庫囉

前面幾章我們一直在本地端辛苦的操作版本控制，但要如何讓其他人也能取得到我的資料，並一同協作編輯呢?

這時候就要建立遠端儲存庫～

註冊好Github帳號後，建立New repository。

![](/assets/xinhe_github.png)

![](/assets/22.png)

輸入repo名稱後建立。

這樣遠端儲存庫就建立好了，讓我們試著把本地端已提交的資料推到Github上吧！![](/assets/23.png)每一個帳號的每一個repo都會有自己專屬的git連結

我們須在本地端把剛剛得到的連結加進這個專案的遠端庫

```
$ git remote add origin https://github.com/Xinhe998/test.git
```



