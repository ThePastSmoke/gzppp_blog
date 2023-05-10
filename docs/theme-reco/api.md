---
title: css基础知识
date: 2022-10-21
---

​	

### 类选择器（重点）

**作用：**实际开发中我们可以通过类选择器给对应的标签设置名称，然后设置不同的样式，从而实现同一类标签的差异化设置；

实际开发中如果想要使用类选择器我们需要两步来完成：

第一步：在css文件中用英文点( **.** )后面紧跟着类名 称给元素设置对应的样式；

```css
 .类名称 { 
 	css属性:css属性值;
 }
```

第二步：在html结构中给对应的标签设置 **class属性="类名称"** ，调用css设置的样式；

```html
<div class="类名称"></div>
```

![](D:/%E5%89%8D%E7%AB%AF%E9%9D%A2%E8%AF%95%E8%A7%86%E9%A2%91/%E5%89%8D%E7%AB%AF%E5%AD%A6%E4%B9%A0/JS%E5%AD%A6%E4%B9%A0%E8%B5%84%E6%96%99/%E5%9F%BA%E7%A1%80%E7%8F%AD%E5%AD%A6%E4%B9%A0%E8%B5%84%E6%96%99/%E8%AF%BE%E4%BB%B6/12/css%E7%AC%AC%E4%B8%80%E5%A4%A9/%E4%B8%8A%E8%AF%BE%E7%AC%94%E8%AE%B0/assets/04.png)

### id选择器

id选择器可以帮助我们设置标签样式，但是我们在实际开发中一般不会用id选择器设置布局样式。

id选择器在实际开发中我们主要是在javascript中获取元素使用：

```js
    <div id="box">老王</div>
    <script>
        // 获取id名称为box的盒子
        var box = document.getElementById('box')
        box.onclick = function () {
            alert('老王是最好的')
        }
    </script>
```

如果想要使用id选择器设置盒子样式，我们也要通过两步完成：

第一步：在css文件中用 **# 号** 后面紧跟着id名 称给元素设置对应的样式；

```css
 #id名称 { 
 	css属性:css属性值;
 }
```

第二步：在html结构中给对应的标签设置 **id属性="id名称"** ，调用css设置的样式；

```html
<div id="id名称"></div>
```

### 通配符选择器（同学们）*

一个 ***** 可以匹配当前页面的所有标签，设置统一的样式；

实际的开发中我们会设置所有标签的内外边距为0，放在css的最前面

```css
* {
     margin: 0;
     padding: 0;
   }
```



### 选择器命名规范

01、不能用纯数字、数字开头的、中文命名,可以用数字结尾；

02、命名最好有意义，尽量让别人一眼就能知道这个类名的目的，可以参照开发手册或者直接百度翻译即；

03、长名称或者词组可以使用横线或者下划线连接命名；

```html
    <div class="home-brick-box">可爱的程序员</div>
    <div class="home_brick_box">可爱的程序员</div>	
```

### 选择器使用注意事项和技巧（重点）

#### 类选择器使用注意事项 -- 重复使用性

类名称是可以重复调用的，前提条件是两个盒子样式完全一致；

#### 类选择高级技巧 -- 多类名调用

一个标签只能设置一个calss属性，如果想要调用多个类名我们可以在一个class里面直接以空格隔开直接书写另一个类名称即可；

```html
<!-- 语法： class="类名1 类名2 类名3 ..." -->
<div class="w box">可爱的程序员</div>
```

#### id选择器使用技巧 -- 唯一性

id选择器是唯一的不能重复使用，一个id名称一个页面只能出现一次；

## 元素的实体化三属性（重点）

所谓的实体化三属性指的就是元素的宽度width、高度height、背景background：

```css
        .box {
            width: 300px;
            height: 300px;
            background: red;
        }
```

**注意：**01、实体化三属性非常重要，只要书写的宽高都是和设计稿一样，静态页面就不会出现兼容问题；

​	    02、宽度和高度必须要加px像素单位；

## 常见文本控制属性（记住）

### 文字字体  font-family（ff）

设置文字显示的字体

```css
font-family: '宋体'; 
font-family: '宋体', Arial, 'Microsoft Yahei';
```

**注意：**01、字体的取值可以是一个值也可以是多个值，如果是**多个值需要用英文逗号隔开**，如果**字体是汉字或者多个英文单词组成可以用英文引号包裹起来**；

