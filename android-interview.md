## android 面试题集锦

### Android部分
1. Android事件分发机制。
2. Android View 绘制机制和加载过程。
3. Activity加载过程 Activity启动模式 Activity缓存方式。
4. Service生命周期，启动方式，区别。如何保证service不被杀死。
5. 广播的注册方式和差别。
8. Handler Looper消息队列模型，各部分作用。
9. Binder原理.
10. Android 权限管理
11. android术语
    >* ActivityManagerServices
    >* ActivityThread
    >* ApplicationThread
    >* ApplicationThreadProxy
    >* Instrumentation
    >* ActivityStack
    >* ActivityRecord
    >* TaskRecord
11. 理解Window和WindowManager
12. 安卓采用自动垃圾回收机制，请说下安卓内存管理的原理
12. 说下安卓虚拟机和java虚拟机的原理和不同点
12. Bitmap的处理
13. Android的优化 还有兼容 屏幕适配
14. 多线程和安全。线程并发，通信，同步。单列类线程同步。
15. Intent可以传递哪些数据类型。
7.  动画有哪几类，特点。
15. 怎样退出App。
16. Json有什么优劣势
17. Asset目录与res目录的区别。
17. 插件化框架（dynamicLoadApk）和 热修复框架（Anfix）
18. JNI调用过程 混淆问题
19. Merge与ViewStub布局标签
20. Android长连接，怎么处理心跳机制
20. Activity卡顿原因
21. Zygote进程启动过程
22. Scroller原理
23. Android几种进程
24. 五种布局： FrameLayout 、 LinearLayout 、 AbsoluteLayout 、 RelativeLayout 、 TableLayout 各自特点及绘制效率对比
25. ContentProvider的权限管理(读写分离，权限控制-精确到表级，URL控制)

### Java部分
1. 类加载器 反射
2. abstract和interface的区别?
3. array,arrayList, List ,三者有何区别？
4. hashtable和hashmap的区别,并简述Hashmap的实现原理
5. StringBuilder和String,subString方法的细微差别
7. 解释下java的高内聚和低耦合
8. spring 的反射和代理，在安卓中应用场景（插件和ROM数据框架）
9. equals 与 hashCode 的异同点在哪里？Java 的集合中又是如何使用它们的。
10. 描述下 Java 中集合（Collections），接口（Interfaces），实现（Implementations）的概念。LinkedList 与 ArrayList 的区别是什么？
11. 基础类型（Primitives）与封装类型（Wrappers）的区别在哪里？
12. final 与 static 关键字可以用于哪里？它们的作用是什么？
13. 阐述下 Java 中的访问描述符（Access Modifiers）。
14. 描述下 String,StringBuilder 以及 StringBuffer 区别。
15. 覆盖（Overriding）与重载（OverLoading）的区别在哪里。
16. 异常分为哪几种类型？以及所谓的handle or declare原则应该如何理解？
18. 你是如何处理内存泄露或者栈溢出问题的？
19. 如何构建不可变的类结构？关键点在哪里？
20. 什么是 JIT 编译？
21. Java 8 / Java 7 为我们提供了什么新功能？即将到来的 Java 9 又带来了怎样的新功能？
22. JVM
    >* CAS是什么？
    >* GC收集器有哪些？CMS收集器与G1收集器的特点。
    >* GC的三种收集方法：标记清除、标记整理、复制算法的原理与特点，分别用在什么地方，如果让你优化收集方法，有什么思路？
    >* 内存模型以及分区，需要详细到每个区放什么
    >* 判断一个对象是否存活
    >* 双亲委派模型 Bootstrap ClassLoader、Extension ClassLoader、ApplicationClassLoader
    >* GC的两种判定方法：引用计数与引用链。
    >* 对象的创建、内存布局、对象的访问定位
    >* 新生代老年代内存划分比例及其各自特点
    >* 类加载的五个过程 加载、验证、准备、解析、初始化。
    >* 静态分派和动态分派
    >* Minor GC与Full GC分别在什么时候发生？
    >* 几种常用的内存调试工具：jmap、jstack、jconsole。
    >* 简述字节码文件组成
