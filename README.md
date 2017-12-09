# 垂直居中和水平居中的几种方法总结

## 垂直居中
gfgfdgf
1.table布局

```
<!DOCTYPE html>
<html>
<head lang="en">
    <meta charset="UTF-8">
    <title>垂直居中1</title>
    <style type="text/css">
        table{
             height:500px;
        }
    </style>
</head>
<body>
<div>
<table border="1">
    <tr>
        <td>
            <div>
                aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaav
                aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaav
                aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaav
                aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaav
            </div>
        </td>
    </tr>
</table>
</div>
</body>
</html>
```

2. display:table-cell

```
<!DOCTYPE html>
<html>
<head lang="en">
    <meta charset="UTF-8">
    <title>垂直居中2</title>
    <style type="text/css">
        .div1{
            display:table-cell;
            vertical-align: middle;
            border:1px solid red;
            height:500px;
        }
        .div2{
            width:100px;
            height:100px;
            background-color: #191919;
        }
    </style>
</head>
<body>
    <div class="div1">
        <div class="div2">阿斯达谁</div>
    </div>
</body>
</html>
```

3.父级相对定位，子级绝对定位

```
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title></title>
    <style>
        *{
            margin: 0;padding: 0;
        }
        .div1{
            width:400px;
            height:400px;
            border:2px solid red;
            position: relative;
        }
        .div2{
            width:100px;
            height: 100px;
            background-color: black;
            margin: auto;
            position: absolute;
            top: 0px;
            left: 0px;
            right: 0px;
            bottom: 0px;
        }
    </style>
</head>
<body>
    <div class="div1">
        <div class="div2"></div>
    </div>
</body>
</html>
```
## 水平居中

1.table margin:0 auto

```
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8">
    <title>水平居中1</title>
    <style>
        *{
            margin:0;
            padding:0;
        }
        table{
            margin: 0 auto;
        }
        td{
            border:1px solid red;
        }
        li{
            list-style-type: none;
        }
    </style>
</head>
<body>
    <table>
        <tr>
            <td>
                <ul>
                    <li>aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa</li>
                    <li>baaaaa</li>
                    <li>caaaaaa</li>
                </ul>
            </td>
        </tr>
    </table>
</body>
</html>
```

2.相对定位left 50%

```
<!DOCTYPE html>
<html>
<head>
    <meta http-equiv="Content-Type" content="text/html;charset=utf-8"/>     <!--定义字符编码gb2312  GBK-->
    <meta name="keywords" content="百度,搜索器,爬虫,搜索引擎"/>
    <meta name="description" content="百度网是一个什么都可以找到的网站"/>
    <meta name="author" content="作者"/>
    <meta name="copyright" content="声明 版本"/>   <!--定义网页的基本信息-->
    <title>百度一下，你就知道</title>         <!--定义网页的标题-->
    <link />                                    <!--导入外部CSS文件-->
    <style type="text/css">
        *{
            margin:0;
            padding:0;
        }
        .d1{
            display: inline-block;
            position:relative;
            left:50%;
            border:1px solid red;
        }
        .d1 ul{
            border:1px solid black;
            float: left;
            position:relative;
            left:-50%;
        }
        .d1 li{
            float:left;
            list-style:none;
        }
    </style>                           <!--定义CSS样式-->
    <script></script>                         <!--定义脚本语言JS Jquery-->
    <!--<meta http-equiv="refresh" content="3;url=http://www.baidu.com">-->
</head>
<body>
    <div class="d1">
        <ul>
            <li>aaaaaaaaaaaa</li>
            <li>bbbbb</li>
            <li>ccccc</li>
        </ul>
    </div>
</body>
</html>
```