​	   02、谷歌浏览器默认的文字字体是微软雅黑；

### 文本大小font-size（fs）

设置文字字体大小，必须加px单位，其他单位（比如em、cm、mm）也可以但是我们常用px单位；

```css
 font-size: 30px;

```

### 文本粗细font-weight（fw）

html标签有一些标签默认有加粗效果（b、strong、h1-h6），有些没有加粗效果，我们可以通过font-weight来设置是否加粗；

**设置加粗样式**：font-weight取值为bold或者700

```css
   font-weight: bold;
   font-weight: 700;
```

**设置不加粗样式**：font-weight取值为normal或者400

```css
   font-weight: normal;
   font-weight: 400;
```

### 文本倾斜样式font-style （fs）

html标签i和em默认是倾斜样式，但是我们实际开发中很少出现倾斜的文字效果，如果使用i和em我们需要设置不倾斜，或者某些标签需要设置倾斜效果；

我们可以设置i和em不倾斜

```css
        i,
        em {
            font-style: normal;
        }
```

如果想要设置倾斜可以取值为italic

```css
 font-style: italic;
```

### 文本颜色color

设置文字的颜色显示，取值有三种：

01、预定义的英文（red，green，gold）；

02、十六进制取值，必须要用#号链接取值（#ffff00，#000，#f00);

03、rgb(颜色值1，颜色值2，颜色值3)   ----  ，rgb表示红绿蓝( rgb(red, green, blue))，取值为0-255的数字（黑色（0,0,0），白色rgb(255,255,255))；

```css
   /* 预定义英文 */
   color: red;
   /* 16进制取值 */
   color: #f00;
   /* rgb取值 */
   color: rgb(255, 0, 0);
```

### 行间距（行高）line-height  （lh）

设置两行文本之间的距离，也是一行文本的高度；

```css
line-height: 30px;
```

**注意：**如果**设置行高的时候不书写单位最终得到的行高大小是当前文字大小的倍数**，一般我们那会设置较小的倍数，当然我们推荐每一行的行高尽量按照设计稿的实际大小进行设置；

**测量行高的方法：**

**方法1：**从一行文本的开始到另一行文本开始或者从一行文本的结束到另一行文本的结束的高度；

![](D:/%E5%89%8D%E7%AB%AF%E9%9D%A2%E8%AF%95%E8%A7%86%E9%A2%91/%E5%89%8D%E7%AB%AF%E5%AD%A6%E4%B9%A0/JS%E5%AD%A6%E4%B9%A0%E8%B5%84%E6%96%99/%E5%9F%BA%E7%A1%80%E7%8F%AD%E5%AD%A6%E4%B9%A0%E8%B5%84%E6%96%99/%E8%AF%BE%E4%BB%B6/12/css%E7%AC%AC%E4%B8%80%E5%A4%A9/%E4%B8%8A%E8%AF%BE%E7%AC%94%E8%AE%B0/assets/05.png)

**方法2：**UI设计师会给我们提前标注好，直接使用即可，如果没有标注就用方法1来测量即可；

### **单行文本垂直居中**（重点）

设置盒子的**行高等于盒子的高度就可以实现单行文本在盒子中垂直居中**；

![](D:/%E5%89%8D%E7%AB%AF%E9%9D%A2%E8%AF%95%E8%A7%86%E9%A2%91/%E5%89%8D%E7%AB%AF%E5%AD%A6%E4%B9%A0/JS%E5%AD%A6%E4%B9%A0%E8%B5%84%E6%96%99/%E5%9F%BA%E7%A1%80%E7%8F%AD%E5%AD%A6%E4%B9%A0%E8%B5%84%E6%96%99/%E8%AF%BE%E4%BB%B6/12/css%E7%AC%AC%E4%B8%80%E5%A4%A9/%E4%B8%8A%E8%AF%BE%E7%AC%94%E8%AE%B0/assets/06.png)

```html
    <style>
        .loging {
            width: 180px;
            height: 40px;
            background-color: #4e6ef2;
            font-size: 18px;
            color: #fff;
            text-align: center;
            /*设置盒子的行高等于盒子的高度实现垂直居中*/
            line-height: 40px;
        }
    </style>
    <div class="loging">登录</div>
```

### 文本对齐text-align （ta）

设置一个盒子里面的文字对齐方式，默认取值为left，还有center和right取值；

