
### 1. 为什么说Java是一门平台无关语言？
平台无关实际的含义是“一次编写到处运行”。Java 能够做到是因为它的字节码（byte code）可以运行在任何操作系统上，与底层系统无关。

### 2. 为什么 Java 不是100%面向对象？
Java 不是100%面向对象，因为它包含8个原始数据类型，例如 boolean、byte、char、int、float、double、long、short。它们不是对象。

### 3. 什么是 singleton class，如何创建一个 singleton class？
Singleton class 在任何时间同一个 JVM 中只有一个实例。可以把构造函数加 private 修饰符创建 singleton。

### 4. 什么是多态？什么是运行时多态，也称动态方法分配？
多态简单地说“一个接口，多种实现”。多态的出现使得在不同的场合同一个接口能够提供不同功能，具体地说可以让变量、函数或者对象能够提供多种功能。下面是多态的两种类型：

- 编译时多态。
- 运行时多态。
- 编译时多态主要是对方法进行重载（overload），而运行时多态主要通过使用继承或者实现接口。

在 Java 中，运行时多态或动态方法分配是一种在运行过程中的方法重载。在这个过程中，通过调用父类的变量引用被重载的方法。下面是一个例子：

```java
class Car {
    void run()
    {
        System.out.println(“car is running”); 
    }
}

class Audi extends Car {
    void run()
    {
        System.out.prinltn(“Audi is running safely with 100km”);
    }
    public static void main(String args[])
    {
        Car b= new Audi();    //向上转型
        b.run();
    }
}
```