# 代码混淆
## 概念：
> * 将变量名改为无意义的符号。单个字母或者是下划线 __ 。
> * 重写逻辑使其更难理解，但是必须等价。
> * 打乱格式。
> * 构造特殊的指令使得反汇编器出错。
## 工具
> * ProGuard  免费开源的。Android Studio 支持的，可以被反编译，但是难以阅读。
> * DexGuard 收费的。部分不能反编译。
> * 备注：大部分人还是使用ProGuard的。第一，因为它是免费的；第二，很多第三方的库没有DexGuard的配置文档，而ProGuard的文档
比较齐全。

详情连接：<https://shadowzwy.github.io/2016/12/04/Android%E6%B7%B7%E6%B7%86%E5%B7%A5%E5%85%B7-Proguard%E5%AE%9E%E8%B7%B5.html>
