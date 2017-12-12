## Android Studio指南
1. 问题：gradle 版本不兼容导致的各种问题
解决办法：在Project的build.gradle文件下配置gradle为最新版本
![](http://oepm6q4qh.bkt.clouddn.com/gradle.png)
备注：注意区分gradle的版本和Android Gradle Plguin 版本。

2. 问题：invalid LOC header
解决办法：删除项目目录下的gradle或者build文件夹，重新编译项目。

3.  问题：编辑器字体有明显锯齿。
解决办法：打开如下图的设置，设置抗锯齿。
![](http://oepm6q4qh.bkt.clouddn.com/12.png)

4.  问题：没有Logcat信息。
解决办法：如下图所示刷新logcat。如果是华为手机，在拨号处输入
\*#\*#2846579#\*#\*,开启日志。
详情见文章<http://devlu.me/2016/07/29/open-android-debug-log-in-device/>

5. 问题：Android Studio的配置问题。
解决办法：下载自己已保存的配置文件直接导入。
以下是我的配置文件。
<http://oepm6q4qh.bkt.clouddn.com/settings.jar>
