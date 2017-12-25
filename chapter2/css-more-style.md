# 更多CSS樣式

### 文字
| 屬性            | 說明                                                  |
| --------------- | ----------------------------------------------------- |
| color           | 設定文字顏色                                          |
| text-align      | 設定文字對齊：right、center、left                      |
| font-size       | 設定文字大小                                          |
| font-weight     | 設定文字加粗                                          |
| font-family     | 設定字體                                              |
| text-decoration | 設定文字裝飾：underline、none、overline、line-through |

### 背景

| 屬性                  | 說明                                                    |
| --------------------- | ------------------------------------------------------- |
| background            | 將背景屬性一次設定。                                    |
| background-color      | 背景顏色                                                |
| background-image      | 背景圖片                                                |
| background-position   | 背景圖片位置：center、top、bottom、right、left          |
| background-repeat     | 背景圖片是否重複：repeat、repeat-x、repeat-y、no-repeat |
| background-attachment | 背景圖片是否固定或滾動：scroll、fixed                   |

#### background-image
```
body {background-image: url(/assets/bg.png);}
```

#### background-repeat
```
body {
  background-image: url(/assets/bg.png);
  background-repeat: no-repeat;
}
```

#### background-position
```
body {
  background-image: url(/assets/bg.png);
  background-repeat: no-repeat;
  background-position:center;
}
```
也可以只用百分比值或長度值。
```
body {
  background-image: url(/assets/bg.png);
  background-repeat: no-repeat;
  background-position:50px 100px;
}
```

#### background-attachment
```
body {
  background-image: url(/assets/bg.png);
  background-repeat: no-repeat;
  background-attachment:fixed
}
```

### 表格

#### 邊框：border
```
table, td, th
{
  border:1px solid green;
}
```
