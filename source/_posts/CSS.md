---
title: CSS回顾
date: 2022-09-17 17:43:31
tags: CSS
categories:
- Web前端
cover: https://www.v2fy.com/asset/0i/jikemiji/jikemiji-md/kr-000063.assets/%E5%88%9D%E9%9F%B3%E6%9C%AA%E6%9D%A5.jpg
---
<h3>CSS是Cascading Style Sheets（层叠样式表单）的缩写，它是一种用来表现HTML或 XML 等文件式样的计算机语言。CSS的作用就是为网页设置外观，相
当于给HTML文档穿上了华丽的衣服。</h3>
<h3>CSS</h3>
```HTML   
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <!-- 
        第二种方式（内部样式表）：
            -将样式写在head里的style标签里
                然后通过css的选择器来选中元素并为其设置各种样式
                可以同时为多个标签设置样式，并且修改时只需要修改一处
            -方便复用
            -问题：
                内联样式表只对一个网页生效，不能跨网页起复用的作用
     -->
     <style>
       p{
            color: bisque;
            font-size: 60px;
        }
     </style>

     <!-- 
        第三种方式（外部样式表）：
            -创建一个css文件，并用<link>标签引入
            -可跨页面复用
            -最佳的使用方式
            -将样式编写到外部的css文件中，可最大的利用浏览器的缓存机制。
            从而加快网页的加载速度，提升用户的体验。
      -->
      <link rel="stylesheet" href="./p.css">
</head>
<body>
    <!-- 
        css
            -层叠图样式表
            -网页实际上是一个多层的结构，通过css可以分别为网页的没一层来设置样式
             最终我们能看到的只是最上面的一层
            -css就是用来设置网页中元素的样式
     -->

     <!-- 
        使用css来修改元素的样式
        第一种方式（内联样式，行内样式）：
            -在标签内通过style属性来设置元素的样式
            -问题：
                使用内联式，样式只能对一个标签生效
                如果希望影响多个必须在每一个元素中复制一遍
                当样式发生变化时，要修改的太多
        开发中不要使用
      -->
     <p style="color:red; font-size: 90px;">学习html5</p>

     <p>学习css3</p>
</body>
</html>
```
<h3>CSS语法</h3>
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
            css的基本语法：
                选择器 声明
                选择器，通过选择器可以选择页面中的指定元素
                    比如p的作用就是选中页面中的所有p元素（标签选择器）
                声明块
                    通过声明块为标签设置样式
        */
        h1{
            color: aquamarine;
            font-size: medium;
        }
        /* 标签选择器 标签名+{} */
        p{
            color: blanchedalmond;
            font-size: small;
        }
    </style>
</head>
<body>
    <h1>css的基本语法学习</h1>
    <p>css</p>
</body>
</html>
```
<h3>常用的选择器</h3>
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
            元素选择器
                作用：根据标签名来选中指定的元素
                语法：标签名{}
                例子：p{}，h1{}
        */
        h1{
            color: brown; 
        }
        p{
            color: aquamarine;
        }

        /* 
            id选择器
                作用：根据唯一的id来选中元素
                语法：#id名{}
                例子：#slow{}
        */
        #slow{
            color: blue;
        }

        /* 
            类选择器
                作用：根据claa的属性选中一组元素
                语法：.class名{}
                例子：.blue{}
        */
        .blue{
            color: blueviolet;
        }
        .fontSize{
            font-size: 60px;
        }

        /* 
            通配符选择器
                作用：选中页面中所有元素
                语法：*{}
        */
        *{
            font-size: xx-large;
        }
    </style>
</head>
<body>
    <h1>我是标题</h1>
    <p>css的基本语法学习</p>
    <p id="slow">进度太慢了</p>
    <!-- 
        class是一个标签的属性，它和id类似。但是它是一组，
        里面的值可以出现在多个标签中
         可以同时为一个元素指定多个class
     -->
    <p class="blue fontSize">测试</p>
    <p class="blue">看看</p>
</body>
</html>
```
<h3>复合选择器</h3>
```HTML   
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width==device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        /* 
            交集选择器
                作用：选择同时复合多个条件的元素
                语法：选择器1选择器2选择器3{}
                例子：p.red{} 不推荐p#slow{} #slow已经具有唯一性
        */
        p.red{
            color: red;
        }

        /* 
            选择器分组（并集选择器）
                作用：同时选择多个选择器对应的元素
                语法：选择器1，选择器2，选择器3
                例子：p，sapn
        */
        p,span{
            color: blueviolet;
        }
    </style>
</head>
<body>
    <h1>我是标题</h1>
    <p>第一行</p>
    <p class="red">第二行</p>
    <span>第三行</span>
</body>
</html>
```
<h3>关系选择器</h3>
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
            为div的子元素span设置一个字体颜色为红色
            （为div直接包含的span设置一个字体颜色）
            子元素选择器（只有第一代变）
                作用：选中指定父元素的指定的子元素
                语法：父元素 > 子元素
        */
        div > span{
            color: bisque;
        }

        /* 
            后代元素选择器 (是后代都变)
                作用：选中指定的元素内的指定后代元素
                语法：祖先 后代
        */
        div span{
            color: aqua;
        }

        /* 
            选择下一个兄弟（相邻的是才变不是不变）
                语法：前一个 + 下一个
                p + span
            选择下边所有的兄弟
                语法：兄 ~ 弟
                p ~ span
        */
        /* p ~ span{
            color: blue;
        } */
    </style>
