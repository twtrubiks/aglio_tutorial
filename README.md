# aglio-tutorial

aglio tutorial

 aglio 基本教學

* [Youtube Tutorial]()

相信大家在網路上一定都看過 **API 文件**，

那我們該如何撰寫 **API 文件** 給別人看呢 ？

今天我要教大家使用  [aglio](https://github.com/danielgtaylor/aglio) 來完成他 ！！

***溫馨小提醒***

之前也有介紹過利用 Swagger 建立 **API 文件**

[django_rest_framework_swagger_tutorial](https://github.com/twtrubiks/django_rest_framework_swagger_tutorial)

但今天的主角是 [aglio](https://github.com/danielgtaylor/aglio)

 自由度更高！！

## 安裝環境

***安裝 nodejs***

請先確認自己的電腦有安裝 [nodejs](https://nodejs.org/en/)

***安裝 aglio***

請在你的命令提示字元 (cmd ) 底下輸入

使用 npm 安裝  [aglio](https://github.com/danielgtaylor/aglio)
>npm install -g aglio

## 教學

我們依照 [DRF-dataTable-Example-server-side](https://github.com/twtrubiks/DRF-dataTable-Example-server-side) 這篇文章下去設計 API

Commandline executable

要將 **.apib** 邊譯為 **.html** , 可以執行

```cmd
aglio -i index.apib -o index.html
```

那你現在一定在想，每次都要重新編譯超級麻煩 :angry:，但請不用擔心，

我們可以使用 **Live-reloading preview server**

( 也就是即時觀看，改什麼立即可以看到結果 )

```cmd
aglio -i index.apib --server
```

![](http://i.imgur.com/9AyeIyS.png)

接下來我們只需要去瀏覽 [http://localhost:3000/](http://localhost:3000/) 就可以即時看到修改的內容。

***注意***

有時候在編譯，會提醒你錯誤，請把錯誤都修正，避免不必要的問題

## 其他功能介紹

為了方便維護 API 文件，我們可以使用 **Including Files** 的方法

```no-highlight
<!-- include(filename.md) -->
```

更多用法可參考官方說明

[https://github.com/danielgtaylor/aglio#installation--usage](https://github.com/danielgtaylor/aglio#installation--usage)

## 執行畫面

依照 [DRF-dataTable-Example-server-side](https://github.com/twtrubiks/DRF-dataTable-Example-server-side) 這篇文章下去設計 API

可以參考我的 [index.html](https://github.com/twtrubiks/aglio_tutorial/blob/master/index.html)，直接用瀏覽器開啟即可 :smile:

![](http://i.imgur.com/xOe8qsD.png)

畫面蠻漂亮的，也有很多種 theme 可以選擇

更多 theme 可以參考

[https://github.com/danielgtaylor/aglio#example-output](https://github.com/danielgtaylor/aglio#example-output)

## 結論

由於之前介紹過 Swagger ，所以就用 [aglio](https://github.com/danielgtaylor/aglio) 和 Swagger 比較一下吧 !!

API 文件  | 優點                  |  缺點
--:      | ----------            | ----------
 Aglio   | 自訂性高且支援 Markdown | 不可以直接測試 API
 Swagger | 可以直接測試 API        | 自訂性較低

其實說穿了，還是要看自己的需求，如果需要自訂性比較高的，那一定就是選 [aglio](https://github.com/danielgtaylor/aglio) ;

相反的，假如需要可以直接測試且自動的幫你生成，就選 Swagger ( 自訂性較低 )。

所以說依照當下的需求下去選擇撰寫 **API 文件** 的工具絕對沒錯！！

## Reference

* [aglio](https://github.com/danielgtaylor/aglio)
