# 设计模式
**设计模式（Design Pattern）**是一套呗反复使用的、多数人知晓的、经过分类编目的、代码设计经验的总结，使用设计模式是为了可重用代码、让代码更容易被他人理解并且保证代码可靠性。
## 一、概况
设计模式分为三大类：

1. 创建型模式（描述如何创建对象），共五种：工厂方法模式、抽象工厂模式、单例模式、建造者模式、原型模式。

2. 结构型模式（描述如何实现类或对象的组合），共七种：适配器模式、装饰器模式、代理模式、外观模式、桥接模式、组合模式、享元模式。

3. 行为型模式（描述类或对象怎样交互以及怎样分配职责），共十一种：策略模式、模板方法模式、观察者模式、迭代子模式、责任链模式、命令模式、备忘录模式、状态模式、访问者模式、中介者模式、解释器模式。

## 二、设计模式的七大原则
1、**单一职责原则(Single Responsibility Principle,SRP)**

一个类只负责一个功能领域中的相应职责。

2、**开闭原则（Open Close Principle）**

开闭原则就是说对扩展开放，对修改关闭。在程序需要进行拓展的时候，不能去修改原有的代码，实现一个热插拔的效果。

3、**里氏代换原则（Liskov Substitution Principle）**

所有引用基类对象的地方能够透明地使用其子类的对象。
实际上可以这样理解：（1）子类的能力必须大于等于父类，即父类可以使用的方法，子类都可以使用。（2）返回值也是同样的道理。假设一个父类方法返回一个List，子类返回一个ArrayList，这当然可以。如果父类方法返回一个ArrayList，子类返回一个List，就说不通了。这里子类返回值的能力是比父类小的。（3）还有抛出异常的情况。任何子类方法可以声明抛出父类方法声明异常的子类。
而不能声明抛出父类没有声明的异常。

4、**依赖倒转原则（Dependence Inversion Principle）**

这个是开闭原则的基础，抽象不应该依赖于细节，细节应该依赖于抽象。换言之，要针对接口编程，而不是针对实现编程。

5、**接口隔离原则（Interface Segregation Principle）**

这个原则的意思是：使用多个隔离的接口，比使用单个接口要好。还是一个降低类之间的耦合度的意思，从这儿我们看出，其实设计模式就是一个软件的设计思想，从大型软件架构出发，为了升级和维护方便。所以上文中多次出现：降低依赖，降低耦合。

6、**迪米特法则（最少知道原则）（Demeter Principle）**

为什么叫最少知道原则，就是说：一个实体应当尽量少的与其他实体之间发生相互作用，使得系统功能模块相对独立。

7、**合成复用原则（Composite Reuse Principle）**

原则是尽量使用合成/聚合的方式，而不是继承来达到复用的目的。

## 三、创建型模式
1、**抽象工厂模式(Abstract factory pattern)**: 提供一个接口, 用于创建相关或依赖对象的家族, 而不需要指定具体类.

2、**生成器模式(Builder pattern)**: 使用生成器模式封装一个产品的构造过程, 并允许按步骤构造. 将一个复杂对象的构建与它的表示分离, 
使得同样的构建过程可以创建不同的表示.

3、**工厂模式(factory method pattern)**: 定义了一个创建对象的接口, 但由子类决定要实例化的类是哪一个. 工厂方法让类把实例化推迟到子类.

4、**原型模式(prototype pattern)**: 当创建给定类的实例过程很昂贵或很复杂时, 就使用原形模式.

5、**单例模式(Singleton pattern)**: 确保一个类只有一个实例, 并提供全局访问点.

6、**多例模式(Multition pattern)**: 在一个解决方案中结合两个或多个模式, 以解决一般或重复发生的问题.

## 四、结构型模式

1、**适配器模式(Adapter pattern)**: 将一个类的接口, 转换成客户期望的另一个接口. 适配器让原本接口不兼容的类可以合作无间. 对象适配器使用组合, 类适配器使用多重继承.

2、**桥接模式(Bridge pattern)**: 使用桥接模式通过将实现和抽象放在两个不同的类层次中而使它们可以独立改变.

3、**组合模式(composite pattern)**: 允许你将对象组合成树形结构来表现"整体/部分"层次结构. 组合能让客户以一致的方式处理个别对象以及对象组合.

4、**装饰者模式(decorator pattern)**: 动态地将责任附加到对象上, 若要扩展功能, 装饰者提供了比继承更有弹性的替代方案.

5、**外观模式(facade pattern)**: 提供了一个统一的接口, 用来访问子系统中的一群接口. 外观定义了一个高层接口, 让子系统更容易使用.

6、**亨元模式(Flyweight Pattern)**: 如想让某个类的一个实例能用来提供许多"虚拟实例", 就使用蝇量模式.

7、**代理模式(Proxy pattern)**: 为另一个对象提供一个替身或占位符以控制对这个对象的访问.

## 五、行为型模式
1、**责任链模式(Chain of responsibility pattern)**: 通过责任链模式, 你可以为某个请求创建一个对象链. 每个对象依序检查此请求并对其进行处理或者将它传给链中的下一个对象.

2、**命令模式(Command pattern)**: 将"请求"封闭成对象, 以便使用不同的请求,队列或者日志来参数化其他对象. 命令模式也支持可撤销的操作.

3**、解释器模式(Interpreter pattern)**: 使用解释器模式为语言创建解释器.

4、**迭代器模式(iterator pattern)**: 提供一种方法顺序访问一个聚合对象中的各个元素, 而又不暴露其内部的表示.

5、**中介者模式(Mediator pattern)** : 使用中介者模式来集中相关对象之间复杂的沟通和控制方式.

6、**备忘录模式(Memento pattern)**: 当你需要让对象返回之前的状态时(例如, 你的用户请求"撤销"), 你使用备忘录模式.

7、**观察者模式(observer pattern)**: 在对象之间定义一对多的依赖, 这样一来, 当一个对象改变状态, 依赖它的对象都会收到通知, 并自动更新.

8、**状态模式(State pattern)**: 允许对象在内部状态改变时改变它的行为, 对象看起来好象改了它的类.

9、**策略模式(strategy pattern)**: 定义了算法族, 分别封闭起来, 让它们之间可以互相替换, 此模式让算法的变化独立于使用算法的客户.

10、**模板方法模式(Template pattern)**: 在一个方法中定义一个算法的骨架, 而将一些步骤延迟到子类中. 模板方法使得子类可以在不改变算法结构的情况下, 重新定义算法中的某些步骤.

11、**访问者模式(visitor pattern)**: 当你想要为一个对象的组合增加新的能力, 且封装并不重要时, 就使用访问者模式.

## 六、常用的设计模式（详细）


