## 构造器
1. 子类不能继承父类的构造器（构造方法或构造函数），但是如果父类的构造器是有参数的，则必须在子类的构造器中显式地通过super关键字调用父类的构造器并配以适当的参数列表。
2. 如果父类有个没有参数的构造器，则在子类的构造器中用super调用父类构造器不是必须的，如果没有使用super关键字，系统会自动调用父类的无参构造器。
>
```Java
class SuperClass {
    private int n;
    SuperClass(){
        System.out.println("父类没有参数构造器")；
    }
    SuperClass(int n){
        System.out.println("父类有参数构造器，参数为n")；
        this.n = n;     //指向自己的引用，就是private int n这个n
    }
}
    Class SubClass extends SuperClass{
        private int n;
        
        SubClass(){
            super(300);     //super用来引用当前父类构造器
            System.out.println("子类无参数构造器")；
            
        }
        
        public SubClass (int n){
            System.out.println("子类有参数构造器:"+n);
            this.n = n;     //this指向SubClass的n
        }
    }
    public class TestSuperSub{
        public static void main (String [] args){
            SubClass sc = new SubClass();
            SubClass sc2 = new SubClass(200);
        }
    }
```

## 静态内部类

- 静态内部类实例方法不能访问外部类的实例成员
- 静态内部类是外部类一个静态成员，外部类所有方法，所有初始化块中可使用静态内部类来定义变量，创建对象等。

```Java
public class a
{
    private int c = 5;
    private int b = 6;
    public void abc(){
        ABC g = new ABC();
    }
    static class ABC{
        System.out.println("hahahah");
    }
}

```
- 在外部类内部使用内部类时，不要用静态访问非静态内部类
- 在外部类外部使用内部类时，访问修饰符不能使private,而类名则应该是       外部类名.内部类  变量名
- 创建内部类对象时    外部类实例.new 内部对象

```
Class out{
    class in
    {
        public in(String msg)
        {
            System.out.println(msg);
        }
    }
}
public class a
{
    public static void main(String[] args)
    {
        out.in b = new out().new in("测试信息区")；/*创建了一个内部对象
        左边是外部类.内部类  引用变量名
        右边是先new出一个外部实例然后再.new出个内部类实例这样
    }
}
```
