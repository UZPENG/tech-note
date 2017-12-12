## android IO 大会上的笔记
### 构建
* gradle提速的十个技巧
>

* gradle3.0的特性
>* complie 和 implement的区别   
>* abi change 和 non-abi change

### RecylerView
* `ListView`：
>* 展示持久化内容的结构
>* 怎么样去快速地展示成千上万的items,创建view的代价高昂并且设备的内存有限。只将用户看到的
创建并且展示，当用户滚动再创建新的可见的view。

* best practices
>* `ViewHolder` 作为回收和复用的基本单位
>* 将`View`的创建和绑定分开
>* 使用标准框架的焦点和输入处理
>* 更容易维护
>* 更细粒度的数据变动监听
>* 让回收和动画更加高效
* `LayoutManager`:`LinearLayoutManager`、`GridLayoutManager`、`StaggeredGridLayoutManager`
> 定位`View`
> `recyclerview` 交互 然后 `layoutmanager` 负责滚动
> 在可见范围内的焦点处理时recyclerview处理的，如果要从可视范围以外获取视图，需要layoutmanager

* `Adaper`:create and populate item view on demand
>* 创建view和viewholder
>* 绑定item到viewholder
>* 通知recyclerview相关的变化
>* 处理item的交互
>* 多种view type
>* 恢复recycler
>* 细粒度的data变化事件监听

* 如果有Gaint and expensive的bitmap的话，只缓存视图结构，不缓存代价高昂的View。
