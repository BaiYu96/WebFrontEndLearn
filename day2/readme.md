## 创建偶像主页

    date:2019/11/23
    by:baiyu
    用时：4个小时

### 前言

上一篇简单浏览了一下前端的相关背景知识和概念，这次便开始动手做一个自己偶像的主页。本篇用到的是HTML+CSS。

### 代码与解释

#### day2.html代码如下：

	<html>
	    <head>
	        <link rel="stylesheet" type="text/css" href="day2.css">
	    </head>
	    <body>
	        <div class="titleName">
	           <h1>Michael Jackson</h1> <img src="./MJ.jpg">           
	        </div><hr>
	        <div id="introduction">
	            <h2>简介</h2>
	            <p>
	                1958年8月29日 ~ 2009年6月25日
	            </p>
	         </div><hr>
	        <div>
	
	        </div>
	        <div>
	            <h2>个人生活</h2>
	            <p>
	                迈克尔·杰克逊（Michael Jackson，1958年8月29日～2009年6月25日），出生于美国印第安纳州加里市，美国男演唱家、词曲创作人、舞蹈家、表演家、慈善家、音乐家、人道主义者、和平主义者、慈善机构创办人。
	                杰克逊是家族的第七个孩子，他在1964年作为杰克逊五人组的成员和他的兄弟一起在职业音乐舞台上初次登台，1968年乐队与当地的一家唱片公司合作出版了第一张唱片《Big Boy》。1971年12月，发行了个人首支单曲《Got to be there》，标志着其个人独唱生涯的开始。
	                1982年12月，杰克逊音乐生涯最畅销的专辑《Thriller》发行。1987年9月，杰克逊展开个人首次全球巡演。通过舞台和视频的表演，杰克逊普及了一些像机械舞和太空步等舞蹈技术。杰克逊一生中获得了13个格莱美奖和26个全美音乐奖。在他单飞生涯中，他拥有13支美国冠军单曲。2000年吉尼斯世界纪录大全里认证他资助过39个慈善机构。
	                2009年5月，杰克逊宣布将在伦敦举行系列音乐会。2009年6月25日，他因为急性丙泊酚和苯二氮平类药物中毒导致心脏骤停不幸身亡，终年50岁。洛杉矶法医裁定这是一宗凶杀案，他的私人医生康拉德·莫里被判定过失杀人罪，服刑四年监禁。2010年，迈克尔·杰克逊被授予格莱美终生成就奖。    
	            </p>
	        </div><hr>
	        部分获奖信息
	        <table border="1" cellpadding="10">
	            <tr>
	                <th>年份</th>
	                <th>获得奖项</th>
	            </tr>
	            <tr>
	            <td>2010</td>
	            <td>格莱美终生成就奖</td>
	            </tr>
	            <tr>
	             <td>1995</td>
	              <td>最佳短篇音乐录像带</td>
	            </tr>
	            <tr>
	            <td>1993</td>
	            <td>当代传奇奖</td>
	            </tr>
	            <tr>
	            <td>1985</td>  
	            <td>年度歌曲奖</td>
	            </tr>
	            </table>
	        <address>
	            Written by baiyu.<br> 
	            Visit us at:<br>
	            <a href="https://github.com/BaiYu96/WebFrontEndLearn">https://github.com/BaiYu96/WebFrontEndLearn</a> <br>
	            China
	        </address>
	    </body>
	</html>

从上到下看到的标签依次解释
`<html> 与 </html> 之间的文本描述网页`

`<head></head>定义文档的头部，它是所有头部元素的容器。<head> 中的元素可以引用脚本、指示浏览器在哪里找到样式表、提供元信息等等。`
`<link></link>标签定义文档与外部资源的关系,这里我是链接了我的样式表`

`<body> 与 </body> 之间的文本是可见的页面内容`

`<div></div>之间定义文档中的分区或节，可以把文档分割为独立的、不同的部分。然后用不用的class，id进行标记，这个可以在使用样式表的时候可以整个区域进行修改`

`<h1> 与 </h1> 之间的文本被显示为一级标题`

`<hr>是画出一条水平线`

`<h1> 与 </h1> 之间的文本被显示为二级标题`

`<p> 与 </p> 之间的文本被显示为段落`

`<table></table>之间是表格`

`<th>是定义表头`

`<tr>是定义表格的行`

`<td>定义表格单元`

`<address></address>之间是定义文档或文章的作者/拥有者的联系信息`

`<a></a>这个标签用于定义超链接，标签之间是超链接显示的名字，href参数是设置超链接的目标`

如果想更多相关标签的信息，请参阅，W3Cschool的[HTML参考手册](https://www.w3school.com.cn/tags/index.asp)

#### day2.css代码如下：

	/* .是class 选择器，用来匹配相同class类的标签 */
	.titleName {
	    color: yellow;
	    font-size: 35px;
	}
	/* #号是id 选择器， 用来匹配id名称的标签 */
	#introduction {
	    color: blue;
	    font-size:24px;
	}
	/* 也可以直接选中标签*/
	p{
	  color:pink ;  
	}
css里面的类名跟id号，与你要改变html对应标签的类名或者id号要对应

* 类的选择器我们用井号（#），使用格式：#className{}

* id的选择器我们用点（.），使用格式： .idNumber{}
* 也可以是直接选中标签，例如选中p标签：p{}

在day2.html文件中调用day2.css文件的方法就是在`<head>`标签里面添加`<link>`标签，关联css文件

	<head>
	    <link rel="stylesheet" type="text/css" href="day2.css">
	</head>