```css
    line-height: 30px;
    /* 左对齐 */
    text-align: left;
    /* 居中对齐 tac */
    text-align: center;
    /* 居右对齐 */
    text-align: right;
```

**注意：**text-align不仅可以**让盒子里面**文字设置对齐方式，也可以给盒子里面的img、a、span、input、button等在一行显示多个的标签设置对齐方式；

![](D:/%E5%89%8D%E7%AB%AF%E9%9D%A2%E8%AF%95%E8%A7%86%E9%A2%91/%E5%89%8D%E7%AB%AF%E5%AD%A6%E4%B9%A0/JS%E5%AD%A6%E4%B9%A0%E8%B5%84%E6%96%99/%E5%9F%BA%E7%A1%80%E7%8F%AD%E5%AD%A6%E4%B9%A0%E8%B5%84%E6%96%99/%E8%AF%BE%E4%BB%B6/12/css%E7%AC%AC%E4%B8%80%E5%A4%A9/%E4%B8%8A%E8%AF%BE%E7%AC%94%E8%AE%B0/assets/19.png)

### 文本缩进text-indent（ti）

网页的文章段落设置首行缩进两个文字的效果；

![](D:/%E5%89%8D%E7%AB%AF%E9%9D%A2%E8%AF%95%E8%A7%86%E9%A2%91/%E5%89%8D%E7%AB%AF%E5%AD%A6%E4%B9%A0/JS%E5%AD%A6%E4%B9%A0%E8%B5%84%E6%96%99/%E5%9F%BA%E7%A1%80%E7%8F%AD%E5%AD%A6%E4%B9%A0%E8%B5%84%E6%96%99/%E8%AF%BE%E4%BB%B6/12/css%E7%AC%AC%E4%B8%80%E5%A4%A9/%E4%B8%8A%E8%AF%BE%E7%AC%94%E8%AE%B0/assets/07.png)

```css
    p {
        text-indent: 2em;
    }
```

**注意：**单位设置可以是px，也可以是em，em单位是一个相对单位，他是相对于当前文字的大小，1em=当前一个文字的大小（比如：文字font-size:30px;那么2em就相当于60px）；

### 文本线条text-decoration（td）

设置文字的下划线、上划线、删除线等样式

**取值有**：none、underline、overline、line-through

**none表示没有线**，一般超链接a浏览器默认会设置对应的下划线，我们可以通过none取值将a默认的下划线去除；

一般情况下我们会将以下代码放在css的最前面，表示将当前页面所有的a的默认下划线全部去除即可；

**没有线 tdn，一般设置在css的最前面，设置为超链接a，让页面中所有的a没有默认的下划线；**

```css
    a {
        text-decoration: none;
    }
```

underline下划线（tdu），overline上划线（tdo），line-through删除线（tdl）

```css
    /* 下划线 tdu */
    text-decoration: underline;
    /* 上划线 tdo */
    text-decoration: overline;
    /* 删除线 tdl */
    text-decoration: line-through;
```

## 文本的综合写法font

实际开发中我们可以将**文字样式font-style、文字加粗font-weight、文字大小font-size、行高line-height，文字字体font-family进行合并书写**，达到简化代码的作用；

**基本语法：**

​    ***font*: font-style  font-weight  font-size/line-height  font-family;**

​    ***font*：是否倾斜 是否加粗 文字大小/行高 字体;**

```css
    /* 
    	font-size: 80px;
    	font-family: '微软雅黑';
    	line-height: 120px;
    	font-style: italic;
    	font-weight: 700; 
    */
    font: italic 700 80px/120px '微软雅黑';
```

**注意：**01、font的书写顺序是不能打乱的；
	     02、如果没有的属性可以省略不写，但是**文字大小和字体必须要存在，否则无效**；





## 复合选择器分类

### 后代选择器（死了都记）

html结构存在嵌套的父子级或者后代关系（比如：ul无序列表）

**基本语法**

 **选择器1    选择器2 {  css样式 }**

01、选择器1相当于父级元素，选择器2相当于后代元素，之间**用空格隔开表示后代关系**；

02、后代元素可以是子元素，也可以是孙子级别的元素，只要有嵌套关系就可以查找到；

