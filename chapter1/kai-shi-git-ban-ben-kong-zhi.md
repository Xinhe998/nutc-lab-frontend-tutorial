# Git的檔案狀態

![](/assets/4)

新建的檔案和更動過的檔案會進入紅色區，經由** git add **指令進入**等待提交**的黃色區。

**git commit**後，檔案便置於儲存區\(Repo\)，這些放在儲存區的檔案即是**已提交**的狀態。

暨上一篇建立的test專案，我們在之中加入一文字檔來做練習。

```
$ touch practice.txt
```

接著查看Git狀態

```
$ git status
```

![](/assets/5)

可以看到，現在practice.txt這份檔案現在處於

