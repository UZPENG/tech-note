# 代码模板使用
下面选中的三块分别为：
> * 文件和代码模板
> * 动态模板
> * 意图（自动补全对应代码）

![动态模板的位置](http://oepm6q4qh.bkt.clouddn.com/templatelocation.png)

## AndroidSutio文件模板介绍
如下图所示，总共有四个部分组成。
1.  Files-新建文件时采用的模板
2. Include-文件模板中可以引入的模板
3.  Code-某些情况下会触发的代码模板
4.  Other-其他文件的模板

![动态模板的位置](http://oepm6q4qh.bkt.clouddn.com/filetemplate.png)

#### Files模板
这是新建文件时采用的模板。当我们尝试新建一个文件时，IDE会让我们选择一个文件模板。如下图所示：

![动态模板的位置](http://oepm6q4qh.bkt.clouddn.com/3.png)
可以看到，这里面的模板全部都是我们在 设置->Editor->File and Code Template->Files模板里面定义好的。

模板的使用就是这么简单，下面来看看模板的定义。
先简单介绍一下文件模板的组成：
	**1. 静态代码 **
	**2. 动态变量（系统预定义的和自定义的）**

![动态模板的位置](http://oepm6q4qh.bkt.clouddn.com/7.png)

观察上图，${NAME}、${PACKAGE_NAME}、${INTERFACE}都是属于**动态变量**，其中${NAME}、${PACKAGE_NAME}是系统预定义的变量，所有系统**预定义变量**如下图。**自定义变量**会在创建文件的时候输入。其余部分属于**静态代码**，可以观察到头部还有有两个宏定义。第一个是条件语句，第二个是引入一个模板。是否有其他的宏定义我就没有去了解了，大家有了解的话可以分享一下。另外关于引入模板是什么正是下面要讨论的内容。

![动态模板的位置](http://oepm6q4qh.bkt.clouddn.com/8.png)
#### Include模板
其实这个也很简单，就是我们可以预先定义好一些模板，然后在写其他模板的时候可以引用。用得比较多的就是文件的头部了，因为我们一般都会在文件的头部定义作者和版本信息，为了不用每个文件都重复写一遍，我们就可以把这部分单独作为一个模板方便其他模板引用。

![动态模板的位置](http://oepm6q4qh.bkt.clouddn.com/9.png)
IDE默认就定义了上面两个模板，如果有需要的话，可以自己另外定义一些模板。比如我就根据需要修改了一下File Header模板。

#### Code模板
这个模板是在特定情况下触发的一个模板，不支持添加，但是可以修改。目前的话娿，我没发现有什么修改的。如果有发现的小伙伴可以share一下。
#### Other
这一部分的模板是新建其他文件使用的模板，同样不支持添加，但可以修改。具体文件如下图：
![动态模板的位置](http://oepm6q4qh.bkt.clouddn.com/10.png)

## AndroidStudio动态模板介绍
Living Template的使用就更加简单了，直接输入对应的缩写就能够补全对应的代码。详细的映射关系可以在 **设置->Editor->Living Templates**查看。Living Template支持修改和添加，可以根据自己的需要进行添加和修改。自定义和方法和文件模板的差不多，就不在赘述了。

![动态模板的位置](http://oepm6q4qh.bkt.clouddn.com/11.png)

## Intentions
Intentions也是在特定情况下触发的代码补全机制，具体情况参考设置。**Intentions不支持自定义和修改**，但可以学习使用一下。

##附自定义的文件模板：
#### view 接口:

```java
#if (${PACKAGE_NAME} && ${PACKAGE_NAME} != "")package ${PACKAGE_NAME};#end
#parse("File Header.java")
public interface ${NAME} {
   /**
   * 事件回调
   */
  interface ActionCallback {
  }

  /**
   * 设置事件回调
   * 
   * @param callback 事件回调
   */
  void setActionCallback(ActionCallback callback);
  
  /**
   * 绑定资源
   * 
   * @param rootActivity 根活动
   */
  void bindRes(FragmentActivity rootActivity);

  /**
   * 绑定资源
   * 
   * @param rootView 根视图
   */
  void bindRes(View rootView);

  /**
   * 初始化
   */
  void init();

}
```

#### view实现
```java
#if (${PACKAGE_NAME} && ${PACKAGE_NAME} != "")package ${PACKAGE_NAME};#end
#parse("File Header.java")
public class ${NAME} implements ${INTERFACE}{
  private FragmentActivity rootActivity;
  private ActionCallback actionCallback;

  @Override
  public void bindRes(FragmentActivity rootActivity) {
    this.rootActivity = rootActivity;
  }
  
  @Override
  public void init() {
    if (rootActivity == null) {
      DebugTool.postDebugError("invalid rootActivity null");
    }
  }
}

```

#### Presenter接口
```java
#if (${PACKAGE_NAME} && ${PACKAGE_NAME} != "")package ${PACKAGE_NAME};#end
#parse("File Header.java")
public interface ${NAME} {

  /**
   * 绑定视图
   * 
   * @param view 视图
   */
  void setView(${IView} view);

  /**
   * 绑定资讯详情模型
   * 
   * @param model 资讯详情模型
   */
  void setModel(${IModel} model);

  /**
   * 初始化
   */
  void init();

  /**
   * 销毁
   */
  void destroy();

    
}

```

#### Presenter实现
```java
#if (${PACKAGE_NAME} && ${PACKAGE_NAME} != "")package ${PACKAGE_NAME};#end
#parse("File Header.java")
public class ${NAME} implements ${IPresenter},
    ${IView}.ActionCallback,
    ${IModel}.DataCallback,{
    
  private ${IView}  view;
  private ${IModel} model;

  @Override
  public void setView(${IView}. view) {
    this.view = view;
  }

  @Override
  public void setModel(${IModel} model){
    this.model = model;
  }

  @Override
  public void init() {
    if (view != null) {
      view.setActionCallback(this);
      view.init();
    }

    if (model != null) {
      model.setOnDataCallback(this);
    }
  }

  @Override
  public void destroy() {
    if (view != null) {
      view.setActionCallback(null);
    }

    if (model != null) {
      model.setOnDataCallback(null);
    }
  }
}

```

#### Model接口
```java
#if (${PACKAGE_NAME} && ${PACKAGE_NAME} != "")package ${PACKAGE_NAME};#end
#parse("File Header.java")
public interface ${NAME} {
 /**
   * 数据回调接口
   */
  interface DataCallback {
  
  }
  
    /**
   * 设置数据回调接口
   * 
   * @param callback
   */
  void setOnDataCallback(DataCallback callback);

}

```

#### Model实现
```java
#if (${PACKAGE_NAME} && ${PACKAGE_NAME} != "")package ${PACKAGE_NAME};#end
#parse("File Header.java")
public class ${NAME} implements ${IModel}{
  private final Context context;
  private final HttpEngine httpEngine;

  private final ${IModel} model;

  private ${IModel}.DataCallback dataCallback;
  
    /**
   * 
   * @param context 上下文
   */
  public NewsDetailModelImpl(Context context) {
    this.context = context;
    httpEngine   = new HttpEngine();
    model = new ${IModel}(context);
  }

  @Override
  public void setOnDataCallback(${IModel}.DataCallback callback) {
    this.dataCallback = callback;
  }
}
}
```

#### Fragment
```java
#if (${PACKAGE_NAME} && ${PACKAGE_NAME} != "")package ${PACKAGE_NAME};#end
#parse("File Header.java")
public class ${NAME} {
  @Override
  public View onCreateView(LayoutInflater inflater, ViewGroup container, Bundle savedInstanceState) {
    return inflater.inflate(R.layout.frg_ticker_kline, container, false);
  }

  @Override
  public void onActivityCreated(Bundle savedInstanceState) {
    super.onActivityCreated(savedInstanceState);
  }

  @Override
  public void onDestroy() {
    super.onDestroy();
  }
}
```