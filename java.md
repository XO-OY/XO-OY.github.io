### 1.JTextField自定义大小
    jtf.setPreferredSize(new Dimension(400, 100));
    
### 2.md5加密
    DigestUtils.md5Hex(str);
    
### 3.判字符串是否全为数字
    str.matches("[0-9]+");//boolean### 
    
### 4.java中全都是值传递

### 5.程序设计原则 
1. 单一责职原则
2. 里氏替换原则
3. 依赖倒置原则
4. 接口隔离原则
5. 最少知道原则
6. 开放封闭原则

### 6.java合法标示符
    由数字、字母、下划线、$构成(数字不能开头)
    或者Unicode字符("猫")
    
### 7.静态代码块属于类 非静态代码块属于对象(有对象才执行)

### 8.final修饰的成员域要初始化

### 9.获取str单精度浮点
    Float.parseFloat(str) //返回float类型值  
    Float.valueOf(str) //返回Float对象
    
### 10.System.gc()==Runtime.getRuntime().gc();

### 11.单元测试为==程序员开发时==使用

### 12.线程
    resume() <-> suspend() //已弃
    wait() <-> notify()/notifyAll() 
    //wait()会释放资源 notify()随机唤醒，唤醒线程进入锁池，等待获得锁
    stop()//终止线程 已弃
    yield()//线程退让给>=其优先级的
    join()//线程插入，使正在运行的线程进入阻塞态，等运行完再运行原线程
    
### 13.位运算
    a|b 对应的二进制数按位进行或运算
    & 位与或逻辑与（非短路）
    ~ 位非
    ^ 位异或
    
### 14.初始化过程： 
1. 初始化父类中的静态成员变量和静态代码块 ； 
2. 初始化子类中的静态成员变量和静态代码块 ； 
3. 初始化父类的普通成员变量和代码块，再执行父类的构造方法；
4. 初始化子类的普通成员变量和代码块，再执行子类的构造方法； 

### 15.初始化
类成员域会有默认值 局部变量没有  
数组初始化后元素会有出初始值  
封装类初始化默认值为null(String、Byte)  
基本数据类型为0(byte)或false(boolean)

### 16.将GB2312编码的字符串转换为ISO-8859-1编码的字符串
String s2 = new String(s1.getBytes("GB2312"), "ISO-8859-1");

### 17.char定义
char ch = '烨' //字符  
char ch = 28904 //十进制unicode码  
char ch = 0x70e8 //16进制unicode码  
char ch = '\u70e8' //16进制unicode码  
char ch = 070350 //8进制unicode码  
char ch = '\70350' //8进制unicode码 

### 18.内部类实例化
T.Inner ti = new T().new Inner();

### 19.Array与ArrayList的区别
Array | ArrayList
---|---
声明时需实例化 | 允许仅声明
只能存同构对象 | 允许存异构对象
连续存放 | 不一定连续存放
大小固定 | 大小可动态变化
不可随意增删 | 可随意增删

### 20.interface
继承多个接口中如果有同名方法==不会==冲突

### 21.Integer
JVM会自动维护八种基本类型的常量池，int常量池中初始化-128~127的范围。自动装箱过程中取常量池中的值，超出范围需要new新的对象

    Integer e = 127;
	Integer f = 127; ->e==f

	Integer g = 128;
	Integer h = 128; ->g!=h

### 22.数组有length属性，String有length()方法

### 23.跳出指定多重循环或条件语句
    A:for(...)
       B:for(...)
            break A;
            
### 24. is A（继承|实现）has A（引用，定义为其属性）use A(作为参数注入)

### 25.重写方法只能保持或者扩大其访问范围