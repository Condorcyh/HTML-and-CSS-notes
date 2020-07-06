# HTML&CSS笔记

本笔记取自网课[尚硅谷前端基础李立超2019版（含HTML、CSS、 HTML5、CSS3）](https://www.bilibili.com/video/av77217003)

整理：车一晗



[toc]





## 1 Introduce

### 1.1 test

+ lan 表示语言（en表示英文）
+ ！+ 回车：快速生成框架
+ ctrl + /   ：快速生成注释
+ p + Tab  ：自动补全

```html
<!DOCTYPE html>
<html lang="zh">  <!--lan表示语言，en表示英语-->
<!-- ! Tab  生成框架 -->
<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>
<body>
    <h1>Hello</h1>
    <p>hhh</p>
    <p>12345678</p>

    <!-- crtl+/  注释 -->
    <!-- p+Tab 自动补全 -->
    <p></p>
    <h1></h1>
</body>
</html>
```





### 1.2 实体（Entities）

+ 在网页中编写的多个空格在默认情况下会自动被浏览器解析为一个空格
+ 在html中，有时不能直接书写一些特殊符号，比如多个连续的空格、字符两侧的大于和小于号
+ 如果需要在网页中写出特殊符号，则需要使用html中的实体（转义字符）
+ 实体的语法：  &实体名;

```html
<!-- 实体 -->
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>实体</title>

    <!-- 
        1、在网页中编写的多个空格在默认情况下会自动被浏览器解析为一个空格
        2、在html中，有时不能直接书写一些特殊符号，比如多个连续的空格、字符
        两侧的大于和小于号
        3、如果需要在网页中写出特殊符号，则需要使用html中的实体（转义字符）
        4、实体的语法：
           &实体的名字;
              &nbsp;空格
              &gt;大于
              &lt;小于
              &copy;版权符号
     -->

     
    <p>
        今天&nbsp;天气真不错
    </p>

    <p>
        a&gt;b&lt;c
        &copy;
    </p>
</head>
<body>
    
</body>
</html>
```





### 1.3 meta标签

+ meta主要用于设置网页中的一些元数据，元数据不是给用户看的
  + charset  指定网页的字符集
  + name 指定的数据的名称
  + content 指定的数据的内容
    + keywords  表示网站的关键字，可以同时指定多个关键字，逗号隔开
    + description 用于指定网站的描述，显示在搜索引擎的搜索结果中
+ title标签的内容会作为搜索结果的超链接上的文字显示



```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <!-- 
        meta主要用于设置网页中的一些元数据，元数据不是给用户看的
            charset  指定网页的字符集
            name  指定的数据的名称
            content  指定的数据的内容
                keywords  表示网站的关键字，可以同时指定多个关键字，逗号隔开
                description  用于指定网站的描述，显示在搜索引擎的搜索结果中

                title标签的内容会作为搜索结果的超链接上的文字显示
     -->
    <meta name="keywords" content="HTML5,前端,CSS3">
    <meta name="description" content="这是一个非常不错的网站">
    <!-- 将页面重定向到另一个网站  content中的3表示时间，隔3秒跳转，跳转地址为百度 -->
    <meta http-equiv="refresh" content="3;url=https://www.baidu.com">
    
</head>
<body>
    
</body>
</html>
```





### 1.4 语义化标签

#### 1.4.1 标签

+ 在网页中，html负责网页的结构，所以在使用html标签的时候应该关注的是标签的语义，而不是它的样式
+ 标题标签：
  +  h1~h6 一共有6级标题
  +  从h1到h6重要性递减
  + h1重要性仅次于title标签，一般情况下**一个页面只有一个h1**
  + 一般情况下标题标签只会使用到h3，h4~h6很少用，当普通标签用
+ 块元素（block element）：在页面中==独占一行==的元素
+ p标签：表示页面中的一个段落
+ 标题标签、p标签都是==块元素==



#### 1.4.2 hgroup

+ hgroup用来将标题分组，将一组相关的标题同时放入一组



#### 1.4.3 行内元素

+ 行内元素（inline element）：在页面中不会独占一行的元素
+ em标签用于表示语音语调的加重 
+ strong标签表示强调重要的内容
+ blockquote表示一个长引用
+ q表示一个短引用，带引号
+ br标签表示换行



```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <!-- 
        在网页中，html负责网页的结构，所以在使用html标签的时候应该关注的是标签的语义，而不是它的样式

        标题标签：
            h1~h6  一共有6级标题
            从h1到h6重要性递减
            h1重要性仅次于title标签，一般情况下一个页面只有一个h1
            一般情况下标题标签只会使用到h3，h4~h6很少用，当普通标签用

        块元素（block element）：在页面中独占一行的元素

        p标签：表示页面中的一个段落

        标题标签，p标签都是块元素
     -->
    <h1>一级标题</h1>
    <h2>二级标题</h2>
    <h3>三级标题</h3>
    <h4>四级标题</h4>
    <h5>五级标题</h5>
    <h6>六级标题</h6>


    <p>在p标签中的内容就表示一个段落</p>

    <!-- hgroup用来将标题分组，将一组相关的标题同时放入一组 -->
    <hgroup>
        <h1>Calculus</h1>
        <h2>Introductions</h2>
    </hgroup>

    <!-- 
        行内元素（inline element）：在页面中不会独占一行的元素
        em标签用于表示语音语调的加重 
        strong标签表示强调重要的内容
        blockquote表示一个长引用
        q表示一个短引用，带引号
        br标签表示换行
    -->
    <p>今天天气<em>真</em>不错</p>
    <p>今天必须<strong>写完</strong>作业</p>
    鲁迅说：
    <blockquote>这句话我从没说过</blockquote>

    子曰：<q>学而时习之</q>
    <br>
    今天天气真不错


</body>

</html>
```



代码效果显示：

<img src="assert\1.4.PNG" alt="1.4" style="zoom:200%;" />

###  1.5 语义化标签2

+ 块元素（block element）:  在网页中通过块元素来进行==布局==
+ 行内元素（inline element）：主要用来==包裹文字==



​    一般情况下会==在块元素中放行内元素==，不会在行内元素中放块元素

​    块元素内基本什么都能放

​    p元素中不能放任何的块元素



+ 浏览器在解析网页时，会**自动**对网页中不符合规范的内容进行修正，比如：
  + 标签写在了根元素的外部
  + p元素中嵌套了块元素
  + 根元素中出现了除head和body以外的子元素





### 1.6 语义化标签3

+ 布局标签（结构化语义标签）
  + header表示网页的头部
  + main表示网页的主体部分(一个页面中只能有一个)
  + footer表示网页的底部
  + nav表示网页中的导航
  + aside表示和主体相关的其他内容（侧边栏）
  + article表示一个独立的文章
  + section表示一个独立的区块，即上面的标签都不能表示的情况
  + div：没有语义，表示一个区块，目前来讲div还是主要的布局元素，==万物皆可div==
  + span是一个行内元素，没有任何语义，一般用于在网页中选中文字



```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>
<body>
    <!-- 
    布局标签（结构化语义标签）
     -->
    
     <header></header>
    
     <main></main>
    
     <nav></nav>
    
     <aside></aside>
    
     <article></article>
    
     <section></section>
    
     <div></div>
    
     <span></span>
</body>
</html>
```





### 1.7 列表

+ 列表（list）
+ 在html中也可以创建列表，html分为三种：有序列表、无序列表、定义列表
  + 无序列表：使用ul标签来创建，用li表示列表项（==用的最多==）
  + 有序列表：使用ol标签来创建，用li表示列表项
  + 定义列表：使用dl标签来创建，用dt表示定义的内容，用dd对内容进行解释
+ 列表之间可以互相嵌套



```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <!-- 
        列表（list）
            1、铅笔
            2、橡皮
            3、尺子

        在html中也可以创建列表，html分为三种：
            1、有序列表
            2、无序列表
            3、定义列表

        无序列表：使用ul标签来创建，用li表示列表项，用的最多
        有序列表：使用ol标签来创建，用li表示列表项
        定义列表：使用dl标签来创建，用dt表示定义的内容，用dd对内容进行解释

        列表之间可以互相嵌套

     -->

    <ul>
        <li>结构</li>
        <li>表现</li>
        <li>行为</li>
    </ul>

    <ol>
        <li>结构</li>
        <li>表现</li>
        <li>行为</li>
    </ol>

    <dl>
        <dt>结构</dt>
        <dd>表示网页的结构，规定网页中哪些是标题，哪些是段落</dd>
    </dl>

    <ul>
        <li>
            A
            <ul>
                <li>a</li>
                <li>b</li>
            </ul>
        </li>
    </ul>

</body>

</html>
```



代码效果显示：

<img src="assert\1.7.PNG" alt="1.7" style="zoom:200%;" />

### 1.8 超链接

+ 超链接可以从一个页面跳转到其他页面或者当前页面的指定位置
+ 使用==a标签==来定义超链接
+ 属性：
  + href：指定跳转的目标路径，值可以是一个外部网站的地址，也可以是一个内部页面的地址
+ 超链接是一个行内元素，在a标签中可以嵌套除自身外的任何元素



```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>超链接</title>
</head>
<body>

    <a href="https://www.baidu.com">超链接1</a>
    <br><br>
    <a href="https://www.apple.com">超链接2</a>
    <br><br>
    <a href="07列表.html">超链接3</a>
</body>
</html>
```





### 1.9 相对路径

+ 当需要跳转到一个服务器内部的页面时，一般使用相对路径
+ 相对路径都是用./或者../开头
  + ./可以不写，如果不写./，也不写../，就相当于写了./
+ ./表示当前文件所在的目录
  + 在这里当前页面就是 09相对路径.html
  + ./就等于 09相对路径.html所在的目录，即path
+ ../表示当前文件所在目录的上一级目录



```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>
<body>
    <a href="../07列表.html">超链接1</a>
    <br><br>
    <a href="./inner/target.html">超链接2</a>
    <br><br>
    <a href="../outer/target2.html">超链接3</a>
</body>
</html>
```





### 1.10 超链接2

+ target属性，用来指定超链接打开的位置
+ 可选值：
  + self：默认值，在当前页面中打开超链接
  + blank：在新的页面中打开
+ 在开发中，可以将#或者javascript:;作为herf的属性使用，达到==先占用==的目的
+ 将href属性设置为#后，点击超链接页面会转到当前页面的顶部，也可以跳转到页面的指定位置，只需将herf的属性设置为：#目标元素的id属性值 
+ id属性：唯一不重复
  + 每一个标签都能添加id属性
  + 同一个页面中不能出现重复id属性



```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>
<body>
    <!-- 
        target属性，用来指定超链接打开的位置
            可选值：
                -self：默认值，在当前页面中打开超链接
                -blank:在新的页面中打开
    -->

    
    <a href="07列表.html" target="_self">超链接1</a>  
    <br><br>
    <a href="07列表.html" target="_blank">超链接2</a>  
    <br><br>
    <a href="#bottom">去底部</a>
    <br><br>
    <a href="#p3">去第三个自然段</a>
    <br><br>
    <!-- 在开发中，可以将#作为超链接的路径的占位符使用 -->
    <a href="#">超链接占位符</a>
    <br><br>
    <!-- 可以使用javascript:;来作为herf的属性，此时点击这个超链接什么也不会发生 -->
    <a href="javascript:;">无用超链接</a>

    <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quam deserunt ex eius temporibus excepturi eligendi accusantium, ducimus, saepe obcaecati quasi delectus reiciendis molestias earum perferendis minus voluptatem vitae. Dignissimos, provident.</p>
    <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quam deserunt ex eius temporibus excepturi eligendi accusantium, ducimus, saepe obcaecati quasi delectus reiciendis molestias earum perferendis minus voluptatem vitae. Dignissimos, provident.</p>
    <p id="p3">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quam deserunt ex eius temporibus excepturi eligendi accusantium, ducimus, saepe obcaecati quasi delectus reiciendis molestias earum perferendis minus voluptatem vitae. Dignissimos, provident.</p>
    <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quam deserunt ex eius temporibus excepturi eligendi accusantium, ducimus, saepe obcaecati quasi delectus reiciendis molestias earum perferendis minus voluptatem vitae. Dignissimos, provident.</p>
    <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quam deserunt ex eius temporibus excepturi eligendi accusantium, ducimus, saepe obcaecati quasi delectus reiciendis molestias earum perferendis minus voluptatem vitae. Dignissimos, provident.</p>
    <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quam deserunt ex eius temporibus excepturi eligendi accusantium, ducimus, saepe obcaecati quasi delectus reiciendis molestias earum perferendis minus voluptatem vitae. Dignissimos, provident.</p>
    <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quam deserunt ex eius temporibus excepturi eligendi accusantium, ducimus, saepe obcaecati quasi delectus reiciendis molestias earum perferendis minus voluptatem vitae. Dignissimos, provident.</p>
    <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quam deserunt ex eius temporibus excepturi eligendi accusantium, ducimus, saepe obcaecati quasi delectus reiciendis molestias earum perferendis minus voluptatem vitae. Dignissimos, provident.</p>
    <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quam deserunt ex eius temporibus excepturi eligendi accusantium, ducimus, saepe obcaecati quasi delectus reiciendis molestias earum perferendis minus voluptatem vitae. Dignissimos, provident.</p>
    <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quam deserunt ex eius temporibus excepturi eligendi accusantium, ducimus, saepe obcaecati quasi delectus reiciendis molestias earum perferendis minus voluptatem vitae. Dignissimos, provident.</p>
    <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quam deserunt ex eius temporibus excepturi eligendi accusantium, ducimus, saepe obcaecati quasi delectus reiciendis molestias earum perferendis minus voluptatem vitae. Dignissimos, provident.</p>
    <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quam deserunt ex eius temporibus excepturi eligendi accusantium, ducimus, saepe obcaecati quasi delectus reiciendis molestias earum perferendis minus voluptatem vitae. Dignissimos, provident.</p>
    <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quam deserunt ex eius temporibus excepturi eligendi accusantium, ducimus, saepe obcaecati quasi delectus reiciendis molestias earum perferendis minus voluptatem vitae. Dignissimos, provident.</p>

    <!-- 
        可以直接将超链接的href属性设置为#，这样点击超链接后页面会转到当前页面的顶部
        也可以跳转到页面的指定位置，只需将herf的属性设置为：#目标元素的id属性值 

        id属性：唯一不重复
            -每一个标签都能添加id属性
            -同一个页面中不能出现重复id属性
    -->
    <a id="bottom" href="#">回到顶部</a>

</body>
</html>
```





### 1.11 图片标签

+ 图片标签用于向当前页面中引入一个外部图片

+ img标签，它是一个**自结束标签**

  + src指定外部图片的路径，路径规则和超链接相同
  + alt是对图片的描述，默认情况下不会显示，有些浏览器会在图片无法加载时显示，搜索引擎会根据alt的内容来识别图片。不写的话，图片就不会被搜索引擎找到
  + width：图片的宽度(单位：像素)
  + height：图片的高度（单位：像素）
    + ==如果宽度和高度中只修改一个，另一个会等比例缩放==
  + **注意**：一般情况下在pc端不建议修改图片的大小，需要多大图片就裁多大，但是在移动端，经常需要对图片进行缩放（大图缩小）
  +  img属于有替换元素（基于行内和块元素之间，具有两种元素的共同特点）

+ 图片的格式

  + jpg：支持颜色比较丰富，不支持透明效果和动图，一般表示照片

  + gif：支持颜色较少，支持简单透明和动图，表示颜色单一的图片和动图

  + png：颜色丰富，复杂透明，不支持动图，专为网页

  + webp：谷歌新推出的专门用来表示网页中的图片的一种格式，具备了其他图片格式所有优点，而且文件还很小，缺点是兼容性差

  + base64：将图片用base64进行编码，这样可以直接将图片转换成字符，通过字符的形式来引入图片，一般都是一些需要和网页一起加载的图片才会使用base64

    **效果一样用小的，加载速度快**

    **效果不一样用效果好的**





```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>
<body>
    <img height="200" src="./pictures/logo.JPG" alt="小黄人">
    <br><br>
    <!-- 其他网站的图，不建议使用，容易引发版权问题 -->
    <img width="500" src="https://www.sciencealert.com/images/2019-12/processed/CatsHaveFacialExpressionsButHardToRead_600.jpg" alt="猫">
</body>
</html>
```



代码效果显示：

<img src="assert\1.11.PNG" alt="1.11" style="zoom:200%;" />





### 1.12 内联框架

+ 内联框架：用于向当前页面中引入其他页面
  + src指定要引入的网页的路径
  + frameborder：指定内联框架的边框，0表示无，1表示有



```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>
<body>
     <iframe src="https://www.qq.com" width="800" height="600" frameborder="0"></iframe>
</body>
</html>
```



代码效果显示：

<img src="assert\1.12.PNG" alt="1.12" style="zoom:200%;" />





### 1.13 音视频播放

+ audio标签：用来向页面中引入外部音频文件
  + 音视频引入时默认情况下==不允许==用户自己控制播放和停止
  + 属性：
    + controls：是否允许用户自动播放，不需要给值
    + autoplay：音频文件是否自动播放(太魔性了)
      + 如果设置了autoplay，则音乐在网页打开时会自动播放
      + 目前来讲大部分浏览器不会自动对音乐进行播放
    + loop：循环播放
  +  除了通过src指定外部文件的路径外，还可以通过source标签来指定文件
    + 可以在最前面加上报错文字，支持的浏览器会忽略，不支持的会显示
    + 可以同时指定多个文件，优先使用第一个，不能用则顺延
    + 可以有效解决各种不兼容的情况
+ embed标签：老版本的浏览器引入音视频 
  + 缺点：自动播放，禁不掉
+ video标签
  + 使用video标签向网页中引入视频文件，跟audio差不多



```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>
<body>
    <!-- 
        audio标签：用来向页面中引入外部音频文件
        音视频引入时默认情况下不允许用户自己控制播放和停止

        属性：
            controls：是否允许用户自动播放，不需要给值
            autoplay：音频文件是否自动播放(太魔性了)
                -如果设置了autoplay，则音乐在打开时会自动播放
                -目前来讲大部分浏览器不会自动对音乐进行播放
            loop：循环播放
     -->
    <audio src="./source/EXO (엑소) - Love Shot.mp3" controls></audio>
    <br><br>
    <!-- 除了通过src指定外部文件的路径外，还可以通过source来指定文件 -->
    <!-- 支持的浏览器会忽略，不支持的会显示错误文字 -->
    <!-- 可以同时指定多个文件，优先使用第一个，不能用则顺延 -->
    <!-- 可以有效解决各种不兼容的情况 -->
    <audio controls>
        播放错误
        <source src="./source/MIC Drop (Steve Aoki Remix).mp3">
    </audio>

    <!-- 老版本的浏览器引入音视频 -->
    <!-- 缺点：自动播放，禁不掉 -->
    <embed src="" type="" width="" height="">

    <!-- 使用video标签向网页中引入视频文件，跟audio差不多 -->
    <video src=""></video>

    <iframe frameborder="0" src="https://v.qq.com/txp/iframe/player.html?vid=i0032qxbi2v" allowFullScreen="true" width="500" height="300"></iframe>
</body>
</html>
```



代码效果显示：

<img src="assert\1.13.PNG" alt="1.13" style="zoom:200%;" />

## 2 CSS

### 2.1 CSS简介

+ 网页分成三个部分：结构（HTML）、表现（CSS）、行为（JavaScript）
+ CSS：
  + 层叠样式表
  + 网页实际上是一个多层的结构，通过CSS可以分别为网页的每一层设计样式，而最终我们看到的只是网页的最上面一层
  + 总的来说，CSS可以用来设置网页中元素的样式
+ 使用CSS来修改文字的样式
  + 第一种方案：内联样式（行内样式）—开发不推荐使用
    + 在标签内部通过style属性来设置元素的样式 
    + 问题：使用内联样式，样式只能在一个标签内生效。如果希望影响到多个元素要一个一个修改，并且当样式发生变化时要一个一个修改
  + 第二种方案：内部样式表
    + 将样式编写到head中的style标签里，然后通过CSS的选择器来选中元素并为其设置各种样式
    + 可以同时为多个标签设置样式，并且修改时只需要修改一处即可全部应用
    + 优点：内部样式表更加方便对样式进行复用
    + 问题：内部样式表只能对一个网页起作用，即里面的样式不能跨页面进行复用
  + 第三种方案：外部样式表（==推荐使用==）
    + 可以将CSS样式编写到一个外部的CSS文件中，然后通过==link标签==来引入外部的CSS文件
    + 优点：外部样式表需要通过link标签进行引入，意味着只要想使用这些样式的网页都可以对其进行引用，使样式可以在不同页面之间进行复用，将样式编写到外部的CSS文件中，可以使用到浏览器的缓存机制，从而**加快网页的加载速度**



```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>

    <!-- 
        第二种方案：内部样式表
                   将样式编写到head中的style标签里，然后通过CSS的选择器来选中元素并为其设置各种样式
                   可以同时为多个标签设置样式，并且修改时只需要修改一处即可全部应用
        优点：内部样式表更加方便对样式进行复用
        问题：内部样式表只能对一个网页起作用，即里面的样式不能跨页面进行复用
    -->

    <style>
        p {
            color: green;
            font-size: 20px;
        }
    </style>

    <!-- 
        第三种方案：外部样式表（推荐使用）
                   可以将CSS样式编写到一个外部的CSS文件中，然后通过link标签来引入外部的CSS文件
        优点：外部样式表需要通过link标签进行引入，意味着只要想使用这些样式的网页都可以对其进行引用，使样式可以在不同页面之间进行复用
             将样式编写到外部的CSS文件中，可以使用到浏览器的缓存机制，从而加快网页的加载速度

     -->
     <link rel="stylesheet" href="./style.css">
</head>

<body>
    <!-- 
        网页分成三个部分：
            结构（HTML）
            表现（CSS）
            行为（JavaScript）
        CSS
            -层叠样式表
            -网页实际上是一个多层的结构，通过CSS可以分别为网页的每一层设计样式
             而最终我们看到的只是网页的最上面一层
            -总的来说，CSS可以用来设置网页中元素的样式
    -->

    <!-- 
        使用CSS来修改文字的样式
        第一种方案：内联样式（行内样式）——开发不推荐使用
                   在标签内部通过style属性来设置元素的样式 
        问题：使用内联样式，样式只能在一个标签内生效。如果希望影响到多个元素要一个一个修改，
              并且当样式发生变化时要一个一个修改
    -->
    <p style="color: red;font-size: 30px;">少小离家老大回，乡音无改鬓毛衰</p>
    <p>少小离家老大回，乡音无改鬓毛衰</p>
    <p>少小离家老大回，乡音无改鬓毛衰</p>
</body>

</html>
```



style.css：

```css
p{
    color: tomato;
    font-size: 20px;
}
```





代码效果显示：

<img src="assert\2.1.PNG" alt="2.1" style="zoom:200%;" />

### 2.2 CSS语法

+ 基本语法：选择器、声明块
  + 选择器：通过选择器可以选中页面中的指定元素
    + 比如p的作用就是选中页面中**所有的**p元素
  + 声明块：通过声明块来指定要为元素设置的样式
    + 声明块由一个一个声明组成
    + 声明是一个名值对结构（一个样式名对应一个样式值，名和值之间以冒号连接，分号结尾）
+ CSS的注释：  /* 这是注释 */



```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        /* 
        这边就不属于html了，现在是CSS的注释
        */

        p{
            color: red;
            font-size: 30px;

        }

        h1{
            color: green;
        }
    </style>
</head>
<body>
    <h1>哈哈</h1>
    <p>今天天气不错</p>
</body>
</html>
```





### 2.3 常用选择器

+ 元素选择器
  + 作用：根据标签名选中指定的元素
  + 语法：标签名{}
  + 例子：p{} h1{} div{}
+ id选择器
  + 作用：根据元素的id属性值选中一个元素
  + 语法：#id属性值{}
  + 例子：#box{} #red{}
+ 类选择器
  + 作用：根据元素的class属性值选中一组元素
  + 语法：.class属性值{}
+ 通配选择器
  + 作用：选中页面中的所有元素
  + 语法：*{}
+ class 是标签的一个属性，和id类似，不同的是class可以重复使用，可以通过class属性为元素分组，也可以同时为一个元素指定多个class，多个class用空格隔开





```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        /* 
        将所有的段落设置为红色

        元素选择器
            作用：根据标签名选中指定的元素
            语法：标签名{}
            例子：p{}  h1{}  div{}
        */
        
        p{
            color: red;
        }
        h1{
            color: green;
        }
       

        /* 
        将第三段设为红色

        id选择器
            作用：根据元素的id属性值选中一个元素
            语法：#id属性值{}
            例子：#box{}  #red{}
        */
            
        #red{
            color: red;
        } 

        /* 
        将最后两行设为蓝色

        类选择器
            作用：根据元素的class属性值选中一组元素
            语法：.class属性值{}

        */
        
        .blue{
            color: blue;
        }
        .abc{
            font-size: 30px;
        }
       

        /* 
        通配选择器
            作用：选中页面中的所有元素
            语法：*{}

        */
        *{
            color: red;
        }
        

    </style>
</head>
<body>
    <h1>标题</h1>
    <p>少小离家老大回</p>
    <p>少小离家老大回</p>
    <p id="red">少小离家老大回</p>
    <p>少小离家老大回</p>
    <p class="blue abc">少小离家老大回</p>
    <p class="blue">少小离家老大回</p>

    <!-- 
        class 是标签的一个属性，和id类似，不同的是class可以重复使用
        可以通过class属性为元素分组
        可以同时为一个元素指定多个class，多个class用空格隔开
     -->

</body>
</html>
```



代码效果显示：

<img src="assert\2.3.PNG" alt="2.3" style="zoom:200%;" />



### 2.4 复合选择器

+ 交集选择器
  + 作用：选中同时符合多个条件的元素
  + 语法：选择器1.选择器2...选择器n{}，用.连接
  + 注意：交集选择器中如果有元素选择器，必须以元素选择器开头
+ 并集选择器（选择器分组）
  + 作用：同时选择多个选择器对应的元素
  + 语法：选择器1,选择器2,选择器3,选择器n{}，用，连接



```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        /* 将class为red的元素设为红色 */
        .red{
            color: red;
        }

        /* 
            交集选择器
                作用：选中同时符合多个条件的元素
                语法：选择器1选择器2...选择器n{}，用.连接
                注意：交集选择器中如果有元素选择器，必须以元素选择器开头
        */

        /* 将class为red的div元素字体大小设置为30px */
        div.red{
            font-size: 30px;
        }
        .a.b.c{
            color: green;
        }

        /* 
            选择器分组（并集选择器） 
                作用：同时选择多个选择器对应的元素
                语法：选择器1,选择器2,选择器3,选择器n{}
        */
        h1,span{
            color: blue;
        }
    </style>
</head>
<body>
    <div class="red">我是div</div>

    <p class="red">我是p元素</p>
    <p class="red2 a b c">我是p元素2</p>

    <h1>标题</h1>
    <span>哈哈哈</span>
</body>
</html>
```



代码效果显示：

<img src="assert\2.4.PNG" alt="2.4" style="zoom:200%;" />

### 2.5 关系选择器

+ 元素分类：
  + 父元素：直接包含子元素的元素
  + 子元素：直接被父元素包含的元素
  + 祖先元素：直接或间接包含后代元素的元素
    + 一个元素的父元素也是它的祖先元素
  + 后代元素：直接或间接被祖先元素包含的元素
    + 一个元素的子元素也是它的后代元素
  + 兄弟元素：拥有相同父元素的元素
+ 子元素选择器：
  + 作用：选中指定父元素的指定子元素
  + 语法：父元素>子元素
+ 后代元素选择器：
  + 作用：选中指定元素内的指定后代元素
  + 语法：祖先 后代
+ 下一个兄弟选择器(选择离最近的下一个兄弟，要是不紧挨着就无效)：
  + 语法：前一个+下一个
+ 选择下面所有的兄弟
  + 语法：兄~弟



```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        /* 
        为div的子元素span设置一个字体颜色红色
        （为div直接包含的span设置一个字体颜色）

        子元素选择器
            作用：选中指定父元素的指定子元素
            语法：父元素>子元素
        */

        
        div.box>span{
            color: orange;
        }
       

        /* 
        后代元素选择器
            作用：选中指定元素内的指定后代元素
            语法：祖先 后代
        */
        
        div span{
            color: blue;
        }
       

        /* 子元素的子元素 */
        
        div>p>span{
            color: red;
        }
       

        /* 
        下一个兄弟选择器(选择离最近的下一个兄弟，要是不紧挨着就无效)
            语法：前一个+下一个
        */
        p+span{
            color: red;
        }

        /* 
        选择下面所有的兄弟
            语法：兄~弟
        */
        p~span{
            color: red;
        }
    </style>
</head>
<body>
    <!-- 
        父元素
            -直接包含子元素的元素
        子元素
            -直接被父元素包含的元素
        祖先元素
            -直接或间接包含后代元素的元素
            -一个元素的父元素也是它的祖先元素
        后代元素
            -直接或间接被祖先元素包含的元素
            -一个元素的子元素也是它的后代元素
        兄弟元素
            -拥有相同父元素的元素
     -->
    
    <div class="box">
        我是div
        <p>
            我是div中的p元素
            <span>我是p元素中的span</span>
        </p>
        <div></div>
        <span>我是div中的span元素</span>
        <span>我是div中的span元素</span>
    </div>

    <br><br>

    <span>我是div外的span</span>

    <br><br>

    <div>
            我是div
            <p>
                我是div中的p元素
                <span>我是p元素中的span</span>
            </p>
            <span>我是div中的span元素</span>
        </div>
    
        <span>我是div外的span</span>

</body>
</html>
```



代码效果显示：

<img src="assert\2.5.PNG" alt="2.5" style="zoom:200%;" />

### 2.6 属性选择器

+ [属性名]选择含有指定属性的元素
+ [属性名=属性值]选择含有指定属性和属性值的元素
+ [属性名^=属性值]选择属性值以属性值开头的元素
+ [属性名$=属性值]选择属性值以属性值开头的元素
+ [属性名*=属性值]选择属性值含有属性值的元素



```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>

    <!-- 
        [属性名]选择含有指定属性的元素
        [属性名=属性值]选择含有指定属性和属性值的元素
        [属性名^=属性值]选择属性值以属性值开头的元素
        [属性名$=属性值]选择属性值以属性值开头的元素
        [属性名*=属性值]选择属性值含有属性值的元素
     -->
    <style>
        p[title$=abc]{
            color: red;
        }
    </style>
</head>
<body>
    <h1>标题</h1>
    <p title="abc">一二三四五</p>
    <p title="abcdef">一二三四五</p>
    <p title="helloabc">一二三四五</p>
    <p>一二三四五</p>
</body>
</html>
```



代码效果显示：

<img src="assert\2.6.PNG" alt="2.6" style="zoom:200%;" />

### 2.7 伪类选择器

+ 伪类（不存在的类，特殊的类）:
  + 用来==描述一个元素的特殊状态==，比如：第一个子元素，被点击的元素，鼠标移入的元素
  + 一般情况下都是":"开头
    + :first-child 第一个子元素
    + :last-child 最后一个子元素
    + :nth-child(n) 第n个子元素
    + 特殊值：
      + n                       选中所有元素
      + 2n或even         选中偶数位元素 
      + 2n+1或odd      选中奇数位元素
    + 以上伪类都是根据所有的子元素进行排序的
    + 其他伪类：
      + :first-of-type
      + :last-of-type
      + :nth--of-type()
      + 这几个功能和上述类似，不同的是它们是在同类型元素中进行排序
  + :not() 否定伪类
    + 将符合条件的元素从选择器中去除



```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>

    <style>
        /* 
        将ul里的第一个li设置为红色，自动选中第一个
        */

        /* 
            伪类（不存在的类，特殊的类）
                -用来描述一个元素的特殊状态
                    比如：第一个子元素，被点击的元素，鼠标移入的元素
                -一般情况下都是":"开头
                    :first-child  第一个子元素
                    :last-child  最后一个子元素
                    :nth-child(n)  第n个子元素
                        特殊值：
                            n          选中所有元素
                            2n或even   选中偶数位元素 
                            2n+1或odd  选中奇数位元素
                    以上伪类都是根据所有的子元素进行排序的
                    :first-of-type
                    :last-of-type
                    :nth--of-type()
                        -这几个功能和上述类似，不同的是它们是在同类型元素中进行排序
                - :not() 否定伪类
                    -将符合条件的元素从选择器中去除
        */

        
        ul > li:first-child {
            color: red;
        }

        ul > li:last-child{
            color: red;
        }

        ul > li:nth-child(2n){
            color: red;
        }
       

        /* 要是first-child不是li，这个就无效了   应该用:first-of-type */
        
        ul > li:first-child{
            color: red;
        }
       

        /* 注意下面两个的区别 */
        ul > li:not(:nth-child(3)){
            color: yellowgreen;
        }
        ul > li:not(:nth-of-type(3)){
            color: yellowgreen;
        }


    </style>
</head>

<body>
    <ul>
        <span>我是一个span</span>
        <li>第一个</li>
        <li>第二个</li>
        <li>第三个</li>
        <li>第四个</li>
        <li>第五个</li>
    </ul>
</body>

</html>
```



代码效果显示：

<img src="assert\2.7.PNG" alt="2.7" style="zoom:200%;" />





### 2.8 a元素的伪类

+ :link用来表示没访问过的链接（正常的链接） 
+ :visited表示访问过的链接
  + 由于隐私的原因，所以visited这个伪类只能修改链接的颜色
+ :hover 表示鼠标移入的状态
+ :active 表示鼠标点击的状态



```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
    <style>
        /* 
        :link用来表示没访问过的链接（正常的链接） 
        */
        a:link{
            color: red;
        }

        /* 
        :visited表示访问过的链接

        由于隐私的原因，所以visited这个伪类只能修改链接的颜色
        */
        a:visited{
            color: orange;
        }

        /* 
        :hover 表示鼠标移入的状态
        */
        a:hover{
            color: yellowgreen;
        }

        /* 
        :active 表示鼠标点击的状态
        */
        a:active{
            color: purple;
        }
    </style>
</head>
<body>
    <!-- 
        1、没有访问过的链接
        2、访问过的链接
     -->
    <a href="https://www.baidu.com">Baidu</a>
    <br><br>
    <a href="https://www.baidu123.com">Baidu</a>
</body>
</html>
```





### 2.9 伪元素选择器

+ 伪元素：表示页面中一些==特殊的并不真实存在的元素==（特殊的位置）
+ 使用"::"开头

​        ::first-letter 表示第一个字母

​        ::first-line 表示第一行

​        ::selection 表示选中的内容

​        ::before 表示元素的开始位置

​        ::after 表示元素的最后位置

+ before和after必须结合content属性来使用



```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>

    <style>
        p{
            font-size: 20px;
        }

        p::first-letter{
            font-size: 50px;
        }

        p::first-line{
            background-color: yellow;
        }

        p::selection{
            background-color: green;
        }

        div::before{
            content:"abc";
            color: red;
        }

        div::after{
            content:"hhh";
            color: gold;
        }

        /* 
            伪元素：表示页面中一些特殊的并不真实存在的元素（特殊的位置）
                使用"::"开头

                ::first-letter  表示第一个字母
                ::first-line  表示第一行
                ::selection  表示选中的内容
                ::before  表示元素的开始位置
                ::after  表示元素的最后位置
                    before和after必须结合content属性来使用
        */
    </style>

</head>
<body>

    <div>hello</div>

    <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Exercitationem harum veniam doloremque! Magnam similique consectetur, id, dolore dignissimos dolorem blanditiis distinctio ullam ducimus alias unde aspernatur odit reiciendis quibusdam. Repudiandae.
    </p>
</body>
</html>
```



代码效果显示：

<img src="assert\2.9.PNG" alt="2.9" style="zoom:200%;" />



### 2.10 样式的继承

+ 样式的继承：为一个元素设置的样式也会应用到其后代的元素上
+ 继承是发生在祖先和后代之间的
+ 继承的设计是为了方便开发，利用继承可以将一些通用的样式统一设置到共同的祖先元素上，这样只需设置一次即可让所有的元素都具有该样式
+ **注意**：并不是所有的样式都会被继承
  + 比如：背景相关，布局相关等的这些样式都不会被继承



```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
    <style>
        /* 
            样式的继承：为一个元素设置的样式也会应用到其后代的元素上
            继承是发生在祖先和后代之间的

            继承的设计是为了方便开发，利用继承可以将一些通用的样式统一设置到共同的祖先元素上，这样只需设置一次即可让所有的元素都具有该样式

            注意：并不是所有的样式都会被继承
                比如：背景相关，布局相关等的这些样式都不会被继承
        */

        p{
            color: red;
        }

        div{
            color: green;
        }
    </style>
</head>
<body>
    <p>
        我是一个p元素
        <span>我是p元素中的span</span>
    </p>

    <span>我是p元素外的span元素</span>

    <div>
        我是div
        <span>
            我是div中的span
            <em>我是span中的em</em>
        </span>
    </div>
</body>
</html>
```



代码效果显示：

<img src="assert\2.10.PNG" alt="2.10" style="zoom:200%;" />

### 2.11 选择器的权重

+ 样式的冲突：通过不同的选择器选中相同的元素，并且为相同的样式设置不同的值，此时就发生了样式的冲突

+ 发生样式冲突时，用哪个样式由==选择器的权重（优先级）==决定

+ 选择器的权重：

  ​        内联样式：            1,0,0,0

  ​        id选择器：             0,1,0,0

  ​        类和伪类选择器： 0,0,1,0

  ​        元素选择器：         0,0,0,1

  ​        通配选择器：         0,0,0,0

  ​        继承的样式：没有优先级

  ​        **优先级越高的越先显示**

+ 比较优先级时，需要将所有选择器的优先级进行==相加计算==，最后优先级越高，则越优先显示，分组选择器单独计算
+ 选择器的累加不会超过其最大的数量级，比如类选择器再高也不会超过id选择器
+ 如果优先级计算后相同，此时则==优先使用靠下的样式==
+ 可以在某一个样式的后面添加==!important==，则此时该样式会得到最高优先级
+ **注意**：在开发中慎用



```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
    <style>
        div{
            color: red;
        }

        .red{
            color: green;
        }

        #box1{
            color: orange;
        }

        .red{
            background-color: yellowgreen !important;
        }
        .d1{
            background-color: purple;
        }

        *{
            font-size: 50px;
        }

        div{
            font-size: 20px;
        }

    </style>
</head>
<body>
    <div id="box1" class="red d1">我是一个div <span>我是div中的span</span></div>
</body>
</html>
```



代码效果显示：

<img src="assert\2.11.PNG" alt="2.11" style="zoom:200%;" />



### 2.12 单位

+ 长度单位：
  + 像素：
    + 屏幕（显示器）实际上是由一个一个发光的点构成
    + 不同屏幕的像素大小不一样，==像素越小的屏幕效果越清晰==
    + 同样的200px在不同的设备下显示效果不一样
  + 百分比
    + 可以将属性值设置为相对于其父元素属性的百分比
    + 可以使子元素==跟随父元素的改变而改变==
  + em
    + 相对于元素的字体大小计算的
    + 1em = 1 font-size，一般默认一个字体大小为16px
    + em会根据字体大小的改变而改变
  + rem
    + root
    + 相对于根元素的字体大小来计算



```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
    <style>

        html{
            font-size: 5px;
        }
        .box1{
            /* 
                长度单位：
                    像素
                        -屏幕（显示器）实际上是由一个一个发光的点构成
                        -不同屏幕的像素大小不一样，像素越小的屏幕效果越清晰
                        -同样的200px在不同的设备下显示效果不一样
                    百分比
                        -可以将属性值设置为相对于其父元素属性的百分比
                        -可以使子元素跟随父元素的改变而改变
                    em
                        -相对于元素的字体大小计算的
                        - 1em = 1 font-size，一般默认一个字体大小为16px
                        -em会根据字体大小的改变而改变
                    rem
                        -root
                        -相对于根元素的字体大小来计算
            */

            width: 200px;
            height: 200px;
            background-color: orange;
        }

        .box2{
            width: 50%;   
            height: 50%;
            background-color: aqua;
        }

        .box3{
            font-size: 20px;
            /* width: 10em;
            height: 10em; */
            width: 10rem;
            height: 10rem;
            background-color: greenyellow;
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



代码效果显示：

<img src="assert\2.12.PNG" alt="2.12" style="zoom:200%;" />



### 2.13 颜色

+ 颜色单位：
  + 在CSS中可以直接使用颜色名称来设置各种颜色
  + 但是在CSS中直接使用颜色名是非常局限的
+ RGB值：
  + 通过红绿蓝三种颜色的不同浓度来调配出不同的颜色（Red Green Blue）
  + 每一种颜色的范围在0-255（0%-100%）
  + 语法： RGB(红色,绿色,蓝色)
+ RGBA：
  + 在RGB的基础上增加了一个A表示透明度
  + 需要4个值，前三个和RGB一样，第四个表示透明度
  + 1表示完全不透明，0表示完全透明，0.5表示半透明
+ 十六进制的RGB值：
  + 语法：#红色绿色蓝色
  + 颜色浓度范围00-ff
  + 如果颜色两位两位重复，可以进行简写
    + \#aabbcc  —>  #abc
+ HSL值：
  + H：色相（0%~360% 一个环）
  + S：饱和度（0%~100%）
  + L：亮度（0%~100%）





## 3 Layout

### 3.1 文档流

+ 文档流（normal flow）:
  + 网页是一个多层的结构，一层叠着一层
  + 通过CSS可以分别为每一层来设置样式
  + 作为用户来讲只能看到最上面一层
  + 这些层中，==最底下的一层称为文档流==，是网页的基础，我们所创建的元素默认都是在文档流中进行排列
  + 元素主要有两个状态，在文档中、不在文档流中（脱离文档流）
  + 元素在文档流中的特点：
    + 块元素：
      + 块元素会在页面中==独占一行==
      + 默认宽度是父元素的==全部==（会把父元素撑满）
      + 默认高度是被内容（子元素）==撑开==
    + 行内元素:
      + 行内元素不会在页面中独占一行，==只占自身的大小==
      + 在页面中从左向右水平排列，如果一行之中不能容纳下所有的行内元素，则元素会换到第二行继续自左向右排列
      + 行内元素的默认宽度和高度都是==被内容撑开==



```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
    <style>
        .box1{
            
            background-color: yellow;
        }
        .box2{
            background-color: red;
        }
        span{
            background-color: #bfa;
        }
    </style>
</head>
<body>
    <!-- 
        文档流（normal flow）
            -网页是一个多层的结构，一层叠着一层
            -通过CSS可以分别为每一层来设置样式
            -作为用户来讲只能看到最上面一层
            -这些层中，最底下的一层称为文档流，是网页的基础
                我们所创建的元素默认都是在文档流中进行排列
            -元素主要有两个状态，在文档中或不在文档流中（脱离文档流）
            -元素在文档流中有什么特点：
                -块元素
                    -块元素会在页面中独占一行
                    -默认宽度是父元素的全部（会把父元素撑满）
                    -默认高度是被内容（子元素）撑开
                -行内元素
                    -行内元素不会在页面中独占一行，只占自身的大小
                    -在页面中从左向右水平排列，如果一行之中不能容纳下所有的行内元素，则元素会换到第二行继续自左向右排列
                    -行内元素的默认宽度和高度都是被内容撑开
    -->
    <div class="box1">我是div1</div>
    <div class="box2">我是div2</div>

    <span>我是span1</span>
    <span>我是span2</span>
</body>
</html>
```



代码效果显示：

<img src="assert\3.1.PNG" alt="3.1" style="zoom:200%;" />



### 3.2 盒子模型

+  盒模型、盒子模型、框模型（box model）
  + CSS将页面中的所有元素都设置成了一个==矩形的盒子==
  + 将元素设置为矩形的盒子后，对页面的布局就变成将不同的盒子摆放到不同的位置
  + 每个盒子都由以下几个部分组成：
    + 内容区（content）
    + 内边距（padding）
    + 边框（border）
    + 外边距（margin）
+ 内容区（content）：元素中的所有子元素和文本内容都在内容区排列，大小由width和height两个属性来设置 
+ 边框（border）：盒子的边缘，边框里面属于盒子内部
  + 边框的大小影响整个盒子的大小
  + 要设置边框，至少要设置三个样式
    + 宽度 border-width
    + 颜色 border-color
    + 样式 border-style 



```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
    <style>
        .box1{
            /*
                内容区（content），元素中的所有子元素和文本内容都在内容区排列
                    内容区的大小由width和height两个属性来设置 
            */
            width: 200px;
            height: 200px;
            background-color: #bfa;

            /*
                边框（border），盒子的边缘，边框里面属于盒子内部
                边框的大小影响整个盒子的大小
                要设置边框，至少要设置三个样式
                    宽度 border-width
                    颜色  border-color
                    样式  border-style 
            */
            border-width: 10px;
            border-color: red;
            border-style: solid;
        }
    </style>
</head>
<body>
    <!-- 
        盒模型、盒子模型、框模型（box model）
            -CSS将页面中的所有元素都设置成了一个矩形的盒子
            -将元素设置为矩形的盒子后，对页面的布局就变成将不同的盒子摆放到不同的位置
            -每个盒子都由以下几个部分组成
                内容区（content）
                内边距（padding）
                边框（border）
                外边距（margin）
    -->

    <div class="box1">div1</div>
</body>
</html>
```



代码效果显示：

<img src="assert\3.2.PNG" alt="3.2" style="zoom:200%;" />



### 3.3 盒子模型-边框

边框：宽度、颜色、样式 

+ border-width：
  + 有默认值，一般3个像素 
  + 用来指定四个方向的边框的宽度
  + 值的情况：
    + 四个值：上 右 下 左
    + 三个值：上 左右 下
    + 两个值：上下 左右
    + 一个值：上下左右
  + 除了border-width，还有一组border-xxx-width
    + xxx可以是top，right，bottom，left
    + 用来单独指定某一个边的宽度
+ border-color：
  + 指定边框的颜色，同样可以分别指定四个边框，规则同上
  + 不指定边框颜色就默认color值
+ border-style：
  + 指定边框的样式
    + solid表示实线
    + dotted表示点状虚线
    + dashed表示线状虚线
    + double表示双线
+ **border简写属性**：通过该属性可以同时设置边框所有的相关样式，并且==没有顺序要求==
  + 除了border以外还有四个 border-xxx
    +  border-top
    +  border-right
    +  border-bottom
    +  border-left



```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
    <style>
        .box1{
            width: 200px;
            height: 200px;
            background-color: #bfa;

            /*
                边框：宽度、颜色、样式 
            */


            border-width: 10px;
            /*
                有默认值，一般3个像素 
                用来指定四个方向的边框的宽度
                值的情况：
                    四个值：上 右 下 左
                    三个值：上 左右 下
                    两个值：上下 左右
                    一个值：上下左右

                除了border-width，还有一组border-xxx-width
                xxx可以是top，right，bottom，left
                用来单独指定某一个边的宽度
            */

            color: orangered;

            border-color: orange;
            /* 
                指定边框的颜色，同样可以分别指定四个边框，规则同上
                不指定边框颜色就默认color值
            */
            
            border-style: solid;
            /*
                指定边框的样式
                solid表示实线
                dotted表示点状虚线
                dashed表示线状虚线
                double表示双线
            */


            /* 
                !!!
                border简写属性，通过该属性可以同时设置边框所有的相关样式，并且没有顺序要求
                除了border以外还有四个  border-xxx
                    border-top
                    border-right
                    border-bottom
                    border-left
            */
            border: 10px orange solid;
        }
    </style>
</head>
<body>
    <div class="box1"></div>
</body>
</html>
```



代码效果显示：

<img src="assert\3.3.PNG" alt="3.3" style="zoom:200%;" />



### 3.4 盒子模型-内边距

+ 内边距padding
  + ==内容区和边框之间的距离==
  + 一共有四个方向的内边距
    + padding-top
    + padding-right
    + padding-bottom
    + padding-left
  + 内边距的设置==会影响到盒子大小==
  + 背景颜色会延伸到内边距上
+ 一个盒子可见宽的大小，由内容区，内边距和边框共同决定
+ 所以在计算盒子大小时，需要将三个区域加到一起计算



```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
    <style>
        .box1{
            width: 200px;
            height: 200px;
            background-color: #bfa;
            border: 10px orange solid;

            padding-top: 100px;

            /* 
                padding简写属性，和border一样 
            */

        }

    

        .inner{
            width: 100%;
            height: 100%;
            background-color: yellow;
        }
    </style>
</head>
<body>
    <div class="box1">
        <div class="inner"></div>
    </div>
</body>
</html>
```



代码效果显示：

<img src="assert\3.4.PNG" alt="3.4" style="zoom:200%;" />



### 3.5 盒子模型-外边距

外边距（margin）：

+ 外边距==不会影响盒子可见框的大小==，但是外边距==会影响盒子的位置==
+ 一共有四个方向的外边距
  + margin-top
  + margin-right 一般情况下设置不会产生任何效果
  + margin-bottom 下外边距，设置一个正值，其下边的元素会向下移动。如果是负值，则元素则会向==相反==的方向移动
  + margin-left
+ 元素在页面中是按照自左向右的顺序排列的，故默认情况下若==设置左和上外边距则会移动元素自身==，而==设置下和右外边距会移动其他元素==
+ 简写属性，用法和padding一样
+ margin==会影响到盒子实际占用空间==



```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
    <style>
        .box1{
            width: 200px;
            height: 200px;
            background-color: #bfa;
            border: 10px red solid;

            margin-top: 100px;
            margin-bottom: 100px;
        }

        .box2{
            width: 200px;
            height: 200px;
            background-color: yellow;
            border: 10px red solid;
        }
        
    </style>
</head>
<body>
    <div class="box1"></div>
    <div class="box2"></div>
</body>
</html>
```



代码效果显示：

<img src="assert\3.5.PNG" alt="3.5" style="zoom:200%;" />



### 3.6 盒子的水平布局

元素水平方向的布局：

+ 元素在其父元素中水平方向的位置由以下几个属性共同决定

  + margin-left
  + border-left
  + padding-left
  + width
  + padding-right
  + border-right
  + margin-right

+ 一个元素在其父元素中，水平布局**必须满足**以下的等式：

  + margin-left + border-left + padding-left + width + padding-right + border-right + margin-right            = 其父元素内容区的宽度

  + 若不成立，则称为==过度约束==，等式会自动调整

  + 调整的情况：

    + 如果上述七个值中没有为auto的情况，则浏览器==会自动调整margin-right值==来使等式成立

    + 这七个值中有三个值可以设置为auto： width   margin-left   margin-right

    + 如果设置为auto，则会自动调整为auto的那个值来使等式成立

    + 如果将一个宽度和一个外边距设置为auto，则宽度会调整到最大，为auto的外边距会是0

    + 如果将三个值都设置为auto，则外边距都是0，宽度最大

    + 如果将两个外边距设置为auto，宽度固定值，则会将外边距设置为相同值，所以经常利用这个特点来使一个元素==在其父元素中水平居中==

      + 示例：

       ```html
        width:20px;
        margin:0 auto;  /* 上下是0，左右时auto */
       ```

        

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
    <style>
        .outer{
            width: 800px;
            height: 200px;
            border: 10px red solid;
        }

        .inner{
            /* width的值默认使auto */
            width: 200px;   
            height: 200px;
            background-color: #bfa;
            margin-left: 100px;

            /* 
            元素水平方向的布局：
                -元素在其父元素中水平方向的位置由以下几个属性共同决定
                    margin-left
                    border-left
                    padding-left
            		width
                    padding-right
                    border-right
                    margin-right
                -一个元素在其父元素中，水平布局必须满足以下的等式：
margin-left + border-left + padding-left + width + padding-right + border-right + margin-right = 其父元素内容区的宽度
                0 + 0 + 0 + 200 + 0 + 0 + 0 != 800
                若不成立，则称为过度约束，等式会自动调整
                0 + 0 + 0 + 200 + 0 + 0 + 600 = 800

                -调整的情况：
                	-如果上述七个值中没有为auto的情况，则浏览器会自动调整margin-right值来使等式成立
                    -这七个值中有三个值可以设置为auto：
                        width
                        margin-left
                        margin-right
                	-如果设置为auto，则会自动调整为auto的那个值来使等式成立
                      0 + 0 + 0 + auto + 0 + 0 + 0 = 800                                                   auto = 800
                      0 + 0 + 0 + 800 + 0 + 0 + 0 = 800
                    -如果将一个宽度和一个外边距设置为auto，则宽度会调整到最大，为auto的外边距是0
                    -如果将三个值都设置为auto，则外边距都是0，宽度最大
                    -如果将两个外边距设置为auto，宽度固定值，则会将外边距设置为相同值，所以经常利用这个特点来使一个元素在其父元素中水平居中
                     	示例：
                           width:20px;
                           margin:0 auto;  上下是0，左右时auto

            */
        }
    </style>
</head>
<body>
    <div class="outer">
        <div class="inner"></div>
    </div>
</body>
</html>
```



代码显示效果：

<img src="assert\3.6.PNG" alt="3.6" style="zoom:200%;" />



### 3.7 盒子的垂直布局

+ 默认情况下父元素的高度被内容撑开
+ 子元素是在父元素的内容区排列的
  + 如果子元素的大小超过了父元素，则子元素会从父元素中==溢出==
  + 使用 ==overflow 属性==来设置父元素如何处理溢出的子元素
  + 可选值：
    + visible：默认值，子元素会从父元素中溢出，在父元素外部的位置显示
    + hidden：溢出的内容将会被裁剪，不会显示
    + scroll：生成两个滚动条（水平和垂直），通过滚动条查看完整的内容
    + auto：根据需要生成滚动条
    + overflow-x：水平
    + overflow-y：垂直



```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
    <style>
        .outer{
            background-color: #bfa;
            height: 600px;
            /* 
                默认情况下父元素的高度被内容撑开
            */
        }

        .inner{
            height: 200px;
            width: 100px;
            background-color: yellow;
            margin-bottom: 100px;

        }

        .box1{
            width: 200px;
            height: 200px;
            background-color: #bfa;
            /* 
                子元素是在父元素的内容区排列的
                    如果子元素的大小超过了父元素，则子元素会从父元素中溢出
                    使用 overflow 属性来设置父元素如何处理溢出的子元素
                    可选值：
                        -visible  默认值，子元素会从父元素中溢出，在父元素外部的位置显示
                        -hidden  溢出的内容将会被裁剪，不会显示
                        -scroll  生成两个滚动条（水平和垂直），通过滚动条查看完整的内容
                        -auto  根据需要生成滚动条
                        -overflow-x  水平
                        -overflow-y  垂直
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
        <div class="inner"></div>
    </div>

    <div class="box1">
        <div class="box2"></div>
    </div>
</body>
</html>
```



代码显示效果：

<img src="assert\3.7.PNG" alt="3.7" style="zoom:200%;" />





### 3.8 外边距的折叠

垂直外边距的折叠

+ 相邻的垂直方向的外边距会发生重叠的现象
+ 兄弟元素：
  + 兄弟元素间的相邻垂直外边距会取两个之间的较大值（两者都是正值）
  + 特殊情况：
    + 如果相邻的外边距一正一负，则取两者之和
    + 如果两者都为负，取较小值
  + 兄弟元素之间外边距的重叠，对于开发是有利的，所以不需要进行处理
+ 父子元素：
  + 父子元素间的相邻外边距，子元素的会传递给父元素（上外边距）
  + 父子外边距的折叠会影响到页面的布局。必须要进行处理



```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
    <style>
        .box1,.box2{
            width: 200px;
            height: 200px;
        }

        /* 
            垂直外边距的折叠
                -相邻的垂直方向的外边距会发生重叠的现象
                -兄弟元素
                    -兄弟元素间的相邻垂直外边距会取两个之间的较大值（两者都是正值）
                    -特殊情况：
                        如果相邻的外边距一正一负，则取两者之和
                        如果两者都为负，取较小值
                    -兄弟元素之间外边距的重叠，对于开发是有利的，所以不需要进行处理
                -父子元素
                    -父子元素间的相邻外边距，子元素的会传递给父元素（上外边距）
                    -父子外边距的折叠会影响到页面的布局。必须要进行处理
        */

        .box1{
            background-color: #bfa;
            /* 设置一个下外边距 */
            margin-bottom: 100px;
        }

        .box2{
            background-color: orange;
            /* 设置一个上外边距 */
            margin-top: 100px;
        }

        .box3{
            width: 200px;
            height: 200px;
            background-color: #bfa;
            padding-top: 100px; 
            border-top: 1px red solid;
        }

        .box4{
            width: 100px;
            height: 100px;
            background-color: orange;
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



代码显示效果：

<img src="assert\3.8.PNG" alt="3.8" style="zoom:200%;" />





### 3.9 行内元素的盒模型

+ 行内元素不支持设置宽度和高度
+ 行内元素可以设置padding，但垂直方向的padding不会影响页面的布局
+ 行内元素可以设置border，但垂直方向的border不会影响页面的布局
+ 行内元素可以设置margin，垂直方向的margin不会影响页面的布局



+ display属性：用来设置元素显示的类型
  + 可选值：
  + inline：将元素设置为行内元素
  + block：将元素设置为块元素
  + inline-block：将元素设置为行内块元素（行内块，既可以设置宽度和高度又不会独占一行）
  + table：将元素设置成一个表格
  + none：元素不在页面中显示
+ visibility属性：用来设置元素的显示状态
  + 可选值：
  + visible 默认值，元素在页面中正常显示
  + hidden 元素在页面中隐藏不显示，但是**依然占据页面的位置**



```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
    <style>
        .s1{
            background-color: yellow;

            /* 
                行内元素的盒模型
                    -行内元素不支持设置宽度和高度
                    -行内元素可以设置padding，但垂直方向的padding不会影响页面的布局
                    -行内元素可以设置border，但垂直方向的border不会影响页面的布局
                    -行内元素可以设置margin，垂直方向的margin不会影响页面的布局
            */

            width: 100px;
            height: 100px;

            padding: 100px;

            border: 100px red solid;

            margin: 50px;

        }

        .box1{
            width: 200px;
            height: 200px;
            background-color: #bfa;
        }

        a{
            /* 
                display  用来设置元素显示的类型
                    可选值：
                        inline  将元素设置为行内元素
                        block  将元素设置为块元素
                        inline-block  将元素设置为行内块元素
                                      行内块，既可以设置宽度和高度又不会独占一行
                        table  将元素设置成一个表格
                        none  元素不在页面中显示
                visibility  用来设置元素的显示状态
                    可选值：
                        visible 默认值，元素在页面中正常显示
                        hidden  元素在页面中隐藏不显示，但是依然占据页面的位置
            */
            visibility: visible;
            display: block;
            background-color: orange;
            width: 100px;
            height: 100px;
        }
    </style>
</head>
<body>

    <a href="javascript:;">超链接</a>
    <span class="s1">我是span</span>
    <span class="s1">我是span</span>
    <div class="box1"></div>
</body>
</html>
```



代码效果显示：

<img src="assert\3.9.PNG" alt="3.9" style="zoom:200%;" />





### 3.10 默认样式

通常情况，浏览器都会为元素设置一些默认样式

默认样式的存在会影响到页面的布局 ，通常情况下编写网页是必须要去除掉浏览器的默认样式



一般开发中使用的reset.css：

```css
/* http://meyerweb.com/eric/tools/css/reset/ 
   v2.0 | 20110126
   License: none (public domain)
*/

html, body, div, span, applet, object, iframe,
h1, h2, h3, h4, h5, h6, p, blockquote, pre,
a, abbr, acronym, address, big, cite, code,
del, dfn, em, img, ins, kbd, q, s, samp,
small, strike, strong, sub, sup, tt, var,
b, u, i, center,
dl, dt, dd, ol, ul, li,
fieldset, form, label, legend,
table, caption, tbody, tfoot, thead, tr, th, td,
article, aside, canvas, details, embed, 
figure, figcaption, footer, header, hgroup, 
menu, nav, output, ruby, section, summary,
time, mark, audio, video {
	margin: 0;
	padding: 0;
	border: 0;
	font-size: 100%;
	font: inherit;
	vertical-align: baseline;
}
/* HTML5 display-role reset for older browsers */
article, aside, details, figcaption, figure, 
footer, header, hgroup, menu, nav, section {
	display: block;
}
body {
	line-height: 1;
}
ol, ul {
	list-style: none;
}
blockquote, q {
	quotes: none;
}
blockquote:before, blockquote:after,
q:before, q:after {
	content: '';
	content: none;
}
table {
	border-collapse: collapse;
	border-spacing: 0;
}
```





### 3.11 盒子的大小

默认情况下，盒子可见框的大小由==内容区、内边框和边框共同决定==

+ box-sizing 用来设置盒子尺寸的计算方式（设置width和height的作用）
+ 可选值：
  + content-box 默认值，宽度和高度用来设置内容区的大小
  + border-box 宽度和高度用来设置盒子可见框的大小
    + width和height指的是内容区和内边距和边框的大小



```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
    <style>
        .box1{
            width: 100px;
            height: 100px;
            background-color: #bfa;
            padding: 10px;
            border: 10px red solid;
            /*
                默认情况下，盒子可见框的大小由内容区、内边框和边框共同决定
                    box-sizing 用来设置盒子尺寸的计算方式（设置width和height的作用）
                        可选值：
                            content-box 默认值，宽度和高度用来设置内容区的大小
                            border-box 宽度和高度用来设置盒子可见框的大小
                                width和height指的是内容区和内边距和边框的大小
            */
            box-sizing: content-box;
        }
    </style>
</head>
<body>
    <div class="box1"></div>
</body>
</html>
```



代码效果显示：

<img src="assert\3.11.PNG" alt="3.11" style="zoom:200%;" />





### 3.12 轮廓和转角

**轮廓**： box-shadow 用来设置元素的阴影效果，不会影响页面布局

+ 第一个值：水平偏移量 设置阴影的水平位置 正值向右移动 负值向左移动
+ 第二个值：垂直偏移量 设置阴影的垂直位置 正值向下移动 负值向上移动
+ 第三个值：阴影的模糊半径，越大越模糊
+ 第四个值：阴影颜色

**转角**： border-radius: ; 用来设置圆角,圆角设置的是圆的半径大小

+ 可以分别指定四个角的圆角，左上，右上，右下，左下
+ 三个值：左上，右上左下，右下
+ 两个值：左上右下，右上左下
  + border-top-left-radius: ;
  + border-top-right-radius: ;
  + border-bottom-left-radius: ; 
  + border-bottom-right-radius: ;
  + border-top-left-radius: 50px;
  + border-top-right-radius: 50px 80px;



```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
    <style>
        .box1{
            width: 200px;
            height: 200px;
            background-color: #bfa;

            /* 
                box-shadow 用来设置元素的阴影效果，不会影响页面布局
                第一个值：水平偏移量 设置阴影的水平位置 正值向右移动 负值向左移动
                第二个值：垂直偏移量 设置阴影的垂直位置 正值向下移动 负值向上移动
                第三个值：阴影的模糊半径，越大越模糊
                第四个值：阴影颜色
            */
            
            box-shadow: 10px 10px 10px rgba(0,0,0,0.3);

            /* 
                outline用来设置元素的轮廓线，用法和border一模一样，
                和轮廓不一样的点是不会影响可见框的大小
            */
            outline: 10px red solid;
        }

        .box1:hover{
            outline: 10px red solid;
        }

        .box2{
            width: 200px;
            height: 200px;
            background-color: orange;
            margin-top: 50px;
            /* 
                border-radius: ; 用来设置圆角,圆角设置的是圆的半径大小
                可以分别指定四个角的圆角，左上，右上，右下，左下
                三个值：左上，右上左下，右下
                两个值：左上右下，右上左下
            */
            /* border-top-left-radius: ; */
            /* border-top-right-radius: ; */
            /* border-bottom-left-radius: ; */
            /* border-bottom-right-radius: ; */

            /* border-top-left-radius: 50px;
            border-top-right-radius: 50px 80px; */

            /* 如果想将元素设置为一个圆形 */
            border-radius: 50%;

        }
    </style>
</head>
<body>
    <div class="box1"></div>

    <div class="box2"></div>
</body>
</html>
```



代码效果显示：

<img src="assert\3.12.PNG" alt="3.12" style="zoom:200%;" />







## 4 Float

### 4.1 浮动简介

通过浮动可以使一个元素向其父元素的左侧或右侧移动

+ 使用float属性来设置元素的浮动
+ 可选值：
  + none：默认值，元素不浮动
  + left right：向左向右浮动
+ **注意**：元素设置浮动以后，水平布局的等式便不需要满足。元素会==完全从文档中分离==，不再占用文档流的位置，所以元素下边的还在文档流中的元素会自动向上移动
+ 浮动的特点：
  + 浮动元素会完全脱离文档流，不再占据文档流中的位置
  + 设置浮动后元素会向父元素的左侧或者右侧移动
  + 浮动元素默认不会从父元素中移出
  + 浮动元素向左或向右移动时，不会超过其前面的其他浮动元素
  + 如果浮动元素的上边是一个没有浮动的块元素，则浮动元素无法上移
  + 浮动元素不会超过其上边的浮动的兄弟元素，最多就是和兄弟一样高

简单总结：

+ 浮动目前来讲它的主要作用就是让页面中的元素可以**水平排列**
+ 通过浮动可以制作一些==水平方向==的布局



```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
    <style>
        .box1{
            width: 200px;
            height: 200px;
            background-color: #bfa;
            float: left;
        }

        .box2{
            width: 200px;
            height: 200px;
            background-color: orange;
            float: left;
        }

        .box3{
            width: 200px;
            height: 200px;
            background-color: yellow;
            float: left;
        }
    </style>
</head>
<body>
    <div class="box1"></div>

    <div class="box2"></div>

    <div class="box3"></div>
</body>
</html>
```



代码效果显示：

<img src="assert\4.1.PNG" alt="4.1" style="zoom:200%;" />



### 4.2 浮动的其他特点

元素设置浮动以后，会从文档流脱离，然后元素的一些特点也会发生变化 

脱离文档流的特点：

+ 块元素：
  + 块元素不再独占页面的一行
  + 脱离文档流以后，块元素的宽度和高度默认都被内容撑开
+ 行内元素：
  + 行内元素脱离文档流后会变成块元素，特点和块元素一样

脱离文档流以后，不需要再区分块和行内了

浮动元素不会盖住文字，文字会自动环绕子浮动元素的周围所以我们可以利用浮动来设置文字环绕图片的效果



```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
    <style>
        *{
            margin: 0;
            padding: 0;
        }

        .box1{
            width: 100px;
            height: 100px;
            background-color: #bfa;
            float: left;
            /* 
                浮动元素不会盖住文字，文字会自动环绕子浮动元素的周围所以我们可以利用浮动来设置文字环绕图片的效果
            */
        }

        .box2{
            background-color: yellowgreen;
            float: left;
        }

        .box3{
            background-color: orange;
        }

        .s1{
            background-color: yellow;
            float: left;
            width: 200px;
            height: 200px;
        }
    </style>
</head>
<body>
    <div class="box1"></div>
    <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Possimus assumenda tempore dolorum officia aliquid, pariatur sunt odio, similique fugit sequi magni nobis veniam fuga quia, eaque odit ab ea aut.</p>

    <span class="s1">这是一个span</span>

    <div class="box2">hello</div>

    <div class="box3">hello</div>
</body>
</html>
```



代码效果显示：

<img src="assert\4.2.PNG" alt="4.2" style="zoom:200%;" />



### 4.3 网页布局

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
    <style>
        header,main,footer{
            width: 500px;
            margin: 0 auto;
        }
        
        /* 设置头部 */
        header{
            height: 120px;
            background-color: silver;
        }

        /* 设置主体 */
        main{
            height: 400px;
            background-color: #bfa;
            margin: 10px auto;
        }

        /* 设置左侧的导航 */
        nav{
            float: left;
            width: 90px;
            height: 100%;
            background-color: yellow;
        }

        /* 设置中间的内容 */
        article{
            float: left;
            width: 300px;
            height: 100%;
            background-color: orange;
            margin: 0 10px;
        }

        /* 设置右侧的内容 */
        aside{
            float: left;
            width: 90px;
            height: 100%;
            background-color: pink;
        }

        /* 设置底部 */
        footer{
            height: 150px;
            background-color: tomato;
        }
    </style>
</head>
<body>
    <!-- 创建头部 -->
    <header></header>

    <!--  创建网页的主体 -->
    <main>
        <!-- 左侧导航 -->
        <nav></nav>

        <!-- 中间的内容 -->
        <article></article>

        <!-- 右边的边栏 -->
        <aside></aside>
    </main>

    <!-- 网页的底部 -->
    <footer></footer>
</body>
</html>
```



代码显示效果：

<img src="assert\4.3.PNG" alt="4.3" style="zoom:200%;" />





### 4.4 高度塌陷

+ 在浮动布局中，父元素的高度默认是被子元素撑开的，当子元素浮动后，其会完全脱离文档流，即子元素从文档流中脱离，所以==将会无法撑起父元素的高度==，导致==父元素的高度丢失==，父元素高度丢失以后，其下面的元素会自动上移，导致页面的布局混乱。所以高度塌陷是浮动布局中比较常见的一个问题
+ 解决办法：BFC(Block Formatting Context) 块级格式化环境
  + BFC是CSS中一个隐含的属性，可以为一个元素开启BFC，开启后该元素会变成一个独立的布局区域
  + 元素开启BFC后的特点：
    + 不会被浮动元素覆盖
    + 子元素和父元素的外边距不会重叠
    + 可以包含浮动的子元素
  + 可以通过一些特殊方式来开启元素的BFC
    + 设置元素的浮动
    + 将元素设置为行内块元素
    + (**推荐**)将元素的overflow设为非visible的值
      + 常用方式：为元素设置 overflow:hidden 从而开启其BFC，以使其可以包含浮动元素



```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
    <style>
        .outer{
            border: 10px red solid;
            /* float: left; */
            /* display: inline-block; */
            overflow: hidden;
        }

        .inner{
            width: 100px;
            height: 100px;
            background-color: #bfa;
            float: left;           
        }
    </style>
</head>
<body>
    <div class="outer">
        <div class="inner"></div>
    </div>

    <div style="width: 200px;height: 200px;background-color: yellow;"></div>
</body>
</html>
```



代码效果显示：

<img src="assert\4.4.PNG" alt="4.4" style="zoom:200%;" />



### 4.5 BFC

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
    <style>
        .box1{
            width: 200px;
            height: 200px;
            background-color: #bfa;
            /* float: left; */
            overflow: hidden;
        }
        .box2{
            width: 200px;
            height: 200px;
            background-color: orange;
            overflow: hidden;
        }
        .box3{
            width: 100px;
            height: 100px;
            background-color: yellow;
            margin-top: 100px;
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



代码效果显示：

<img src="assert\4.5.PNG" alt="4.5" style="zoom:200%;" />



### 4.6 clear

如果不希望某个元素因为其他元素浮动的影响而改变位置，则可以通过clear属性来==清除浮动元素对当前元素所产生的影响==



clear：

+ 作用：清除浮动元素对当前元素所产生的影响
+ 可选值：
  + left 清除左侧浮动元素对当前元素所产生的影响
  + right 清除右侧浮动元素对当前元素所产生的影响
  + both 清除两侧中**最大影响**的那侧
+ 原理：设置清除浮动以后，浏览器为自动为元素添加一个上边距，使其位置不受影响



```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
    <style>
        div{
            font-size: 50px;
        }

        .box1{
            width: 200px;
            height: 200px;
            background-color: #bfa;
            float: left;
        }

        .box2{
            width: 400px;
            height: 400px;
            background-color: #ff0;
            float: right;
        }

        .box3{
            width: 200px;
            height: 200px;
            background-color: orange;
            /*
                由于box1的浮动，导致box3位置上移
                也就是box3受到了box1浮动的影响，位置发生了改变

                如果不希望某个元素因为其他元素浮动的影响而改变位置，
                则可以通过clear属性来清除浮动元素对当前元素所产生的影响
            */
            clear: right;
        }
    </style>
</head>
<body>
    <div class="box1">1</div>
    <div class="box2">2</div>
    <div class="box3">3</div>
</body>
</html>
```



代码效果显示：

<img src="assert\4.6.PNG" alt="4.6" style="zoom:200%;" />





### 4.7 高度塌陷的最终方案

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
    <style>
        .box1{
            border: 10px red solid;
        }

        .box2{
            width: 100px;
            height: 100px;
            background-color: #bfa;
            float: left;
        }

        .box1::after{
            content: "";
            display: block;
            clear: both;
        }
    </style>
</head>
<body>
    <div class="box1">
        <div class="box2"></div>
    </div>
</body>
</html>
```



代码效果显示：

<img src="assert\4.7.PNG" alt="4.7" style="zoom:200%;" />





### 4.8 clearfix

clearfix这个样式可以同时解决高度塌陷和外边距重叠的问题，当遇到这些问题时，直接使用clearfix类即可

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
    <style>
        .box1{
            width: 200px;
            height: 200px;
            background-color: #bfa;
        }

        /* .box1::before{
            content: "";
            display: table;
        } */

        .box2{
            width: 100px;
            height: 100px;
            background-color: orange;
            margin-top: 100px;
        }

        /* clearfix这个样式可以同时解决高度塌陷和外边距重叠的问题，当遇到这些问题时，直接使用clearfix类即可 */
        .clearfix::before,
        .clearfix::after{
            content: "";
            display: table;
            clear: both;
        }
    </style>
</head>
<body>
    <div class="box1 clearfix">
        <div class="box2"></div>
    </div>
</body>
</html>
```



代码效果显示：

<img src="assert\4.8.PNG" alt="4.8" style="zoom:200%;" />



## 5 Position

### 5.1 定位（position）的简介

+ 定位是一种更加高级的布局手段
+ 通过定位，可以将一个元素摆放到页面的**任意位置**
+ 使用position属性来设置定位
  + 可选值：
    + static：默认值，元素是静止的，即没有开启定位
    + relative：开启元素的相对定位
    + absolute：开启元素的绝对定位
    + fixed：开启元素的固定定位
    + sticky：开启元素的粘滞定位
+ **相对定位**：当元素的position属性值设置为relative时则开启了相对定位
  + 特点：
    + 元素开启相对定位以后，==如果不设置偏移量，元素不会发生任何变化==
    + 相对定位是参照于元素在文档流中的位置来定位的
    + 相对定位会提升元素的层级（==会盖住其他元素==）
    + 不会使元素脱离文档流
    + 不会改变元素的性质（块还是块，行内还是行内）
+ 偏移量：当元素开启定位后，可以通过偏移量来设置元素的位置
  + top：定位元素和定位位置上边的距离
  +  bottom：定位元素和定位位置下边的距离
  + left
  + right
  + 定位元素垂直方向的位置由top和bottom两个属性来控制，通常只会使用其中一个



```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
    <style>
        body{
            font-size: 60px;
        }

        .box1{
            width: 200px;
            height: 200px;
            background-color: #bfa;
        }

        .box2{
            width: 200px;
            height: 200px;
            background-color: orange;
            position: relative;
            left: 200px;
            top: -200px;
        }

        .box3{
            width: 200px;
            height: 200px;
            background-color: yellow;
        }
    </style>
</head>
<body>
    <div class="box1">1</div>
    <div class="box2">2</div>
    <div class="box3">3</div>
</body>
</html>
```



代码效果显示：

<img src="assert\5.1.PNG" alt="5.1" style="zoom:200%;" />





### 5.2 绝对定位

当元素的position属性值设置为absolute时，则开启元素的绝对定位 

绝对定位的特点：

+ 开启绝对定位后，==若不设置偏移量，元素位置不会发生变化==
+ 开启绝对定位后，元素==会从文档流中脱离==
+ 绝对定位==会改变元素的性质==，行内变成块，块的宽高被内容撑开
+ 绝对定位会使元素提升一个层级
+ 绝对定位元素是相对于其包含块进行定位的
  + 包含块：（containing block）
    + 正常情况下，包含块就是当前元素最近的祖先块元素
    + 开启绝对定位的包含块：包含块就是离它最近的开启了定位的祖先元素。如果所有的祖先元素都没有开启定位，则相对于根元素进行定位，即根元素就是它的包含块
    + html：根元素/初始包含块



```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
    <style>
        body{
            font-size: 60px;
        }

        .box1{
            width: 200px;
            height: 200px;
            background-color: #bfa;
        }

        .box2{
            width: 200px;
            height: 200px;
            background-color: orange;
            position: absolute;
            left: 0;
            top: 0;
        }

        .box3{
            width: 200px;
            height: 200px;
            background-color: yellow;
        }

        .box4{
            width: 400px;
            height: 400px;
            background-color: tomato;
            /* position: relative; */
        }

        .box5{
            width: 300px;
            height: 300px;
            background-color: aliceblue;
            /* position: relative; */
        }
    </style>
</head>
<body>
    <div class="box1">1</div>
    <div class="box4">
        4
        <div class="box5">
            5
            <div class="box2">2</div>
        </div>
    </div>
    <div class="box3">3</div>
</body>
</html>
```



代码效果显示：

<img src="assert\5.2.PNG" alt="5.2" style="zoom:200%;" />





### 5.3 固定定位

将元素的position属性设置为fixed则开启了元素的固定定位

固定定位==也是一种绝对定位==，所以固定定位的大部分特点都和绝对定位一样，唯一不同的是固定定位==永远参照于浏览器的视口（可视区域）进行定位==，即固定定位的元素不会随网页的滚动条滚动



```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
    <style>
        body{
            font-size: 60px;
            height: 2000px;
        }

        .box1{
            width: 200px;
            height: 200px;
            background-color: #bfa;
        }

        .box2{
            width: 200px;
            height: 200px;
            background-color: orange;
            position: fixed;
            left: 0;
            top: 0;

        }

        .box3{
            width: 200px;
            height: 200px;
            background-color: yellow;
        }

        .box4{
            width: 400px;
            height: 400px;
            background-color: tomato;
        }

        .box5{
            width: 300px;
            height: 300px;
            background-color: aliceblue;
        }
    </style>
</head>
<body>
    <div class="box1">1</div>
    <div class="box4">
        4
        <div class="box5">
            5
            <div class="box2">2</div>
        </div>
    </div>
    <div class="box3">3</div>
</body>
</html>
```







### 5.4 粘滞定位

当元素的position属性设置为sticky时，则开启了元素的粘滞定位

与相对定位的特点基本一致，不同的时粘滞定位可以在元素==到达某个位置==时将其固定





### 5.5 绝对定位元素的布局

+ 水平布局：

   left + margin-left + border-left + padding-left + width + padding-right + border-right + margin-right + right = 包含块内容区的宽度 



+ 当开启绝对定位以后，水平方向的布局等式就需要添加right和left两个值，规则不变

（规则：当发生过度约束时，如果9个值中没有auto，则自动调整right值以使等式满足。如果有auto，则自动调整auto值来使等式满足）

 **ps**：可设置auto的值 margin width left right



+ 垂直方向布局的等式也必须要满足：

top + margin-top/botttom + padding-top/bottom + border-top/bottom + height = 包含块的高度



```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
    <style>
        .box1{
            width: 500px;
            height: 500px;
            background-color: #bfa;
            position: relative;
        }

        .box2{
            width: 100px;
            height: 100px;
            background-color: orange;
            position: absolute;
            margin-left: auto;
            margin-right: auto;
            margin-top: auto;
            margin-bottom: auto;
            left: 0;
            right: 0;
            top: 0;
            bottom: 0;

        }
    </style>
</head>
<body>
    <div class="box1">
        <div class="box2"></div>
    </div>
</body>
</html>
```



代码效果显示：

<img src="assert\5.5.PNG" alt="5.5" style="zoom:200%;" />





### 5.6 元素的层级

+ 对于**开启了定位**的元素，可以通过==z-index属性==来指定元素的层级
+ 参数是整数，参数越大，元素的层级越高，越优先显示（甚至可以设置9999） 
+ 如果元素的层级一样，则优先显示靠下的
+ 祖先元素的层级再高，也不会盖住后代元素



```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
    <style>
        body{
            font-size: 60px;
        }

        .box1{
            width: 200px;
            height: 200px;
            background-color: #bfa;
            position: absolute;
            /*
                对于开启了定位的元素，可以通过z-index属性来指定元素的层级
                参数是整数，参数越大，元素的层级越高，越优先显示 
                如果元素的层级一样，则优先显示靠下的
                祖先元素的层级再高，也不会盖住后代元素
            */
            z-index: 1;
            
        }

        .box2{
            width: 200px;
            height: 200px;
            background-color: rgba(255, 0, 0, 0.3);
            position: absolute;
            top: 50px;
            left: 50px;
            z-index: 2;
        }

        .box3{
            width: 200px;
            height: 200px;
            background-color: yellow;
            position: absolute;
            top: 100px;
            left: 100px;
            z-index: 3;
        }

        .box4{
            width: 100px;
            height: 100px;
            background-color: orange;
            position: absolute;
        }
    </style>
</head>
<body>
    <div class="box1">1</div>
    <div class="box2">2</div>
    <div class="box3">3
        <div class="box4">4</div>
    </div>

</body>
</html>
```



代码效果显示：

<img src="assert\5.6.PNG" alt="5.6" style="zoom:200%;" />