```html
  <style>
   ul li {
       color: red;
   }

   .box .son {
       color: green;
   }
  </style>

  <ul>
    <li>我是无序列表</li>
    <li>我是无序列表</li>
    <li>我是无序列表</li>
 </ul>
<div class="box">
    <div class="son"></div>
 </div>
```

**案例：**书写导航的基本结构，设置超链接a的颜色为#333和文字大小为18px；

```html
<div class="nav">
    <ul>
        <li><a href="#">首页</a></li>
        <li><a href="#">产品分类</a></li>
        <li><a href="#">联系我们</a></li>
    </ul>
</div>
```



### 子代选择器（亲儿子选择器）

html结构必须是父子级的嵌套关系，只能选择第一级的嵌套，不会选择里面的孙子；

**基本语法**

 **选择器1>选择器2 {  css样式 }**

01、选择器1相当于父级元素，选择器2相当于子元素，之间**用大于号>连接表示选中第一级的子元素**；

02、后代元素必须是子元素（亲儿子），不可以是孙子级别的元素；

```html
    <style>
        .box>p {
            color: red;
        }
    </style>
    <div class="box">
        <p>我是亲儿子级别的p标签1</p>
        <p>我是亲儿子级别的p标签2</p>
        <p>我是亲儿子级别的p标签3</p>
        <div class="son">
            <p>我是孙子级别的p标签1</p>
            <p>我是孙子级别的p标签2</p>
            <p>我是孙子级别的p标签3</p>
        </div>
    </div>
```

**注意：子元素选择器只能选择嵌套的父子级的子级盒子，可以理解为亲儿子选择器**

### 交集选择器

选中页面中 同时满足 多个选择器的标签，满足**即又的关系**，**主要是可以提高被选择元素的权重**；

**基本语法**

 **选择器1选择器2 {  css样式 }**

01、交集选择器可以更加精准的选择某一个元素，**相当于即又关系**，也就是两个需求都要满足（比如：我要找一个人，这个人是男生并且有个名字叫王  ----  男生老王）；

02、最常用的还是**标签选择器和类选择器的搭配使用**,选择器2也可以是id选择器；

03、交集选择器两个选择器之间是绝对不能书写空格，有了空格就会变成后代选择器；

```html
    <style>
        .list li.san {
            color: red;
        }
    </style>
    <ul class="list">
       <li>我是无序列表1</li>
       <li>我是无序列表2</li>
       <li class="san">我是无序列表3</li>
       <li>我是无序列表4</li>
       <li>我是无序列表5</li>
       <li>我是无序列表6</li>
    </ul>
```

**注意：交集选择器后期经常用来提升元素的选择权重**，以下的代码会选择第二个样式；

```
        .list .san {
            color: green;
        }

        .list li.san {
            color: gold;
        }
```



### 并集选择器

**同时选择多组标签，设置相同的样式**；

如果一些元素样式完全一致，我们可以通过并集选择器合并起来书写，达到代码简化的作用；

**基本语法**

 **选择器1，选择器2 {  css样式 }**

并集选择器我们经常用来**集体声明某一些标签的共有样式**，比如我们经常在css的前面设置i和em标签的倾斜样式为不倾斜方便咱们在页面中使用；

```html
    <style>
        i,
        em {
            font-style: normal;
        }
    </style>
```



### 伪类选择器

#### 基本介绍

所有的html标签都可以设置伪类，我们只需要用英文状态的**冒号( : )将选择器和伪类状态连接**即可；

**基本语法**

 **选择器:伪类状态 {  css样式 }**

**常见的伪类状态有：** :link，:visited ，:hover，:active 四种状态，还有一种特殊专门作用于表单元素获取焦点状态的 :focus伪类选择器。

#### 常见伪类状态（了解）

选择器:link         鼠标未访问的链接（访问前）
选择器:visited    鼠标已访问的链接（访问后）
选择器:hover      鼠标移动到连接上（鼠标经过）
选择器:active      鼠标选定的链接（按下鼠标的时候）

**注意：**如果以上四个状态都要书写必须按照L~V~H~A的顺序来书写，否则就会失去效果；

```html
    <style>
        /* 鼠标访问前 */
        a:link {
            color: red;
        }

        /* 鼠标访问后 */
        a:visited {
            color: green;
        }

        /* 鼠标访问的时候 */
        a:hover {
            color: royalblue;
        }

        /* 鼠标按下的时候 */
        a:active {
            color: tomato;
        }
    </style>

    <a href="#"></a>
```

