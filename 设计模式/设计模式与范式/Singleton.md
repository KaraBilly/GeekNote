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
