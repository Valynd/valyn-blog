---
title: Layout回顾
date: 2022-09-17 17:43:31
tags: CSS
categories:
- Web前端
cover: https://img.win3000.com/m00/bf/f7/a3dbc7c75ed2768afae99747d33a5a70.jpg
---
<h3>协助进行页面级整体布局。Layout布局容器，其下可嵌套 Header Sider Content Footer 或 Layout 本身，可以放在任何父容器中。</h3>
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
<h3>外边距</h3>
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
            外边距（margin）
                -外边距不会影响盒子可见框的大小
                -但是外边距会影响盒子的位置
                -一共有四个方向的外边距：
                    margin-top
                        -上下边距，设置一个正值，元素会向下移动
                    margin-right
                        -默认情况下设置margin-right不会产生任何效果
                    margin-bottom
                        -下外边距，设置一个正值，其下边元素会向下移动
                    margin-left
                        -左外边距，设置一个正值，元素会向右移动

                -元素在页面中按照自左向右顺序排列
                    所以默认情况下我们设置的左和上边外边距则会移动自身
                    而下和左外边距则会移动其它元素

                -margin简写
                    margin可以设置四个方向的外边距，用法和padding一样

                -margin会影响到盒子实际占用空间
        */
        .box1{
            background-color: #baf;
            width: 220px;
            height: 220px;
            border: 5px orange solid;
            padding: 10px;
            margin: 50px 30px 30px 10px;
        }
        .box2{
            background-color: #bfa;
            width: 250px;
            height: 250px;
        }
        .box3{
            background-color: rgb(69, 133, 224);
            width: 220px;
            height: 220px;
        }
    </style>
</head>
<body>
    <div class="box1">
        <div class="box3"></div>
    </div>
    <div class="box2"></div>
</body>
</html>
```
<h3>盒子的水平布局</h3>
```HTML   
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .outer{
            width: 800px;
            height: 200px;
            border: 10px red solid;
        }
        .inner{
            width: 200px;
            height: 200px;
            background-color: #bfa;
            margin-left: 100px;
        }
        /* 
            元素的水平方向的布局：
                元素在其父元素中水平方向的位置由以下几个属性共同决定：
                    margin-left
                    border-left
                    padding-left
                    width
                    padding-right
                    border-right
                    margin-right
                            
                一个元素在其父元素中，水平布局必须满足以下的等式
        margin-left + border-left + padding-left + width
        + padding-right + border-right + margin-right = 其父元素内容区的宽度（必须满足）

            0 + 0 + 0 + 200 + 0 + 0 + 0 = 800 不成立
            0 + 0 + 0 + 200 + 0 + 0 + 600 = 800 成立

            100 + 0 + 0 +200 + 0 + 0 + 0 = 800
                -以上的等式必须满足，如果相加的结果使等式不成立，则称为过渡约束，则等式会自动调整
                    -调整的情况：
                        -如果这七个值中没有为auto的情况，则浏览器会自动调整margin-right值使得等式成立
                -这七个值中有三个为auto
                    width
                    margin-left
                    margin-right
                    -如果某个值为auto，则自动调整为auto的那个值以使等式成立
                        0 + 0 + 0 + auto + 0 + 0 + 0 = 800      auto = 800
                        0 + 0 + 0 + auto + 0 + 0 + 200 = 800    auto = 600
                        200 + 0 + 0 + auto + 0 + 0 + 200 = 800  auto = 400

                        auto + 0 + 0 + 200 + 0 + 0 + 200 = 800  auto = 400

                        auto + 0 + 0 + 200 + 0 + 0 + auto = 800 auto = 300
                    
                    -如果将一个宽度和一个外边距设置为auto，则宽度会调整到最大，设置为auto的外边距会自动为0
                    -如果将三个值都设置为auto，则外边距都是0，宽度最大
                    -如果将两个外边距设置为auto，宽度值固定，则会将外边距设置为相同的值
                        所以我们经常利用这个特点来使一个元素在其父元素中水平居中
                        eg：
                            width：xxxpx;
                            margin: 0 auto;
        */
    </style>
</head>
<body>
    <div class="outer"></div>
    <div class="inner"></div>
</body>
</html>
```
<h3>垂直方向的布局</h3>
```HTML   
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .outer{
            background-color: #baf;
            height: 600px;
            /* 
                默认的情况下父元素的高度会被内容撑开
            */
        }

        .inner{
            width: 100px;
            background-color: yellow;
            height: 100px;
            margin-bottom: 100px;
        }

        .box1{
            width: 200px;
            height: 200px;
            background-color: #bfa;
            /* 
                子元素是在父元素的内容区排列的，
                    如果子元素的大小超过了父元素，则子元素会从父元素溢出

                    可选值：
                        visible，默认值 子元素会从父元素中溢出，在父元素外部的位置显示
                        hidden 溢出的内容会将被裁剪不会显示
                        scroll 生成两个滚动条，通过滚动条来查看完整的内容
                        auto 根据需求生成滚动条

                overflow-x：
                overflow-y:
            */
            overflow: auto;
        }

        .box2{
            width: 100px;
            height: 400px;
            background-color: orange;
        }
    </style>
