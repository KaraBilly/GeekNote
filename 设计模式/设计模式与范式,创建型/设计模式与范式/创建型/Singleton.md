# 单例模式

Question：
1.为什么要使用单例模式 .Why?
2.单例模式存在哪些问题 .
3.单例与静态类的区别.
4.有何替代方案.

1.why
>解决处理资源冲突，如何实现对类加锁--单例
>表示全局唯一性 ,有些数据在系统中只应该保存一份.
AtmoicLong  Java 并发库提供的原子变量类型   --.net
2.how to implement
main focus point
>private ctor.
>thread safe when created
>support lazy load or not
>getInstance() performance (lock in the func or not)
试着用自己熟悉的语言去实现下单例模式（go/c#）
3.单例存在的问题
> 单例对OOP特性支持不友好
> 单例会隐藏类之间的依赖关系
 通常通过构造函数 参数传递等方式声明类之间的依赖关系
> 单例对代码的拓展性不友好
> 单例对代码的可测试性不友好
> 单例不支持有参数的构造函数
    1.提供Init方法  2.参数放在getinstance方法中  3.参数放在全局变量中，可以通过配置文件读取重写
有何替代解决方案？
    工厂模式 IOC等等

如何解决误导用户的问题
Singleton singleton1 = Singleton.getInstance(10, 50);
Singleton singleton2 = Singleton.getInstance(20, 30);
----------------------------------------------------------
如何设计实现一个集群环境下的分布式单例模式
通过外部共享存储区 ---获得后加锁 释放后解锁 [分布式锁]
如何实现线程唯一的单例？ 
----Dictionary
如何实现多例模式？
Map来存储对象类型和对象间的对应关系，控制对象个数