</head>
<body>
    <!-- 
        父元素
            -直接包含子元素的元素叫父元素
        子元素
            -直接被父元素包含的元素是子元素
        祖先元素
            -直接或间接包含后代元素的元素叫做祖先元素
            -一个元素的父元素也是它的祖先元素
        后代元素
            -直接或间接被祖先元素包含的元素叫后代元素
            -子元素也是后代元素
        兄弟元素
            -拥有相同父元素的元素是兄弟元素
     -->
    <div>
        我是一个div
        <p>
            我是div中的p元素
            <span>
                我是p中的span
            </span>
        </p>
        <span>
            我是div中的span1
        </span>
        <span>
            我是div中的span2
        </span>
        <span>
            我是div中的span3
        </span>
    </div>
    
</body>
</html>
```
<h3>属性选择器</h3>
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
            [属性名] 选择含有指定属性的元素
            [属性名=属性值] 选择含义指定属性和属性值的元素
            [属性名^=属性值] 选择属性值以指定值开头的元素
            [属性名$=属性值] 选择属性值以指定值结束的元素
            [属性名*=属性值] 选择属性值中含有某值的的元素的元素
        */

        /* p[title]{
            color: aqua;
        } */

        /* p[title=abc]{
            color: antiquewhite;
        } */

        /* p[title^=abc]{
            color: beige;
        } */

        /* p[title$=abc]{
            color: blue;
        } */

        p[title*=e]{
            color: brown;
        }


    </style>
</head>
<body>
    <p title="abc">1</p>
    <p title="abcdef">2</p>
    <p title="helloabc">3</p>
    <p title="asdas">4</p>
</body>
</html>
```
<h3>伪类选择器</h3>
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
            伪类（不存在的，特殊的类）
                -伪类用来描述第一个元素的特殊状态
                    比如：第一个子元素，被点击的元素，鼠标移入的元素...
                -伪类一般都是:开头
                    :first-child 第一个子元素
                    :last-child 最后一个子元素
                    :nth-child() 选中的第n个元素
                        特殊值：
                            n 第n个 n的范围从0到正无穷
                            2n 或 even 表示选中偶数位的元素
                            2n+1 或 odd 表示选中基数位的元素  
                        -以上这些伪类都是根据所有的子元素进行排序

                    :first-of-type
                    :last-of-type
                    :nth-of-type()
                        -这几个伪类的功能和上述的类似，不同点是它们是在同类型元素中进行排序

                -:not()否定伪类
                    -将符合条件的元素从选择器去除
                    
        */

        /* ul > li:first-child{
            color: red;
        }
        ul > li:last-child{
            color: green;
        }
        ul > li:nth-child(3){
            color: bisque;
        } 
        ul > li:not():first-child{
            font-size: 50px;
        } */

       

        /* ul > li:first-of-type{
            color: green;
        }
        ul > li:last-of-type{
            color: green;
        }
        ul > li:nth-of-type(3){
            font-size: 30px;
        } */


    </style>
</head>
<body>
    <ul>
        <!-- <span>0</span> -->
        <li>1</li>
        <li>2</li>
        <li>3</li>
        <li>4</li>
        <li>5</li>
    </ul>
</body>
</html>
```
<h3>元素的伪类</h3>
```HTML   
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <!-- 
        :link 用来表示没访问过的链接
        :visited 用来表示没访问过的链接 （只能修改颜色，保护隐私）
     -->
    <style>
        a:link{
            color: orange;
        }
        a:visited{
            color: bisque;
        }

        /* 
            :hover 用来表示鼠标移入的状态
        */
        a:hover{
            font-size: 30px;
        }

        /* 
            :active 鼠标点击
        */
        a:active{
            color: blueviolet;
        }
    </style>
</head>
<body>
    <a href="https://valynd.github.io/valyn/">访问过的链接</a>
    <br><br>
    <a href="https://valynd.github.io/valyn/">没访问过的链接</a>