</head>
<body>
    <div class="outer">
        <div class="inner"></div>
    </div>
    
    <div class="box1">刚刚结束了班夫的自驾游，去之前一点没做攻略，除了传说中对美景的盛赞，对那里几乎一无所知。

        头一次毫无准备地上路，得益于同行的友人一家，他们已是三顾班夫了，轻车熟路，所以我放心地当了甩手掌柜，从装备到路线、酒店、景点、美食，统统不必操心，乐得轻松自在。
        
        这是一片广袤的天地，无一处不风景，无一眼不风情。
        
        最喜欢峡谷里的瀑布，清凉的冰水摧枯拉朽般从高耸的岩壁奔流而下，无止无休，千年万年，冲刷出今日的残岩断壁。伫立在水边，俯仰之间，山水交融，仿佛看到了久远的一幕，子在川上曰：逝者如斯夫。
        
        而友人一家之所以乐此不疲地到此三游，则是为了一座岛——精灵岛，位于嘉士伯国家公园的马琳湖。
        
        精灵岛已经成了他们心中的一份执念。
        
        第一次慕名而至，临近冬季，一场大雪扑灭了他们通往精灵岛的梦幻之旅。
        
        第二次避开了雪季，却不想又被大雾遮望眼，再一次与精灵岛失之交臂。
        
        此行已是第三次了，虽然沿途的�爸掳倏床谎幔幢炔簧闲南稻榈旱囊谎邸�
        
        遗憾的是，又一次天公不作美，明明之前连日的晴空万里，偏偏这一日阴雨绵绵云雾缭绕，注定又要错失梦想中的小岛了。
        
        我的心情还好，因为没有过多的期待，入目皆是美景，撑起雨伞欣赏了一圈雨中湖景朦胧岛影，后来在湖边的礼品店里看到了清晰的精灵岛图片，权当完成了心愿。
        
        友人静静地站在湖边，望着面前的雨幕，一言不发。
        
        我向她提议，“不如我们多呆一天，或许明天就放晴了。”
        
        “天气预报说今天下午才有雨，本以为早上赶过来还能来得及看一眼的。”她失落地说。
        
        “那明天呢？”我暗自惭愧，自己连天气预报都没看。
        
        “明天也有雨。”她皱眉道。
        
        “那--”我不知该说什么安慰好了。
        
        “走吧，这就是人生，总要有点遗憾的，就让它永远留在我的心里，偶尔想念一下，作为求而不得的最美风景吧！”她甩甩头，最后看了一眼她的梦想，然后潇洒地往回走了。
        
        她的一番话似乎把所有的不悦都带走了，突然觉得这样的遗憾竟比睛天还美。
        
        风景自在人心，有时候不完美也是一种完美。
        
        于是想起另一个故事。
        
        一次聚会，有个朋友刚从张家界旅游回来，大赞那里风景绝美，堪称人间仙境。
        
        在看过她晒出的自拍后，所有人都开始兴致勃勃地憧憬起来，相约什么时侯有假期可以同行。
        
        只有闺蜜沉默不语。
        
        我后知后觉地记起来，她和初恋男友分手的那年暑假，正是她男友从张家界回来之后不久。
        
        她曾经说过，此生都不会去那个地方，因为在她心里，那是世界上最美的地方，是他曾经承诺要带她一起去看的风景，因为少了他，再美的风景都是泡影。
        
        难道这么多年过去了，她还没能放下？
        
        她看出我的疑惑，淡淡地笑了，“不是因为他，纯粹是不想去。我相信它是最美的，就因为相信，所以不想破坏了它在我心里的那份完美，一旦真正去了，总会有遗憾，现实永远没有想象的完美。”
        
        她把初恋放下了，却放不下他为她描绘的那片风景。还是因为太在意啊，没有期盼，何来遗憾？
        
        人生需要遗憾，因为遗憾，所以真实；因为遗憾，所以美丽。
        
        就象张家界之于闺蜜，精灵岛之于友人一家，每个人的遗憾都源于心中所念。
        
        心有所系，故有所憾。</div>
    <!-- <div class="box2"></div> -->
