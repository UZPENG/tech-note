## Java IO

### 字节流
`InputStream`接口：

| 方法     |功能|
| :------------------- | :------------- |
| `int read()`         | 读取下一个byte并返回，到达末尾时返回-1。没有数据可用时，会阻塞。|
| `int read(byte[] b)` | 读取数据到byte数组b。如果b长度为0，返回0；到底末尾，返回-1；否则返回成功读取了多少字节。没有数据可用时，会阻塞。|
|`int read(byte[] b,int off,int len)`| 将b数组偏移off再读len个字节，返回结果和上面的方法类似|
|``int available()``      |   返回可以读的byte的数量     |
|`void close()`|  关闭流，释放资源|
|`void skip(long n)`| 跳过n个字符|
|`void mark(int limit)`|  最多能读limit个字节|
|`void reset`| 解除mark的限制|

`OutputStream接口`：

| 方法 | 功能     |
| :------------- | :------------- |
| ``void write(int)``  | 写入一个字节（强制类型转换）|
| `void write(byte[])` | 写入一个字节数组|
| `void write(byte[],int,int)`| 偏移后写入指定长度|
| `void flush()`       | 清空缓冲区|
| `void close()`       | 关闭流释放资源|

字节流的实现类主要有以下：

| 类名 | 构造方法 |
| :------------- | :------------- |
| `FileInputStream` | `new FileInputStream(new File("path"))` |

### 字符流
例子：打开文本文件，设置文本文件编码，读取内容，添加内容等。  
使用：`InputStreamReader(InputStream,charset)`和`OutputStreamWriter(OutputStream,charset)`提供`read()`和`write()`访问进行读写。
```Java
  OutputStreamWriter writer = new OutputStreamWriter(new FileOutputStream(
    new File("path"), true),
    "utf-8");
  writer.writer("String");
  writer.newLine();
```
