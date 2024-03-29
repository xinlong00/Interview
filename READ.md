![优秀的Bug总要优秀的人来写](https://ss3.bdstatic.com/70cFv8Sh_Q1YnxGkpoWK1HF6hhy/it/u=1821742704,3547241851&fm=27&gp=0.jpg)

Linux查询端口号：**

1、lsof -i:端口号

2、netstat -tunlp|grep 端口号

******************************************

**Linux查询进程**

1.ps -ef | grep 进程关键字

************

**Linux结束进程**

1.kill -9 [PID]	# -9标识强迫进程立即停止

********

**Linux安装软件包**

1.管理员身份下使用apt-get install package

**********

**Linux更新源**

1.apt-get update

*************

Linux搜索软件包

1.apt-cache search package

************

**介绍SpringBoot**

1.创建独立的Spring应用程序，简化Maven配置，可以自动配置Spring，有着开箱即用，没有代码生成也无序XML配置，他不是Spring功能的增强，只是提供了快速使用Spring的方式

**********

**常用的集合**

1.List集合：ArrayList，LinkedList，Vector，Stack

2.Map集合：HashMap类，HashTable类

3.Set集合：HashSet，TreeSet

*****

**Redis中五种数据类型及方法**

1.数据类型：字符串类型string，散列类型hash，列表类型list，集合类型set，有序集合类型zset

2.几个基本的命令

（KEYS * 获取当前数据库的所有键）

（EXISTS keyName 判断键是否存在，返回个数）

（DEL keyName 删除键，返回删除个数）

（TYPE keyName 获取减值的数据类型）

（FLUSHALL 清空所有数据库）

（CONFIG [get、set] redis配置）

******

HTTP协议

1.HTTP协议是超文本传输协议，给予TCP/IP通信协议来传递数据，是一个属于应用层的面向对象的协议，适用于分布式超媒体信息系，此协议简单快速，无连接，无状态，支持B/S和C/S模式。

******

MQ用在哪里

1.可以应用于秒杀活动，秒杀活动因为流量过大，会导致流量暴增，严重会导致应用挂掉，可以用MQ在应用前端加入消息队列，可以控制活动的人数，还可以防止短时间内大流量压垮应用。

2.可以实现消息通讯，消息队列有高效的通信机制，可以实现点对点消息队列或聊天室等。

用户请求 ———> 消息队列 ———> 秒杀业务处理

*******

HashMap

1.HashMap是由数组和链表结构组成，查找的时候比纯链表快，插入删除币纯数组快，还可以解决HashCode冲突，当我们在第一次Put元素的时候他会触发数组的初始化。

<u>HashCode：hashCode方法就是根据一定的规则将与对象相关的信息（比如对象的存储地址，对象的字段等）映射成一个数值，这个数值称作为散列值</u>

******

Redis默认端口：6370

Redis默认密码：没有

**********

MySQL调优（选择性记点）

1.通过EXPLAIN可以知道MySQL是如何处理SQL语句的，这可以分析查询语句或表结构的性能瓶颈。

2.开启查询缓存，查询一条数据的话使用 LIMIT 1

3.为经常搜索的字段建立索引，但是在一大篇文章中搜索一个词的时候用索引可能没什么意义。

4.在大数据量下取随机不连续的数据的时候，千万不要用ORDER BY RAND() ，用LIMIT 1也没用。这个血的教训：曾经在大数据量使用此方法造成多次爆CPU，如果是需要大数据量取随机数据的话，可以建立第三个字段，用前两个字段UPDATE的时候计算第三个字段，然后通过第三个字段进行随机筛选，不过局限性比较大。也可以在程序内获取总数据量，然后取不重复的随机数，通过where in方式来获取。

5.避免使用SELECT *

6.为每张表都设置一个ID作为主键

7.大部分情况下，能不用NULL就不用NULL

********

后续继续更新...