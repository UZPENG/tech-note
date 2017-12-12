- [Ubuntu笔记记录](#ubuntu笔记记录)
	- [mysql的配置](#mysql的配置)
	- [命令的使用](#命令的使用)
		- [系统信息](#系统信息)
		- [文件系统](#文件系统)
		- [shell使用](#shell使用)
		- [用户管理](#用户管理)
		- [](#)

<!-- /TOC -->
# Ubuntu笔记记录
## mysql的配置
sudo apt install mysql-server // 安装mysql服务器

配置文件目录:
/etc/mysql/mysql.conf.d/mysqld.conf

更改配置文件的**bind_address**修改为自己想要监听的网段，0.0.0.0为所有网段。

申请用户，赋予用户权限。

问题列表：
* 启动不了，提示exit code -1。
答：备份配置文件，连配置一起卸载掉mysql，然后重装。

## 命令的使用
### 系统信息
* free：查看内存使用情况
* df：查看系统分区
* top：任务管理器<!-- TOC depthFrom:1 depthTo:6 withLinks:1 updateOnSave:1 orderedList:0 -->
* cal：查看日历
* date：查看时间

### 文件系统
* touch：新建空白文件
* vim: 编辑文件
* mv：移动或重命名
* cp：复制文件、复制文件夹
* rm：删除文件或文件夹
* ls：查看目录
* ln：创建连接（软连接or硬链接）
* less：查看文本文件内容
* file：查看文件类型
* cd：改变工作目录
* pwd：显示当前工作目录
* cat：连接文件内容
* tee：获取输入并截取接着输出
* chown:改变文件所有者
* chgrp：改变文件所属组
* chmod：改变文件权限
* ~：当前用户的主目录 .：当前目录 ..：父级目录 -：上次输入pwd的目录
* >:重定向输入 <:重定向输入 >>:追加输出 <<:追加输入
* |：管道

### shell使用

### 用户管理
* passwd：修改用户密码
* su：切换到root用户
* adduser：添加用户

###
