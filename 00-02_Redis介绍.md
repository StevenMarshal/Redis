# 2 Redis介绍

Redis is an open source, advanced key-value store. It is often referred to as a data structure server since keys can contain strings, hashes, lists, sets and sorted sets.  

Redis是一个开源的，先进的key-value存储。它通常被称为数据结构服务器，因为键可以包含字符串、哈希、列表、集合和 有序集合。

Redis是一个Key-Value存储系统。它支持存储的value类型很多，包括string（字符串）、list（链表）、set（集合）、zset（有序集合）。这些数据类型都支持push/pop、add/remove及取交集和并集及更丰富的操作，Redis支持各种不同方式的排序。为了保证效率，数据都是缓存在内存中，它也可以周期性的把更新的数据写入磁盘或者把修改操作写入追加的记录文件。

提供的API语言包括：  
C、C++、C#、Clojure、Common Lisp、Erlang、Haskell、Java、Javascript、Lua、Objective-C、Perl、PHP、Python、Ruby、Scala、Go、Tcl。

目前全球最大的Redis用户是新浪微博，在新浪有200多台物理机，400多个端口正在运行着Redis，有+4G的数据在Redis上来为微博用户提供服务。  

在新浪微博Redis的部署场景很多，大概可以分为如下两种：  
1：应用程序直接访问Redis数据库。  
2：应用程序直接访问Redis，只有当Redis访问失败时才访问MySQL。

Redis具体的适用场景：  

1：取最新N个数据的操作  
比如取最新500篇文章等。  

2：排行榜应用，取TOP N操作  
比如通过某种筛选后进行数据操作。  

3：需要精确设定过期时间的应用  
Redis可以对key进行设置过期，就是多长时间有效。  

4：计数器应用  

5：Uniq操作，获取某段时间所有数据排重值  

6：实时系统，反垃圾系统  

7：Pub/Sub构建实时消息系统。
Pub/Sub（发布与订阅）是Redis独有的消息系统。  

8：构建队列系统  

9：缓存

Redis与MySQL的区别点：  
1：两者都有库的概念。  
2：MySQL有表的概念，而Redis没有。  
3：MySQL有字段、行和列的概念，而Redis没有。  
