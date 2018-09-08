## android零碎笔记
### 项目构建与资源使用
* android v26 支持res文件里面定义font文件夹 自定义font文件
![](/img/android-note.png)


### 常见API使用
* `` LayoutInflate.from(Context context).inflate.(@ResInt int layout, ViewGroup viewGroup)``
如果不传入``ViewGroup``参数，将会失去与Parent相关的属性，比如``MatchParent``。


### 系统自带View使用
#### RecylerView
* **五大重要组件**`LayoutManager`、`item Animation`、`Adaper`、`ViewHolder`、`Decoration`
* ``RecyclerView``最简单的实现方式：重写``RecyclerView.Adaper``和`RecyclerView.ViewHolder`
并添加`LinearLayoutManager`。
* ``RecylerView``使用``addItemDecoration()``添加``DividerItemDecoration``作为分割线。``DividerItemDecoration``可以``setDrawable``为分割线添加样式。
* `onBindViewHolder`方法在滑动列表时会反复调用。
* `onViewRecycled()`会在view被回收的时候回调。 **//todo 什么时候被回收？怎么回收？怎么缓冲?**
* `notifyDataChange()`有一系列方法可以通知数据的变更（插入，修改，删除，范围修改等等）。通过`Observerable`和`Observer`实现。**//todo 怎么实现？如果查找修改的数据，如果插入，复杂度**

#### CardView
* ``CardView``使用``setCardViewElevation()``并且``setUseCompatPadding(true)``设置阴影。

#### TextView
* 自定义字体使用``Typeface.create(AssertManger manager,String filename)``获取，该方法为耗时操作，不应该在主线程反复调用。``TextView``使用`setTypeFace(Typeface typeface)`设置字体。

#### toolbar和ActionBarLayout
* `setNavigationIcon()`或者`app:navigationIcon=""`设置Toolbar左边的图标，
使用`setNavigationOnClickListener()`这是点击事件监听
* 使用`setSupportActionBar()`将`Toolbar`设置为`ActionBar`
* 重写`onCreateOptionMenu()`并调用`getMenuInflate.inflate()`绘制菜单
* 重写`onOptionItemSelected(MenuItem item)`监听actionBar上面的view的信息。`androd.R.id.home`是左边的按钮
* `ActionBarLayout`可以和`coordinateLayout`配合实现`toolbar`的嵌套滚动


#### coordinateLayout
* 子view根据`app:layout_behavior`属性来协调滚动，默认有`@string/appbar_srolling_view_behavior`
* 还有使用`app:srcoll_flag`来控制滚动的行为

#### snackbar
* `SnackBar.make(View )`

#### floatingActionBar

### android更新
#### android8.0
* Android Phone支持画中画
* 垃圾回收可以在前台进行，更高效地分配和回收堆内存
* 支持自定义字体和下载字体
* 支持更多emoji表情（通过下载最新字体）
* spring Animation等新的动画API
* TextView支持自适应的大小

#### kotlin的支持
* kotlin编译成java字节码，运行在JVM上面
* kotlin异步编程很简单
* kotlin支持协程,kotlin也可以编译在JS上面跑
