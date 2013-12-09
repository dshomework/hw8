# How to debug?
> 在自己没有调试前请不要问别人程序出了什么问题。        ———— 崔永元  
> 写代码的人居然不会调试，那是一种耻辱。                ———— 白岩松

### 单步调试

#### 调试器
+ VisualStudio on Windows
+ GDB on Linux, Mac, Windows

#### IDE with debugger
+ VisualStudio
+ CodeBlocks
+ Eclipse / MyEclipse
+ XCode on Mac

#### 方法
+ Step into
+ Step Over
+ Breakpoint
+ Continue
+ Watch Variables & Expressions

### Log输出
> 尤其适用于许多无法单步调试的场景，比如程序过于复杂，分布式，其他动态语言等。

#### Log添加技巧
+ 加入前缀方便识别。如 function_name, variable_name 等。
+ 为对象添加序列化方法方便输出。
+ 区分log类型：info，debug，error等。
+ 一般添加在关键地方：函数开始与结束，某些复杂操作的开始与结束，IO操作的前后等。
+ 同时添加在可能出问题的地方，有助于缩小debug范围，迅速定位问题所在。

### 断言
> 适用于一些边界条件保证。

#### 常用于
+ 断言指针非NULL
+ 断言数字变量非零或非负

### 边界测试
#### 常见边界条件
+ 指针为NULL
+ 除零错误
+ 0
+ 空字符串
+ 数据的极限值（压力测试）

## 常见错误可能原因
### TLE
+ 算法选择错误，时间复杂度估计等
+ 死循环
+ 没有做正常的优化或剪枝
+ 同样的操作，有更快的选择？

### MLE
+ 数组开太大
+ 指针动态对象new太多
+ 忘记及时delete／free进行内存释放

### RE
+ 栈溢出，递归层数过多
+ 段错误

### Segment Fault 段错误
> SegFault 基本都和内存有关

+ 栈溢出
+ 数组范围溢出
+ 使用了未初始化的变量或指针
+ 直接使用了NULL指针

### WA
+ RP不好

### AC
+ RP不错

