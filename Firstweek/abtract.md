# 3月21日

---
这天看了很多java，其中包括java的抽象类，接口，内部类

1. 抽象类

    抽象类必须使用abstract定义，抽象类可以没有抽象方法
    
    同时抽象类不能被实例化，就是说抽象类无法创建实例
    抽象类可以包含成员变量，方法（普通方法和抽象方法）
    
    总之，抽象有得有失
    
    得 多了个抽象方法
    
    失 不能用于创建实例
    
    抽象类不能用于创建实例，只能当作父类被其他子类继承。
    
    用abstract修饰的类只能被继承，而用final修饰的类不能被继承，所以abstract和final不能共存
    
    使用static修饰方法，可通过类名调用该方法，但如果有abstract修饰，那么将导致用类名调用了个没有方法体的方法，因此static和abstract不能同时修饰方法
    
    同理，private和abstract不能同时修饰方法。
    
1. 抽象类作用就是提供一个模板，提供了子类通用的方法，并让子类去实现这些方法
2. 使用模板模式的规则：
    
    抽象父类可以只定义需要使用的某些方法，把不能实现的
    父类中可能包含需要调用其他系列方法的方法。父类里提供的方法只是定义了一个通用算法，其实现必须依赖子类的辅助
    
    
```Java
public class CarSpeedMeter extends SpeedMeter
{
    public double getRadius()
    {
        return 0.28;
    }
    public static void main(String [] args)
    {
        CarSpeedMeter csm = new CarSpeedMeter();
        csm.setTurnRate(15);
        System.out.println(csm.getSpeed());
    }
}

```






