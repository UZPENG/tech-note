# Android 进程
## 进程的优先级
![进程优先级](http://www.mrpeak.cn/images/at1.jpg)
## Android线程调度
![](http://www.mrpeak.cn/images/at2.jpg)
<br>
time slice分配图
## 知识点
> * handler与Looper绑定、Looper和线程绑定
> * looper的构造函数
<pre><code> private Looper(boolean quitAllowed) {
        mQueue = new MessageQueue(quitAllowed);
        mThread = Thread.currentThread();
    }
</pre></code>
## API使用
> * runOnUIThread() 