#### 伪类选择器实际工作的用法（死了都要记）

实际开发中我们不会将伪类的四个状态都书写，我们只需要设置鼠标访问状态:hover即可；

01、统一设置一个超链接a的样式，表示我们四个状态的样式都一致；

02、然后通过样式覆盖的原理，设置鼠标访问:hover的样式即可；

```html
    <style>
        /*01、设置a的四个状态link、visited、hover、active的样式都一致 */
        .nav li a {
            font-style: 18px;
            color: #333;
        }

        /* 02、单独设置鼠标访问经过的样式覆盖前面的样式即可 */
        .nav li a:hover {
            color: red;
        }
    </style>
    <div class="nav">
        <ul>
            <li><a href="#">首页</a></li>
            <li><a href="#">产品分类</a></li>
            <li><a href="#">联系我们</a></li>
        </ul>
    </div>
```

#### focus伪类选择器

用于选取获表单元素的焦点，一般input表单或者文本域textarea才能获取该焦点；

```html
    <style>
        input:focus {
            background: springgreen;
        }

        textarea:focus {
            background-color: thistle;
        }
    </style>

    <input type="text">
    <textarea cols="30" rows="10"></textarea>
```

#### ::placeholder占位符的颜色修改（死了都要记）

我们只能用这样方法修改占位符的颜色，其他样是不能 在这里修改；

```css
        input::placeholder {
            color: red;
        }
```



## 背景属性background

background是一个复合属性，可以用用来设置背景颜色。背景图片等操作；

### 背景颜色（bgc）*background-color*

用来设置元素的背景颜色，取值可以是预定义的英文，16进制取值，rgb取值；

```css
    /* 预定义英文 */
    background-color: red;
    /* 16进制 */
    background-color: #f00;
    /* rgb取值 */
    background-color: rgb(255,0,0);
```

### 背景图（bgi） *background-image*

用来设置元素的背景图片，必须要配合url属性值获取背景图片的路径；

```css
    background-image: url(./img/gAT.gif);
```

### 背景图的平铺方式（bgr）*background-repeat*

插入背景图以后背景图默认是平铺的，我们可以通过*background-repeat*设置不同的取值实现背景图是否平铺；

01、取值为repeat，是默认的取值，背景图会平铺；

```css
background-repeat: repeat;
```

**02、取值为no-repeat，设置背景图不平铺；**

```css
background-repeat: no-repeat;
```

03、可以单独设置水平或者垂直方的单一平铺，取值为repeat-x或者repeat-y

```css
    /* 水平方向平铺 */
    background-repeat: repeat-x;
    /* 垂直方向平铺 */
    background-repeat: repeat-y;
```

### 背景位置设置（bgp）*background-position*

#### 基本语法

设置背景图在元素中的位置

![](D:/%E5%89%8D%E7%AB%AF%E9%9D%A2%E8%AF%95%E8%A7%86%E9%A2%91/%E5%89%8D%E7%AB%AF%E5%AD%A6%E4%B9%A0/JS%E5%AD%A6%E4%B9%A0%E8%B5%84%E6%96%99/%E5%9F%BA%E7%A1%80%E7%8F%AD%E5%AD%A6%E4%B9%A0%E8%B5%84%E6%96%99/%E8%AF%BE%E4%BB%B6/12/css%E7%AC%AC%E4%BA%8C%E5%A4%A9/%E4%B8%8A%E8%AF%BE%E7%AC%94%E8%AE%B0/assets/02.png)

默认取值为0,0，表示背景图就在元素的左上角；

```css
background-position: 0 0;
```

#### 取值为方位名词（了解）

水平方向：left、center、right；

垂直方向：top、center、bottom；

```css
     /* 左下角 */
     background-position: left bottom;
     /* 左上角 */
     background-position: left top;
     /* 右下角 */
     background-position: right bottom;
     /* 右上角 */
     background-position: right top;

     /* 顶部和底部水平居中  */
     background-position: center top;
     background-position: center bottom;
     /* 左侧和右侧垂直居中 */
     background-position: left center;
     background-position: right center;

     /* 水平垂直居中 */
     background-position: center center;
     /* 简写 */
     background-position: center;

```

#### 取值为实际像素

取值为两个实际像素，让背景图在我们预定义好的位置显示；

```css
background-position: 100px 100px;
```

