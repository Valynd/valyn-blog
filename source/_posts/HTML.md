---
title: HTML回顾
date: 2022-09-17 17:43:31
tags: HTML
categories:
- Web前端
cover: https://pic1.zhimg.com/v2-077a594b1a64d55e95de392755a8aa76_r.jpg?source=172ae18b
---
<h3>超文本标记语言（英语：HyperText Markup Language，简称：HTML）是一种用于创建网页的标准标记语言。HTML是一种基础技术，常与CSS、JavaScript
一起被众多网站用于设计网页、网页应用程序以及移动应用程序的用户界面。网页浏览器可以读取HTML文件，并将其渲染成可视化网页。HTML描述了一个网站的结构
语义随着线索的呈现，使之成为一种标记语言而非编程语言。</h3>
<h3>HTML</h3>
```HTML   
<!DOCTYPE html>
<html lang="en">
<head>
    <!-- 
        meta元素为网页的源数据，一般提供给浏览器和搜索引擎使用
            -charset属性规定网页的编码格式
            -name属性结合content属性，为搜索引擎提供关键字
     -->
    <meta charset="UTF-8">
    <meta name="keywords" content="博客，学习，前端">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <!-- 
        tab键用于补全代码
            -!+tab 补全html模板
            -标签名+tab补全标签
        自结束标签
            <br>和<br/>都对
     -->
</body>
</html>
```
<h3>语义化标签</h3>
```HTML   
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <!-- 
        块元素（block element）
            -在网页中一般通过块元素对页面进行布局
        行内元素（inline element）
            -行内元素主要用来包裹文字
            -一般会在块元素内放行内元素，不会在行内元素放块元素
            -p元素中不能放任何的块元素
    -->
</body>
</html>
```
<h3>结构化语义标签</h3>
```HTML   
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
  <!--
    header 表示网页的头部
    main 表示网页的主体部分（一个网页只会有一个main）
    footer 表示网页的 底部
    nav 表示网页中的导航
    aside 和主体相关的其它内容（侧边栏）
    article 表示一个独立的文章
    section 表示一个独立的区块，上边的标签都不符合时使用

    div 没有语义，就表示一个区块
    span 行内元素，无任何含义
  -->
  <main></main>
  <footer></footer>
  <nav></nav>
  <aside></aside>
  <article></article>
  <section></section>
  <div></div>
  <span></span>
</html>
```
<h3>列表</h3>
```HTML   
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <!--
    列表：
        1.有序列表
        2.无序列表
        3.定义列表
            定义列表，使用dl标签来创建一个定义列表
                使用dt来表示定义的内容
                使用dd来表示对内容进行解释
        列表之间可以互相嵌套
    -->
    <ol>
        <li>结构</li>
        <li>样式</li>
        <li>行为</li>
    </ol>

    <ul>
        <li>结构</li>
        <li>样式</li>
        <li>行为</li> 
    </ul>

    <dl>
        <dt> 使用dt来表示定义的内容</dt>
        <dd>使用dd来表示对内容进行解释</dd>
    </dl>
</body>
</html>
```
<h3>超链接</h3>
```HTML   
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <!--
        超链接可以让我们从一个页面跳转到其它页面，
        或者当前页面的其它位置
        <a></a>
        a也是一个行内元素，可以嵌套除a以外任何元素
    -->
    <a href="https://valynd.github.io/valyn/">Valyn's blog</a>

    <!--
        可以是内部的页面地址（同一目录下）
        ./ 表示当前目录即文件所在目录
        ../ 表示上一级目录所在位置
    -->
    <a href="04列表.html">列表</a>
  
    <!--
        target属性，用来指定超链接打开的位置
            可选值：
                _self 默认值，在当前页面打开超链接
                _blank 打开一个新的页面
    -->
    <a href="04列表.html" target="_blank">跳转</a>

    <a href="#article04">跳转到文章04</a>

    <p id="article01">作家劉同說過一句話：「浮於表面都是風光，沈下心來自有答案。」

        層次越低，修為不夠，越是難以沈下心來提升自己，越喜歡張揚自己。
        
        毀掉一個人最快的方式，就是讓他得意忘形，活在自吹自擂的虛假世界里。
        
        明朝大才子唐伯虎，自幼聰慧，繪畫天賦非凡。得名師沈周指點後，繪畫技藝更是一日千里，超然於眾人。
        
        但師長的肯定，同行的贊譽，久而久之，唐伯虎內心難免生出驕矜淺薄之氣。
        
        他打心底里瞧不起同行的畫作，有時甚至連老師沈周的批評提點也不放在心上。
        
        唐伯虎卻不知道，自己當時的繪畫水平，離老師還有著天塹之別。
        
        繪畫是如此，連進京趕考也是極度驕傲自負。
        
        作為鄉試第一名的解元，本應前途似錦，但他因自視甚高，科考後口出狂言：「狀元一定會是我的！」
        
        最後，唐伯虎不僅和狀元失之交臂，還應牽扯到科考弊案被下了大獄。
        
        《道德經》早就有言：「自見者不明，自是者不彰。自伐者無功，自矜者不長。」
        
        意思是說，自以為是顯擺自己的人得不到彰顯；自我誇耀大言不慚的人得不到認同。
        
        修為不夠的人，被浮躁張揚裹挾，陶醉於自我優越感之中，止步不前，蹉跎了歲月，也辜負了自我。
        
        越是淺薄的人越愛張揚，越是不凡的人，越是謙遜低調。</p>

    <article id="article02">你人再好：不是每個人都會喜歡你，有人羨慕你，也有人討厭你，有人嫉妒你，也有人看不起你。

        生活就是這樣，你所做的一切不能讓每個人都滿意，不要為了討好別人而丟失自己的本性，因為每個人都有原則和自尊！
        
        鷹，不需鼓掌，也在飛翔；小草，沒人心疼，也在成長；深山的野花，沒人欣賞，也在芬芳。
        
        做事不需人人都理解，只需盡心盡力，做人不需人人都喜歡，只需坦坦蕩蕩。
        
        堅持，註定有孤獨徬徨，質疑嘲笑，也都無妨。
        
        山有山的高度，水有水的深度，沒必要攀比，每個人都有自己的長處。
        
        風有風的自由，雲有雲的溫柔，沒必要模仿，每個人都有自己的個性。
        
        人生1條路：走自己的路。
        
        人生2件寶：身體好、心不老。
        
        人生3好友：肯借錢給你、參加你的婚禮、參加你的葬禮。
        
        人生有4苦：看不透、捨不得、輸不起、放不下。
        
        人生5句話：再難也要堅持，再好也要淡泊，再差也要自信，再多也要節省，再冷也要熱情。
        
        人生6財富：身體、知識、夢想、信念、自信、骨氣。
        
        分享正面積極觀念，帶給您的朋友能量與溫暖。您的一個分享，可能就幫到有需要的朋友。</article>

    <article id="article03">出遠門時，為什麼要在冰箱裡放一枚硬幣。

        我曾經在一個德國人家做保姆，有一次我的雇主一家要回德國探親，他們要回德國，也給我放假了。走的第一天，我的德國雇主讓我端來一碗水，把那一碗水放在冰箱的冷凍庫裡面，等那一碗水凍成冰以後，放一枚硬幣在冰上面。
        
        我百思不得其解，又不敢問德國雇主，因為雇主她的中文不太好，我很少跟她交流。我也不管了，她放就放吧！然後他們一家三口就回德國了。
        
        一個月以後，他們從德國回來了，我就去他們家上班。
        
        上班之前，德國小姐讓我把冰箱裡所有的東西全部扔了。
        
        冰箱裡有牛肉，羊肉，排骨，雞肉，鴨肉，還有各種海鮮。這些東西放在冰箱冷凍庫一個月怎麼不能吃呢？
        
        我看到這些東西凍得好好的啊！
        
        我還是不敢找德國雇主說話，就把這些東西用一個塑膠袋裝起來，準備帶回家和鄰居們分享這些好東西。
        
        因為平時德國小姐也經常把一些快過期的東西給我，我經常把這些東西拿回家和鄰居們分享。
        
        我下班之前把這些東西裝好，然後拿回家了。我的鄰居老許一看我拿了這麼多好東西，非常開心，她知道這些東西我是吃不完的，會分一半給她。
        
        的確這些東西我是吃不完的，我把每一樣東西分了一半給老許，然後剩餘的放在自己冰箱的冷凍庫。因為天天要上班，也沒時間去做飯，那些東西暫時就放在那裡了。
        
        第二天，我上班之前，碰到老許，老許臉色不太好，我問她怎麼了？
        
        老許說她這兩天拉肚子，他們一家人都在拉肚子，老許問我拿回來的東西是不是壞的。
        
        我如實跟老許說那些東西是我們雇主讓我扔掉的，我捨不得扔，才拿回來的。
        
        老許讓我把那些東西都扔掉，那些東西已經壞了。
        
        我真的很奇怪，那些東西在冰箱裡凍得好好的，為什麼會壞呢？帶著這個疑問我繼續去德國小姐家上班。
        
        上班的時候，我繼續清理冰箱，看見那一碗冰還在冰箱裡面，那個硬幣不在上面了，我當時也沒有在意，就把那一碗冰拿出來化成冰水。
        
        冰化了，我去洗碗的時候，突然看見碗裡有一個硬幣，這不是當初放在冰上面的硬幣嗎？怎麼突然到了碗底了？
        
        我把這枚硬幣拿去還給德國小姐，然後德國小姐用她生硬的中文跟我說「這個硬幣在碗底嗎？」
        
        我對她說「是的。」
        
        德國小姐用英語對她老公說了一大堆話，我也不懂，然後我就去幹活了。
        
        後來男雇主來跟我說「那個硬幣在碗底，說明回德國那一段時間，家裡停電了，停電以後冰箱冷凍的東西壞了，來電以後這些東西又凍起來了，碗裡面的水也凍起來了，但是硬幣到了碗底。」
        
        男雇主問我那些東西有沒有扔，我只好對他說已經仍了，我不敢跟他說我拿回家了，老許還吃出問題來了。
        
        寫在最後：經過這次慘痛的教訓，我也學會了一個技巧，就是出遠門必須在冰箱裡面放一碗冰，然後上面放一個硬幣，如果硬幣沉到碗底，冰箱裡面的東西要全部扔掉。
        
        因為硬幣沉到碗底說明停電停了很長時間，整碗冰都化了。如果硬幣在碗中間，那麼這些食物有的還可以食用，說明停電沒有停多久，然後就來電了，冰只化了一半，這些食物可以食用。
        
        如果硬幣在冰上面，那就放心大膽地享受這些食物吧！說明從來沒有停過電。</article>
    
    <article id="article04">

        由於懶散，使得多數人的一生都庸庸碌碌，兩手空空。
        
        大凡有所作為的人，都是勤奮之人。人要想勤奮就要不斷地鞭策自己，努力去克服懶散的毛病。勤奮能塑造偉人，同時也能創造一個最好的自己。
        
        現代社會競爭激烈，你不前進，就會被別人超越。
        
        你懶惰一分鐘，就有可能錯失一筆大業務。
        
        不要為懶惰找藉口，不要說什麼路上堵車……那都是自欺欺人。
        
        華羅庚曾經寫過一首詩：「發白才知智叟呆，埋頭苦幹是第一。勤能補拙是良訓，一分辛苦一分才！」
        
        每一位熱愛生活的人，都有強勁的動力去克服懶惰。所以懶人們啊，別為自己的失敗找藉口了。
        
        關愛自己，從“戒懶”開始；拒絕失敗，從“戒懶”開始！</article>

    <!-- 
        将href属性的值设置为#，可以跳转至顶部
            <a href="#">回到顶部</a>
        跳转至指定位置需配合id属性使用
            <a href="#article04">跳转到文章04</a>       
    -->
    <a href="#">回到顶部</a>
</body>
</html>
```
<h3>图片</h3>
```HTML   
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <!-- 
        图片标签用于向外面引入一个外部图片
            使用img引入外部图片，img是一个自结束的标签
            img属于替换标签(块和行元素之间,具有两种元素的特点)
            属性:
                src:用于引入本地或外部的图片
                alt:
                    -图片的描述:默认情况不显示,有些浏览器在加载失败时会显示
                    -搜索引擎会根据alt的内容识别图片
                width 图片的宽度(单位是像素)
                height 图片的高度
                    图片的高度和宽度一个修改时,会等比例改变

     -->
     <img src="https://pic.qqtn.com/up/2019-9/15690311636958128.jpg" alt="学习">
     <img hight="" src="" alt="">
     <!-- 
        图片的格式：
            jepg（jpg）
                -支持的颜色比较丰富，不支持透明效果，不支持动图
                    一般用来显示图片
            gif
                -支持的颜色比较少，支持简单透明，支持动图
                -颜色单一的图片，动图
            png
                -支持的颜色丰富，支持复杂的透明，不支持动图
                -颜色丰富，复杂透明的图片（为网页而生）
            webp
                -谷歌新推出的专门用于网页的图片的一种格式
                -它具备其它格式的所有优点，且特别小
                -缺点：兼容性不好

            效果一样用小的
            效果不一样，用效果好的


      -->
</body>
</html>
```
<h3>内联框架</h3>
```HTML   
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <!-- 
        内联框架，用于向当前页面中引入一个其它的页面
            -src 指定要引入的网页的路径
            -frameborder 指定内联框架的边框
     -->
     <iframe src="https://valynd.github.io/valyn/" width="1000" height="600" frameborder="0"></iframe>
</body>
</html>
```
<h3>音视频</h3>
```HTML   
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <!-- 
        audio 引入一个外部的音频文件
            -音视频文件引入时，默认不允许用户自己控制播放停止
        属性：
            controls 是否允许用户控制播放
            autoplay 是否自动播放
     -->
     <audio src="" controls autoplay></audio>

    <!-- 
        除了通过src指定外部音频文件的路径外，还可以通过source来指定文件
    -->
      <audio src="">
        对不起，你的浏览器不支持播放音频，请升级浏览器！
        <source src="">
      </audio>

    <!-- 
        使用vedio引入一个视频，使用方法和audio一样
    -->
       <video src="" controls></video>
</body>
</html>
```
