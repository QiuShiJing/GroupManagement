

# Week1

## 3.16

###已完成任务


* 组内第一次会议
  * 成员自我介绍：技术背景、目标
  * 组内规则确认
  
    1.每日固定北京时间完善八点集中讨论问题
    
    2.有任何问题先通过搜索引擎找过答案，明确描述问题是什么（进行何种操作后出现何种结果），描述进行过的尝试，解决后将问题写入教程中
    
  * 同步本周任务
* 更新本组GroupManagement文件夹的内容，添加成员名单和本周作业


## 3.17

组里今日主要是解决大家在基础配置中的问题

* L的SSH问题
* cici的gitbook同步的问题

## 3.18

* 确认一下大家同步的进度
* 建立本组的库
	* 作业打卡
	* 每日日志
* 每日固定时间调整到北京时间九点  
- [x] 已阅。 Mar.19 10:36 Yixuan


# 第一周总结

本周主要完成任务

* 小分队组建，实行每周固定时间讨论的工作方法
* 成员基本完成首周各项任务

存在不足

* 每日log未记录完。原因：后面几天都是解决具体一些小问题，就没有来得及记录。
* 每日讨论不够高效，没有沉淀。

解决措施

* 每日log随手记
* 引导尝试issues的提问方式

第二周主要事项

* 组里一起刷完IIPPy-part1
* 探索更好的小组互助模式

-------------------------
# Week2

## 3.23

确认已经注册的同学：

* 叶舟
* tornote
* 袅袅
* L
* ZSISI
* 糖糖糖
* 阡陌

## 3.24

* 小组**糖糖糖**已经完成作业
* 督促大家跟上进度，交流快速刷题方法

## 3.25

* 小组赶死线ing


## 3.26
* 5位组员冲过死线
* 继续优化代码

# week2 总结

* 我上周做了什么

	- 自己完成作业
	- 鼓励、敦促组员完成作业
* 我这周打算做什么
	- 组内争取在规定时间完成作业
	- 增加作业交流环节
	- 增加典型问题交流环节
* 我遇到了什么困难？
- 时间不够，组员自发会沟通代码，但是主动引导和总结不够。


* 待解决的问题
 - gitbook的问题
 - return的用法
 
附上各成员总结

@ 叶舟

我上一周编了自己的第一个Python程序，学会了做按钮，界面，还有写条件语句。
这一周要完成本周作业，争取做到天才级别，不能像这一周没有惊喜
遇到的困难：没有理解全局和局部变量，还有return的用法。感觉Python有些东西会用但是讲不出来

@cici

我上周写了第一个程序。
这周要周三前完成本周作业，然后把教程补完。而且如果要熟悉python 那么要把coursera课程中的习题尽量多的练一练。
遇到的困难：也是return的用法。我为了避免出错是每个方法下面都写。

@L

我上周写了猜数字的程序；试了下双推，以失败告终；Github也不知道怎么推上去，本地已经有了库了，但是弄不上去。      这周打算把新的程序写了，再弄弄github gitbook什么；听完大妈的QA。       写Python有的东西似懂非懂，比如Return什么的；困难还有Github Gitbook的双推和Github的单推（暴露了我第一周东西还没弄完==

@糖糖糖

我上周就写了那个作业，下周打算慢慢写新作业，问题是还不知道怎么自定义GUI界面…

--------------

## 

Return的使用问题
## 3.30 

- 引导组员总结上周
- 讨论关于return的使用问题，并放在issue上沉淀讨论内容

https://github.com/sunmmy/6godspy/issues/5



不知道什么时候用return，return写完写啥？

@ 糖糖糖

要对外返回值的时候用return
返回空值代表强行结束函数，也用return

@叶舟
我理解对于整个程序来说，单一函数是一个黑箱，从程序这一层看就是y=f(x)，所以如果下面的步骤要用要产出的y就必须return一下

@糖糖糖

不需要返回值就不要了啊
有啊，比如改global值
改list也不用返回值

http://sebug.net/paper/python/ch07s06.html

	def f(x):
    x=x+1
    print x
    
	x=1
	f(x)
	print x
	
	def f(x):
    x=x+1
    print x
    return x
    
	x=1
	f(x)
	print x

这两个的结果一样，显然return是没用的

	def f(x):
    x=x+1
    print x
    return x
    
	x=1
	x=f(x)
	print x

但这样结果就不一样了，大家可以看看
三个例子，第一和第二个的输出都是2，1，第三个的输出是2，2

@ 叶舟 

因为第三个实际上是把fx的运算结果赋值给了x，但前两个fx运行完变化的是局部的x，这个函数运行完了不影响原来x的值
但很奇怪为什么第二个不是2、2因为最后一步return x不是把现在算出来的x(2)返回给了程序么，那么程序下一步print x怎么还是1

@ 糖糖糖 

return是return了，但是没人接受啊
第三个例子里外面的x去接了那个return

    def f(x):
      x=x+1
      print x
      return x
    
	x=1
	print f(x)
	print x

这个的输出是2，2，1，因为print f(x)这里是print接受了return的值

@叶舟

这么理解对不对，fx是厨师，把做好的菜return了，就是放到取菜台子上，但是程序没有安排服务员变量x去取菜，所以最后的结果顾客吃的还是原来的菜！


待解决：

gitbook 的问题

@cici 我也有个问题是 我双推虽然好了 但是在Github写了东西之后 打开gitbook编辑时也能看到同步了  但打开发布的书 就是一开始推上去的样子 还有俩错别字


# 4.7

问题讨论，整理BY@叶舟

## 操作技巧
**cici：**

- 我在学coursera课的时候 发现Scott可以直接用#前缀很多行代码 把暂时不用的代码变成注释 然后我找了一下 是ctrl-k 可以把多行代码变成注释  ctrl-shift-k 再变回来 在调试代码的时候很方便 
- 有时候不小心删了 command-z可以撤销回来

## dispus
**蝈蝈：** [wiki链接](https://github.com/rosing/pythoncamp0/blob/master/wiki/disqus.md)

- 找到了一个靠谱的做法 

1. 修改gitbook书根目录下的book.json文件 

`{
"plugins":[
"disqus"
],
"pluginsConfig":{
"shortName":"rosinggitbook"
} 
}`

2. 在disqus网站添加信任域
位置：setting - advanced - Trusted Domains
填入：gitbook.com,gitbook.io

## codeskulpter在线保存
**叶舟：**点击下载，跳转界面后右键，选择“存储为”

## 新建md文件
**叶舟：**直接点击macdown／mou图标，或者command＋n
**糖糖糖：**终端运行touch命令
**蝈蝈：**ubuntu下直接新建文件，改后缀名

## gitbook问题：
**蝈蝈：**[教程](http://rosing.gitbooks.io/python/content/)
        
 记得写summary.md
 
 **叶舟：**双推经常不管用，所以用以下命令单独推一次到gitbook：
 `git remote add gitbook https://git.gitbook.com/username/repname.git`
`git push -f -u gitbook master`