如果取值为一个值，那么这个值是表示左右的水平位置，垂直方向的位置默认居中显示；

```css
 background-position: 80px;
```

#### 取值为百分比

取值为百分计算的值是按照父级盒子宽高计算的；

```css
background-position: 50% 50%;
```

如果取值为一个值，那么这个值是表示左右的水平位置，垂直方向的位置默认居中显示；

### 背景固定（bga）background-attachment 

设置背景图片是否跟随内容滚动；

**默认取值scroll滚动**

```css
background-attachment: scroll；
```

**不滚动 fixed**

```css
background-attachment: fixed；
```

### 背景属性综合写法1（死了都要记）	

**基本语法**

![](D:/%E5%89%8D%E7%AB%AF%E9%9D%A2%E8%AF%95%E8%A7%86%E9%A2%91/%E5%89%8D%E7%AB%AF%E5%AD%A6%E4%B9%A0/JS%E5%AD%A6%E4%B9%A0%E8%B5%84%E6%96%99/%E5%9F%BA%E7%A1%80%E7%8F%AD%E5%AD%A6%E4%B9%A0%E8%B5%84%E6%96%99/%E8%AF%BE%E4%BB%B6/12/css%E7%AC%AC%E4%BA%8C%E5%A4%A9/%E4%B8%8A%E8%AF%BE%E7%AC%94%E8%AE%B0/assets/08.png)

注意：01、属性值没有书写顺序，没有的属性可以省略不写；
           02、属性值和属性值之间用空格隔开；

```css
  /* background-color: magenta; */
  /* background-image: url(./img/icon.png); */
  /* background-repeat: no-repeat; */
  /* background-position: 5px center; */
  /* background: 背景颜色   背景图片地址   背景平铺   背景图像滚动   背景图片位置; */
  background: magenta url(./img/icon.png) no-repeat 5px center;
```

### 背景尺寸设置（bgs）*background-size*

如果背景图片小于当前的盒子或者大于当前的盒子，设置背景图的尺寸大小；

#### 取值为cover（常用）

背景图等比缩放，一直到铺满整个盒子

```css
background-size: cover;
```

注意：该属性取值如果背景图和盒子比例不一致。可能会导致背景图过大超出盒子显示不全，溢出隐藏；

#### 取值为contain 

背景图等比缩放，直到背景图的宽或者高和盒子一致就停止缩放

```css
background-size: contain;
```

注意：该属性取值如果背景图和盒子比例不一致可能会导致背景图不会完全铺满盒子；

#### 取值为实际像素大小（移动端小图标常用）

设置背景图大小固定

```css
background-size: 45px 45px;
```

案例：苏宁易购移动端小图标

### 背景属性综合写法2（了解）

语法

![](D:/%E5%89%8D%E7%AB%AF%E9%9D%A2%E8%AF%95%E8%A7%86%E9%A2%91/%E5%89%8D%E7%AB%AF%E5%AD%A6%E4%B9%A0/JS%E5%AD%A6%E4%B9%A0%E8%B5%84%E6%96%99/%E5%9F%BA%E7%A1%80%E7%8F%AD%E5%AD%A6%E4%B9%A0%E8%B5%84%E6%96%99/%E8%AF%BE%E4%BB%B6/12/css%E7%AC%AC%E4%BA%8C%E5%A4%A9/%E4%B8%8A%E8%AF%BE%E7%AC%94%E8%AE%B0/assets/10.png)

我们也可以把背景尺寸设置给到综合写法中，用 / 隔开连接即可，但是必须要有background-position值，哪怕是0也要书写，否则综合写法失效；

```css
background: red url(./img/01.gif) no-repeat 0 0 / cover;
```

实际开发中我们建议分开写，不容易出错哦！并且如果background-position值为0就可以直接省略；

```css
/* background: red url(./img/01.gif) no-repeat 0 0; */
background: red url(./img/01.gif) no-repeat;
background-size: cover;
```

## 四、背景颜色透明rgba（死了都要会）

我们可以设置背景颜色的透明度从而实现透明效果；

**语法： rgba(red, green, blue, alpha)**

alpha取值为0-1之间，0表示完全透明，1表示不透明，之间的数字表示透明的程度

```css
background-color: rgba(0,0,0,.5);
```

**注意：**rgba只能设置背景颜色透明不会影响盒子里面的内容透明；

