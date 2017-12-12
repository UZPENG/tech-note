# android 常用快捷键
## 定位类：
*	打开最近访问的文件（或最近修改的文件）
	Ctrl + E
*	跳到父类
	Ctrl + U
*	查找使用的地方
	Alt + F7
*	跳到上一次编辑的地方
	Ctrl+shift+方向键
*	在方法中切换
	Alt + 方向键
*	在文件中切换
	Ctrl + Tab
*	使用bookmarks
	F11、Ctrl + F11、Shift + F11
*	精确定位
	Ctrl + Shift + N
*	在外部打开文件
	Alt+鼠标左键
*	快速定位到布局文件
	Ctrl + Alt + Home
*	关闭窗口回到编辑器
	Esc shift + Esc
*	弹窗结构	Ctrl + F12			
*	Search everywhere  	Double Shift

## 信息类：
*	找到上下文信息
	Alt + Q
*	实现接口或超类方法
	Ctrl+I
* 	生成代码
	Alt+Insert
*	查看方法定义、类定义
	Ctrl + Alt +  P
*	查看参数信息
	Ctrl + Alt + I
*	查找所有操作
	Ctrl + Shift + A

## 编辑类：
*	代码补全 Alt + C
*	取反补全 !
*	后缀补全
	*	.for (补全for each语句)
	*	.format (使用String.format()包裹一个字符串)
	*	.cast (使用类型转化包裹一个表达式)
*	快速注释 快速取消注释  Ctrl + / Ctrl + Shift + /
*	多行选择 Alt + 鼠标左键
*	复制当前行 Ctrl + D
*	删除当前行 Ctrl + Y
*   合并行和文本 Ctrl + Shift + J
*	选择	Ctrl + W
*	提取方法 Ctrl + Alt + M
*   提取参数 Ctrl + Alt + P
*	行上下移动 Alt + Shift + Up/Down
*	移动方法 Ctrl + Shift + Up/Down
*	重命名 Shift + F6
*	包裹代码 Ctrl + Alt + T
*	取消包裹 Ctrl + Shift + Delete
*	提取变量 Ctrl + Alt + V
*   动态模板 Ctrl + J
*	多光标选择 Alt + J

其他类：
*	关掉所有窗口 Ctrl + Shift  + F12
* 	打开剪贴板 Ctrl + Shift + V

# Android Studio FAQ
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

6. 问题：升级android studio 3.0后，terminal中文乱码。  
解决办法：在home目录下修改'.bashrc'文件（没有就新建）添加'export LANG=en_US.UTF-8'
