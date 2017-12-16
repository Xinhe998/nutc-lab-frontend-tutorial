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

![](/assets/11)

當有多人同時進行開發，或做實驗性的功能coding時，又或是臨時有bug要處理，又不想放下手邊開發的流程，此時可以另開分支。

![](/assets/12)

> 通常我們較不會使用master主分支進行開發，多會另開一分支develop，並且又在develop上依正在開發功能細切分支。
>
> 且依照開發功能細開的分支，命名多為 feature-【功能名】，e.g. `feature-profile`。
>
> 若分支為處理bug專用，則通常命名為 fix-【功能名】，e.g. `fix-upload`。

```
$ git checkout -b develop
```

p.s. 如果當下的staging area不為空，此時再新建一分支，staging area內的檔案也會被一併帶到新分支上哦！

但如果這個分支的變更還不想commit，卻想另開新的分支時該怎麼做？

這時只要使用 `git stash` ，就可以先把這個分支的變更丟到暫存區中，它們就不會被帶到新分支上了～

列出暫存區內的所有資料

```
$ git stash list
```

將暫存區內的資料回復到staging area中

```
$ git stash pop
```

清除暫存區內的資料

```
$ git stash clear
```

## 切換分支

git checkout 除了可以捨棄變更，回復狀態外，也可以用來切換分支

```
$ git checkout master
```

使用 `git checkout branchname` 就可以囉

![](/assets/14)

