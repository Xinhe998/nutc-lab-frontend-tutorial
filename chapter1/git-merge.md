## 分支合併\(merge\)

當我們在develop上的開發達到一定程度，可以將develop上的內容合併回master上。

就讓我們來做一個分支合併的練習吧～

```
$ git checkout develop
```

編輯practice.txt![](/assets/15.png)此時在develop分支上的practice.txt內容是"hello develop"，

但在master分支上依然會是"hello"。

我們可以commit剛才編輯的資料後，切換到master分支瞧瞧！

```
$ git add practice.txt
提交剛才編輯的資料
$ git commit -m "新增develop字樣"

切換到master分支
$ git checkout master

將develop的資料合併到master上
$ git merge develop
```

利用 `git merge branchname` 可以將指定的分支內容合併進當前的分支。

現在develop分支和master分支上的practice.txt內容都會是"hello develop"囉～

## 衝突合併

有時候合併並不會如此順利。如果**在不同的分支中都修改了同一個檔的同一部分**，這時就會出現**conflict衝突**。

```
切換到develop分支
$ git checkout develop
```

將practice.txt內容修改為"hello world"

![](/assets/16.png)

```
$ git add practice.txt
提交剛才編輯的資料
$ git commit -m "修改develop分支為hello world"
```

```
切換到master分支
$ git checkout master
```

將practice.txt內容修改為"hello jack"

![](/assets/17.png)

```
$ git add practice.txt
提交剛才編輯的資料
$ git commit -m "修改master分支為hello jack"
```

此時就達成**在不同的分支中都修改了同一個檔的同一部分。**

這時試著將develop分支合併到master分支看看吧！

```
$ git merge develop
```

衝突果然如我們預期的發生la!!!!!!!!!

![](/assets/18.png)

多人協作時發生衝突是無可避免的，大家遇到衝突千萬不要緊張～就讓我們心平氣和地來解個衝突唄～

![](/assets/19.png)使用VSCode的好處切換分支內容也能跟著即時更新，且當有衝突能夠清楚明瞭的顯示，並讓使用者輕鬆合併。

這時就看自己需要留下與捨棄哪個部分的內容，或是要接受兩者變更都可以哦！![](/assets/20.png)

解決完衝突後，別忘了儲存檔案，並再次提交哦~

