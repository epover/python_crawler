![](code/spider-5.png)

### 什么是网络爬虫？

网络爬虫（又称为网页蜘蛛，网络机器人，在FOAF社区中间，更经常的称为网页追逐者），是一种按照一定的规则，自动地抓取万维网信息的程序或者脚本。另外一些不常使用的名字还有蚂蚁、自动索引、模拟程序或者蠕虫。

### 爬虫分类
1.通用网络爬虫(Scalable Web Crawler)
 
 通用网络爬虫的结构大致可以分为页面爬行模块、页面分析模块、链接过滤模块、页面数据库、URL 队列、初始 URL 集合

（1）深度优先策略:按照深度又低到高的顺序，依次访问下一级网页链接，这种策略比较适合垂直搜索或站内搜索。

（2）广度优先策略:按照网页内容目录层次深浅来爬行页面，处于较浅目录层次的页面首先被爬行。这种策略能够有效控制页面的爬行深度。

2.聚焦网络爬虫(Focused Crawler)

 选择性爬行那些与预先定义好的主题相关页面的网络爬虫

（1）基于内容评价的爬行策略：将用户输入查询词作为主题，包含查询词的页面被视为与主题相关，起局限性在于无法评价页面与主题相关度的高低。

（2）基于链接结构评价的爬行策略：通过计算每个已访问页面的Authority权重和Hub权重，并依次决定链接的访问顺序。

（3）基于增强学习的爬行策略：Rennie 和 McCallum 将增强学习引入聚焦爬虫，利用贝叶斯分类器，根据整个网页文本和链接文本对超链接进行分类，为每个链接计算出重要性，从而决定链接的访问顺序。

（4）基于语境图的爬行策略：通过建立语境图学习网页之间的相似度，训练一个机器学习系统，通过该系统可计算当前页面到相关Web页面的距离，距离越近的页面中的链接优先访问。

3.增量式网络爬虫(Incremental Web Carawler)
 指对已下载网页采取增量式更新和只爬行新产生的或者已经发生变化网页的爬虫，它能够在一定程度上保证所爬行的页面尽可能新的页面。
 常用的方法有：
    （1）统一更新发
    （2）个体更新发
    （3）基于分类的更新法

4.Deep Web爬虫(Surface Web)
 Deep Web 是那些大部分内容不能通过静态链接获取的、隐藏在搜索表单后的，只有用户提交一些关键词才能获得的 Web 页面。
 Deep Web 爬虫体系结构包含六个基本功能模块 （爬行控制器、解析器、表单分析器、表单处理器、响应分析器、LVS 控制器）和两个爬虫内部数据结构（URL 列表、LVS 表）。 其中 LVS（Label Value Set）表示标签/数值集合，用来表示填充表单的数据源。
 Deep Web爬虫爬行过程中表单填写类型：
    （1）基于领域知识的表单填写
    （2）基于网页结构分析的表单填写

### 爬虫核心
 1. 爬取网页数据
 2. 解析数据
 3. 爬虫和反爬之间的博弈

### 爬虫用途
 1. 数据分析/数据源
 2. 社交软件冷启动
 3. 竞争对手监控
 4. 舆情监控

![](code/spider-10.jpeg)

### 反爬手段
 1. robots.txt 协议： robots.txt是一种存放与根目录下的ASCCI编码的文本文件，它通常搞忘网络蜘蛛，此网站中的哪些内容是不应被网络蜘蛛爬取的，哪些是可以被网络蜘蛛爬取的。
 > 这个协议也不是一个规范，而只是约定俗成的，有些搜索引擎会遵守这一规范，有些则不然。