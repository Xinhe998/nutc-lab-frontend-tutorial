## 不小心刪除檔案了怎麼辦？

承前篇所建的test專案為例，我們可以試著將practice.txt刪除

```
$ rm practice.txt
```

可以發現檔案已經消失得無影無蹤，連垃圾桶都找不到檔案\(超崩潰Q\_Q\)～

```
$ git checkout practice.txt
```

將將！本來消失的檔案順利被救回了！

使用 `git checkout filename` 會將該檔案回復到上一次commit的狀態，若有多個檔案且要全部回復\(捨棄變更\)，

可以使用 `git checkout .`

## 建立新分支

我們可以查看當下所在的分支

```
$ git branch
```

當有多人同時進行開發，或做實驗性的功能coding時，又或是臨時有bug要處理，又不想放下手邊開發的流程，此時可以另開分支。

> 通常我們較不會使用master主分支進行開發，多會另開一分支develop，並且又在develop上依正在開發功能細切分支。

```
$ git checkout -b develop
```