23. Java中的四种引用及其应用场景是什么？
24. Switch能否用string做参数？
25. Object有哪些公用方法？
26. equals与==的区别
27. Map、Set、List、Queue、Stack的特点与用法
28. TreeMap、HashMap、LindedHashMap的区别。
29. Collection包结构，与Collections的区别。
30. Excption与Error包结构。OOM你遇到过哪些情况，SOF你遇到过哪些情况。
31. Java面向对象的三个特征与含义。
32. java多态的实现原理。
33. 线程同步的方法：sychronized、lock、reentrantLock等
34. 锁的等级：方法锁、对象锁、类锁
35. 写出生产者消费者模式。
25. ThreadLocal的设计理念与作用。
26. ThreadPool用法与优势。
27. Concurrent包里的其他东西：ArrayBlockingQueue、CountDownLatch等等。  
28. wait()和sleep()的区别。
29. foreach与正常for循环效率对比。
30. java IO与NIO
31. 反射的作用于原理。
32. 泛型常用特点，List<String>能否转为List<Object>。
33. 解析XML的几种方式的原理与特点：DOM、SAX、PULL。
34. Java与C++对比。
36. 设计模式：单例、工厂、适配器、责任链、观察者等等。
37. JNI的使用
38. Static class 与non static class的区别。
39. 不同情形下return和finally的执行顺序
40. 如何控制某个方法允许并发访问线程的个数
41. 泛型原理，举例说明；解析与分派
42. 抽象类与接口的区别；应用场景；抽象类是否可以没有方法和属性
43. 静态属性和静态方法是否可以被继承？是否可以被重写？以及原因？
50. 服务器只提供数据接收接口，在多线程或多进程条件下，如何保证数据的有序到达


### 网络部分
1. 多线程多点下载的过程
2. http协议的理解和用法
3. socket短线重连怎么实现，心跳机制又是怎样实现，四次握手步骤有哪些
4. http相关
    >* http中TCP和UDP有啥区别，说下HTTP请求的IP报文结构
    >* HTTP响应报文格式及各种响应码
    >* HTTP请求报文格式
    >* Http1.1和Http1.0的区别
    >* Http怎么处理长连接
5. Cookie与Session的作用于原理
    >* A cookie is a bit of data stored by the browser and sent to the server with every request.
    >* A session is a collection of data stored on the server and associated with a given user (usually via a cookie containing an id code)
6. 电脑上访问一个网页，整个过程是怎么样的：DNS、HTTP、TCP、OSPF、IP、ARP
9. TCP与UDP区别及其各自优缺点
10. TCP和UDP数据报格式
11. TCP拥塞控制和流量控制
12. http与https区别
14. 滑动窗口与回退N针协议
15. 路由器与交换机区别
16. Ping的整个过程。ICMP报文是什么。
15. C/S模式下使用socket通信，几个关键函数。
16. IP地址分类

### 数据结构
1. 链表与数组。
2. 队列和栈，出栈与入栈。
3. 链表的删除、插入、反向
4. 字符串操作。
5. Hash表的hash函数，冲突解决方法有哪些。
6. 各种排序：冒泡、选择、插入、希尔、归并、快排、堆排、桶排、基数的原理、平均时间复杂度、最坏时间复杂 度、空间复杂度、是否稳定。
7. 快排的partition函数与归并的Merge函数。
8. 对冒泡与快排的改进。
9. 二分查找，与变种二分查找。
10. 二叉树、B+树、AVL树、红黑树、哈夫曼树。
11. 二叉树的前中后续遍历：递归与非递归写法，层序遍历算法。
12. 图的BFS与DFS算法，最小生成树prim算法与最短路径Dijkstra算法。
13. KMP算法。
14. 排列组合问题。
15. 动态规划、贪心算法、分治算法。（一般不会问到）
16. 大数据处理：类似10亿条数据找出最大的1000个数.........等等

### 操作系统
1. 说下Linux进程和线程的区别。进程调度优先级，和cpu调度进程关系。
2. IPC几种通信方式
3. 什么是虚拟内存
4. 死锁的必要条件，怎么处理死锁
5. 段存储，页存储，段页存储
6. 虚拟地址、逻辑地址、线性地址、物理地址的区别
8. 银行家算法

### 数据库
1. 关系数据库基本概念
2. 关系模式的规范化
3. 函数依赖与候选码的定义
4. 数据库中数据查询
5. 数据库查询优化
6. 数据的添加、删除、修改
7. 表的创建、修改表结构、删除表
8. Sqlite的基本操作
9. mysql的存储引擎有哪些，区别；

### 开发常见问题
1. multidex解决方法数过大的问题。
2. 5.0/6.0/7.0 新特性。
3. ANR产生的原因和解决步骤/ANR 具体产生的类型有哪些，具体说下其产生的最大超时时间。
4. 安卓为啥要加签名机制

### 零碎问题
1. activty和Fragmengt之间怎么通信，Fragmengt和Fragmengt怎么通信
2. 服务启动一般有几种，服务和activty之间怎么通信，服务和服务之间怎么通信
3. 布局优化主要哪些？具体优化？
4. 自定义view效率高于xml定义吗？说明理由。
5. 怎么让自己的进程不被第三方应用杀掉，系统杀掉之后怎么能启动起来。

### 附录
1. 部分问题参考答案
    >* [java部分知识点](http://www.jianshu.com/p/1990eb1f66eb)
    >* [华超校招笔记](http://huachao1001.github.io/)
    >* [android部分知识点](http://www.jianshu.com/p/89f19d67b348#)
