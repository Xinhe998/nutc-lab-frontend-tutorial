## 分支合併\(merge\)

當我們在develop上的開發達到一定程度，可以將develop上的內容合併回master上。

就讓我們來做一個分支合併的練習吧～

```
$ git checkout develop
```

編輯practice.txt![](/assets/15)此時在develop分支上的practice.txt內容是"hello develop"，

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

