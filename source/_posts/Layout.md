---
title: Layout回顾
date: 2022-09-17 17:43:31
tags: CSS
categories:
- Web前端
cover: https://pic1.zhimg.com/v2-077a594b1a64d55e95de392755a8aa76_r.jpg?source=172ae18b
---
<h3>文档流</h3>
```HTML   
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        /* 
            文档流（normal flow）
                -网页是一个多层的结构，一层摞这一层
                -通过CSS可以分别为每一层设置样式
                -作为用户来说只能看到最上面一层
                -这些层中，最底下的称为文档流，文档流是网页的基础
                    我们所创建的元素默认都是在文档流中进行排列
                -对于我们元素主要有两个状态
                    在文档流中
                    不在文档流中（脱离文档流）

                -元素在文档流中有什么特点：
                    -块元素
                        -块元素会在网页中独占一行（自上而下垂直排列）
                        -默认宽度为父元素的全部（会把父元素撑满，即浏览器大小）
                        -默认的高度是被内容撑开（子元素）
                    -行内元素
                        -行内元素不会独占一行，只占自身大小
                        -行内元素在页面中自左向右水平排列，如果第一行放不下则元
                        素会换到第二行
                        -行内元素宽高都是被内容撑开
        */
        .div1{
            border-color: aquamarine;
            width: 100px;
        }
        .div2{
            border-color: rgb(52, 45, 149);
        }
        span{
            color: bisque;
        }
    </style>
</head>
<body>
    <div class="box1">我是div1</div>
    <div class="box2">我是div2</div>
    <span>1</span>
    <span>2</span>
    <span>3</span>
    <span>4</span>
</body>
</html>
```
<h3>盒模型</h3>
```HTML   
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .box1{
            /* 
                内容区（content），元素中的所有的子元素和文本内容都在内容区中排列
                    内容区的大小由width和heigth两个属性来设置
                        width 设置内容区的宽度
                        height 设置内容区的高度
            */
            background-color: #bfa;
            width: 200px;
            height: 200px;
            /* 
                边框（border），边框属于盒子边缘，边框里边属于盒子内部，出了边框都
                    是盒子的外部边框的大小会影响到整个盒子的大小
                要设置边框，至少需要设置三个样式：
                    边框的宽度 border-width
                    边框的颜色 border-color
                    边框的样式 border-style
            */
            border-width: 5px;
            border-color: aquamarine;
            border-style: solid;
        }
    </style>
</head>
<body>
    <!-- 
        盒模型，盒子模型，框模型（box model）
            -CSS将页面中的所有元素都设置为一个矩形的盒子
            -将元素设置为矩形的盒子后，对页面的布局就变成将不同的盒子摆放到不同的位置
            -每一个盒子都由以下几个部分组成：
                内容区（content）
                内边距（padding）
                边框（border）
                外边距（margin）
     -->
    <div class="box1"></div>
</body>
</html>
```
<h3>盒子模型_边框</h3>
```HTML   
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        /* 
            边框
                边框的宽度 border-width
                边框的颜色 border-color
                边框的样式 border-style
        */
        .box1{
            background-color: #bfa;
        /* 
            border-width: 10px;
                默认值为3px（不指定时）
                border-width可以用来指定四个方向的边框宽度
                    值的情况
                        四个值：上 右 下 左
                        三个值：上 左右 下
                        两个值：上下 左右
                        一个值：上下左右

            除了border-width还有一组border-xxx-width
                xxx可以是top left right bottom
                用来单独指定某一个边的宽度
                eg：border-top-width: 10px;
        */

            border-width: 200px;
        /* 
            border-color用来指定边框的颜色，规则与border-width一样

            border-color也可以省略不写，省略时以color颜色值为准
            eg：color: #bfa;
        */
            border-color: aqua;

        /*
            border-style指定边框的样式
                solid 表示实线
                dotted 点状虚线
                dashed 虚线
                double 双线

            默认值为none表示没有边框，必须写初值
        */
            border-style: solid;

        /*
            border简写属性，通过该属性可以同时设置边框所有的相关样式，并且没有顺序要求

            除了border以外还有四个 border-xxx
                border-top
                border-bottom
                border-left
                border-right
            eg：border: 10px red solid
        */
        }
    </style>
</head>
<body>
    <div class="box1"></div>
</body>
</html>
```
<h3>盒子模型_内边距</h3>
```HTML   
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .box1{
            color: violet;
            background-color: #bfa;
            width: 200px;
            height: 200px;
            border: 10px orange solid;
            /* 
                内边距（padding）
                    -内容区和边框间的距离是内边距
                    -一共有四个方向的内边距：
                        padding-top
                        padding-bottom
                        padding-left
                        padding-right
                    
                    -内边距的设置会影响到盒子的大小
                    -背景颜色会延续到内边框上
                
                一个盒子的可见框的大小，由内容区 内边距 边框共同决定，
                    所以在计算盒子的大小时，需要将这三个区一起计算

                padding内边距的简写属性，可以同时指定四个方向的内边距
                    规则和border-width一样
            */
            padding: 5px;
        }
    </style>
</head>
<body>
    <div class="box1">我是一个div</div>
</body>
</html>
```