</body>
</html>
```
<h3>外边距的折叠</h3>
```HTML   
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .box1,.box2{
            width: 200px;
            height: 200px;
            font-size: 100px;
        }

        /* 
            外边距的重叠（折叠）
                -相邻的垂直方向外边距会发生折叠现象
                -兄弟元素
                    -兄弟元素间的相邻垂直外边距会区两者间的最大值（两者都是正值）
                    -特殊情况：
                        如果相邻的外边距一正一负，则取两者的和
                        如果相邻的外边距都为负值，则取两者中绝对值较大的

                    -兄弟元素之间的外边距的重叠，对于开发是有利的，所以我们不需要进行处理

                -父子元素
                    -父子元素间相邻外边距，子元素的会传递给父元素（上外边距）
                    -父子外边距的折叠会影响到页面的布局，必须要进行处理
        */

        .box1{
            background-color: #bfa;
            /* 设置一个下外边距 */
            margin-bottom: 100px;
        }

        .box2{
            background-color: #baf;
            /* 设置一个上外间距 */
            margin-top: 100px;
        }

        .box3{
            width: 200px;
            height: 200px;
            background-color: rgb(20, 129, 169);
            /* padding-top: 100px; */
        }

        .box4{
            width: 100px;
            height: 100px;
            background-color: rgb(169, 19, 112);
            margin-top: 100px;
        }
    </style>
</head>
<body>
    <div class="box1"></div>
    <div class="box2"></div>

    <div class="box3">
        <div class="box4"></div>
    </div>
</body>
</html>
```

<h3>默认样式</h3>
```HTML   
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <!-- 
        导入通用的去除默认样式css，这里没有提供
     -->
    <link rel="stylesheet" href=""> 
    <style>
        /* 
            默认样式:
                -通常情况下,浏览器都会为浏览器设置默认的样式
                -默认样式的存在会影响页面的布局
                    通常情况下编写页面时必须去除网页的默认样式(PC端)
        */

        body{
            margin: 0;
        }

        p{
            margin: 0;
        }

        ul{
            margin: 0;
            padding: 0;
            /* 去除项目符号 */
             list-style: none; 
         } 

        /* *{
            margin: 0;
            padding: 0;
        } */

        .box1{
            width: 100px;
            height: 100px;
            border: 1px solid black;
        }
    </style>
</head>
<body>
    <div class="box1"></div>

    <p>我是一个段落</p>
    <p>我是一个段落</p>
    <p>我是一个段落</p>
    <p>我是一个段落</p>

    <ul>
        <li>列表1</li>
        <li>列表2</li>
        <li>列表3</li>
    </ul>
</body>
</html>
```

<h3>盒子的尺寸</h3>
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
            width: 100px;
            height: 100px;
            background-color: #baf;
            padding: 10px;
            border: 10px red solid;
        
        /* 
            默认的情况下，盒子的可见框大小由内容区，内边距和边框共同决定

                box-sizing用来设置盒子尺寸的计算方式（设置width和height的作用）
                    可选值：
                        content-box 默认值，宽度和高度用来设置内容区的大小
                        border-box 宽度和高度用来设置整个盒子的大小
                            width和heigth指的是内容区和内边距和边框的总大小
        */
            box-sizing: border-box;
        }
    </style>
</head>
<body>
    <div class="box1"></div>
</body>
</html>
```

<h3>轮廓和圆角</h3>
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
           width: 200px;
           height: 200px;
           background-color: #bfa; 

           /* 
                box-shadow用来设置元素的阴影效果，阴影不会影响页面的布局
                第一个值 水平偏移量 设置阴影的水平位置 正值向右
                第二个值 垂直偏移量 设置阴影的垂直位置 正值向下
                第三个值 阴影的模糊半径
                第四个值 阴影的颜色
           */
           box-shadow: 10px 10px 36px rgba(0, 0, 0, .3);
            
           border: 10px red solid;
           /* outline: 10px red solid; */
           /* 
                outline用来设置元素的轮廓线，用法和border一样
                    轮廓和边框不同的点，就是轮廓不会影响可见框的大小
           */
        }
        
        .box1:hover{
            outline: 10px red solid;
        }
        
        .box2{
            width: 200px;
            height: 200px;
            background-color: #baf;
            border-radius: 50px  100px;
            /* 
                border-radius：用来设置圆角，圆角设置圆的半径
                
                border-top-left-radius: 50px 100px;
                border-top-right-radius:
                border-bottom-left-radius: 
                border-bottom-right-radius: 

                border-radius: 20px 50px;
                border-radius: 20px / 50px;
                两个是不一样的，第二个表示横向20 垂直50为半径的椭圆
            */
        }
    </style>
</head>
<body>
    <div class="box1"></div>
    <span>hello</span>
    <div class="box2"></div>
</body>
</html>
```

