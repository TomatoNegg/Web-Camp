### 3月23日早上
##### 这天上午在CSDN上看到一大堆干货，其中对于编程的优化处理最为有用
1. 尽量指定类，方法的final的修饰符
2. 尽量重用对象
3. 尽可能使用局部变量
4. 尽量减少对变量重复计算
5. 尽量采用懒加载
6. 慎用异常
7. 不要在循环使用try...catch ，应放到外层
8. 乘法除法尽量使用移位操作
9. 循环内不要不断创建对象引用
10. 不要将数组声明为public static final
11. 尽量避免随意使用静态变量
12. 将变量声明为static final,并以大写命名
13. 不要让public方法有太多形参
14. 不要对数组使用toString（）方法
##### 等等共记录下了35种优化处理方法，这些都是能使代码运行更流畅，同时也能让系统性能提高的方法

---
##### 对于Java的学习，在疯狂讲义里看到了
System类，Runtime类，Object类，String类，StringBuff类，Stringbuilder类，Math类，对于每个类的哪些常用类都保存在Xmind里，在Xmind中对这些常用类进行分类
##### 然后昨天还对前面的知识进行了一次回顾
更深入了解了this关键字，对于方法，构造器，接口，抽象类，继承，异常处理，成员变量，局部变量，对象，内部类有了新的理解
##### 同时也还在网上看了Git&GitHub教程
 对于Git有许多命令，如
-  
> $cd F

> $cd Web-camp

> $mkdir learnt

> $cd testgit
- 
git init(初始化仓库)

git add ****(提交文件到缓存区)

git commit -m******(将stage文件送到本地仓库里去）

git status （可以随时掌握当前状态）

git diff（可以查看difference）

git log（显示从最近到最远的日志）

git reset --hard HEAD^(倒退)

cat 文件名（查看内容）

git reflog(记录每一次命令)

git checkout --文件名（把修改全部撤销）

    