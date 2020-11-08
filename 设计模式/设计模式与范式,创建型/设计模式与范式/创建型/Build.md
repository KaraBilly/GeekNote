# 建造者模式   Builder模式

* Q: 直接使用构造函数或者配合set方法就能创建对象,为什么要使用Builder模式来创建
A: 构造函数忠参数列表因可配置项的增多而变得很长，代码在可读性和易用性上都会变差。
考虑使用建造者模式的一些情况：1.可以有效地避免构造函数参数过长
2.如果由依赖关系，但是参数又是可空的 配置项之间有依赖关系，可以让校验逻辑有地安放
3.如果希望对象是不可变对象，在创建好之后，就不能再修改内部的属性值，set()不必暴露
* 与工厂模式的区别
1.工厂模式用来创建不同但是相关类型的对象（继承同一父类或者接口的一组子类），由给定的参数来决定创建哪种类型的对象。
创建这模式 用来创建一种类型的复杂对象，根据设置不同的可选参数，定制化地创建不同的对象。

isRef =true arg表示String类型的refBeanId，type不需要设置
isRef =false arg，type 都要设置

 public class ConstructorArg {
    private boolean isRef;
    private Class type;
    private Object arg;
    // TODO: 待完善...
  }