![](D:/%E5%89%8D%E7%AB%AF%E9%9D%A2%E8%AF%95%E8%A7%86%E9%A2%91/%E5%89%8D%E7%AB%AF%E5%AD%A6%E4%B9%A0/JS%E5%AD%A6%E4%B9%A0%E8%B5%84%E6%96%99/%E5%9F%BA%E7%A1%80%E7%8F%AD%E5%AD%A6%E4%B9%A0%E8%B5%84%E6%96%99/%E8%AF%BE%E4%BB%B6/12/css%E7%AC%AC%E4%BA%8C%E5%A4%A9/%E4%B8%8A%E8%AF%BE%E7%AC%94%E8%AE%B0/assets/11.png)

## 盒子透明opacity

**语法： *opacity*: 透明值；**

opacity 设置盒子的透明，取值为0-1之间，0表示完全透明，1表示不透明，之间的小数表示透明的程度

```css
 opacity: .5;
```

**注意：**用opacity 设置透明，不仅让背景颜色透明，也会影响盒子里面的内容也跟着透明，所以我们不建议使用，后期在制作css3的动画时会用到；

![](D:/%E5%89%8D%E7%AB%AF%E9%9D%A2%E8%AF%95%E8%A7%86%E9%A2%91/%E5%89%8D%E7%AB%AF%E5%AD%A6%E4%B9%A0/JS%E5%AD%A6%E4%B9%A0%E8%B5%84%E6%96%99/%E5%9F%BA%E7%A1%80%E7%8F%AD%E5%AD%A6%E4%B9%A0%E8%B5%84%E6%96%99/%E8%AF%BE%E4%BB%B6/12/css%E7%AC%AC%E4%BA%8C%E5%A4%A9/%E4%B8%8A%E8%AF%BE%E7%AC%94%E8%AE%B0/assets/12.png)

## 盒子显示模式

### 什么是元素的显示模式？

元素（标签）默认以什么方式进行显示，都是盒子显示模式的原因，比如div盒子独自占一行，span标签一行放多个；

### 元素显示模式分类

元素的显示模式分为三类分别是块元素、行内元素，行内块元素；

#### 块元素

**常见的块元素：**div/p/ul/li/ol/dl/dt/dd/h标题等

**特点：** 01、独自占一行；

   	  02、如果不设置固定的宽度，块元素默认的宽度和父级盒子一样宽；

​	      03、给块元素设置内外边距，宽高都生效；

​	      04、块元素里面可以嵌套任何元素，但是段落标签p里面不能嵌套div标签，因为浏览器解析的时候会将p      		        嵌套div解析成两个p标签，一个div标签显示；

![](D:/%E5%89%8D%E7%AB%AF%E9%9D%A2%E8%AF%95%E8%A7%86%E9%A2%91/%E5%89%8D%E7%AB%AF%E5%AD%A6%E4%B9%A0/JS%E5%AD%A6%E4%B9%A0%E8%B5%84%E6%96%99/%E5%9F%BA%E7%A1%80%E7%8F%AD%E5%AD%A6%E4%B9%A0%E8%B5%84%E6%96%99/%E8%AF%BE%E4%BB%B6/12/css%E7%AC%AC%E4%BA%8C%E5%A4%A9/%E4%B8%8A%E8%AF%BE%E7%AC%94%E8%AE%B0/assets/13.png)

#### 行内元素

**常见的行内元素：**a /span/ u/s /del/ strong/em/i / ins

**特点：**01、一行共存多个；

​	    02、默认的宽是由内容多少撑开的；

​	    03、给行内元素直接设置宽高是不生效的，设置内外边距上下不生效，左右生效；

​	    04、行内元素中只能嵌套文本图片或者其他行内元素，但是**超链接a里面可以嵌套块级元**素；

#### 行内块元素

**常见的行内元素：**img/input/button;

**特点：** 01、一行可以共存多个；

​            02、如果不设置宽度，默认的宽是由内容多少撑开的；

​	    03、给行内块元素设置宽高和内外边距都生效；

### 元素显示模式之间的转化display（死了都要记）

实际开发中各个元素的显示模式是可以通过display设置不同的属性值实现的；

#### ****将元素转化为块元素（重点）   display:block;

#### 将元素转化为行内元素      display:inline;**     

#### ****将元素转化为行内块元素     display:inline-block;