</body>
</html>
```
<h3>伪元素选择器</h3>
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
            伪元素，表示在页面中的一些特殊的并不真实的元素（特殊的位置）
                伪元素使用::开头

                ::first-letter 表示第一个字母
                ::first-line 表示第一行
                ::selection 表示选中的内容
                ::before 元素开始的位置
                ::after 元素结束的位置
        */
        p::first-letter{
            color: red;
        }
        p::first-line{
            background-color: beige;
        }
        p::selection{
            font-size: 30px;
        }
        P::before{
            content: "'";
        }
        p::after{
            content: "'";
        }
    </style>
</head>
<body>
    <p>Hello world！</p>
</body>
</html>
```
<h3>样式的继承</h3>
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
            样式的继承，我们为一个元素设置的样式同时也会应用到它的后代元素上

            继承是发生在祖先与后代之间

            继承的设计是为了方便我们的开发，利用它我们可以将一些通用的样式统
            一设计到共同的祖先上，达到复用的作用

            注意：不是所有的样式都会被继承，比如背景相关，布局相关的就不会
        */
        div{
            color: bisque;
            font-size: 30px;
            background-color: rgb(39, 129, 167);
        }
        .p:hover{
            color: brown;
        }
        #h1:active{
            color: blueviolet;
        }
    </style>
</head>
<body>
    <div id="container">
        <h1 id="h1">无为而治</h1>
        <p class="p">我是一段文字</p>
    </div>
</body>
</html>

```
<h3>选择器的权重</h3>
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
            样式发生冲突时，是由于选择器权重（优先级）引起的
            选择器的权重
                -内联样式（标签内的属性）    1000
                -id选择器（#）               100
                -类和伪选择器（.）            10
                -元素选择器（元素名）          1
                -通配选择器（*）               0
                -继承的样式            没有优先级

            比较优先级时，需要将所有的选择器的优先级进行相加，最后优先级高的优先显示（分组选择器是单独计算的eg：span，p）
            选择器的累加不会超过其最大的数量级，类选择器再高也不会超过id选择器
            如果优先级计算后相同，则在下面的优先

            可以在某一个样式后面加!important,此时优先级最高。甚至超过内联样式
        */
        div{
            background-color: rgb(15, 110, 25);
        }
        /* .div{
            background-color: rgb(220, 31, 31)!important;
        } */
        #div1{
            background-color: rgb(170, 23, 116);
        }
        div{
            font-size: 30px;
        }
        *{
            font-size: 50px;
        }
    </style>
</head>
<body>
    <div class="div" id="div1">
        我是一个div标签
        <span>我是一个span标签</span>
    </div>
</body>
</html>
```
<h3>单位</h3>
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
            长度单位：
                像素
                    -屏幕实际上是由一个一个的小点构成
                    -不同的屏幕像素是不同的。像素越小的屏幕显示的效果越清晰
                    -所以同样的200px在不同的设备下显示效果是不一样的

                百分比
                    -也可以将属性值设置为相对于父属性的百分比
                    -设置百分比可以使子元素跟随父元素的改变而改变

                em
                    -em是相对于元素的字体大小来计算的
                    -1em = 1font-size
                    -em会根据字体大小的改变而改变

                rem
                    -rem是根据根元素的字体大小来计算
        */
        .box1{
            background-color: aquamarine;
            width: 50px;
            height: 50px;
        }
        .box2{
            background-color: bisque;
            width: 50%;
            height: 50%;
        }
        .box3{
            background-color: blueviolet;
            width: 25px;
            height: 25px;
        }
    </style>
</head>
<body>
    <div class="box1">
        <div class="box2"></div>
    </div>
    <div class="box3"></div>
</body>
</html>
```
<h3>颜色</h3>
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
            颜色单位：
                在css中可以直接使用颜色名来设置各种颜色
                    比如：red，green
                    但在css中直接使用颜色名是非常不方便的

            RGB值：
                -RGB通过三种颜色的不同浓度调配出不同的浓度
                -R red，G green，B blue
                -每一种颜色的范围在0到255（0%到100%）
                -语法：RGB（红，绿，蓝）

            RGBA：
                -就是在rgb的基础上增加了一个透明度a
                -需要四个值，前三个和rgb一样，第四个表示不透明度（1不透明，0完全透明）

            十六进制的RGB值：
                -语法：#红绿蓝
                -颜色浓度通过 00-ff
                -如果颜色两位两位重复可以进行简写
                    #aabbcc --> #abc 但是 aabbcd不行
            
            HSL值 HSLA值
                H 色相（0 - 360）
                S 饱和度，颜色的浓度 0% - 100%
                L 亮度，颜色的亮度 0% - 100%
                eg：backgroud-color: hsl(360,100%,100%);
        */
        .box1{
            background-color: #bfa;
            width: 100px;
            height: 100px;
        }
        .box2{
            background-color: rgba(23, 25, 150,0.25);
            width: 100px;
            height: 100px;  
        }
    </style>
</head>
<body>
    <div class="box1"></div>
    <div class="box2"></div>
</body>
</html>
```