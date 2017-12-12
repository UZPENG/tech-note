# java基础笔记
### 面向对象三大特征
封装、继承、多态
### java的修饰符总结
* private、public、protected
* static、final
* default、volatile、native、transient

### java数据类型
基本数据类型
* byte、short、int、long、float、double、char、boolean

类型转换
* byte>short>int>long 由低到高带符号自动扩展，由高到低自动截断。
* float、double->byte、short、int、long 取整再按整型处理

引用类型：数组
* 初始化、访问、方法

### 运算符
算术运算符
* 加、减、乘、除、取模
* 算术运算将byte、short、char自动提升为int型
* 如果有long、float、double则转换为对应的类型，从左往右优先级升高

逻辑运算符
* 大于、小于、等于、小于等于、大于等于、不等、与或非、异或

位运算符
* 左移、右移、逻辑右移

三目运算符

### 流程控制
条件
* if-else、switch、嵌套if-else

循环
* while、do-while、for、for-each

循环控制
* break、continue、return


### 类
定义类
* final 不可继承、abstract 抽象类

成员变量
* Field、构造器、方法、初始化块、内部类
* private 类内部访问、无修饰 包内部可访问、protect 子类和包内部可访问、public 所有都可以访问
* static 类变量、final 不可修改、volatile 内存可见、transient 暂时的（序列化时忽略）

this和super
* this 是当前对象的指针
* super 访问父类中的方法和属性

import和import static
* import 省略包名
* import static 省略类名访问

初始化块
* 调用顺序：静态初始化块>初始化块>父类构造器>子类构造器

重载和重写
* 重载是参数列表不一样
* 重写是参数列表完全一样

### 接口
接口的变量
* 默认private static final修饰

接口支持多继承
