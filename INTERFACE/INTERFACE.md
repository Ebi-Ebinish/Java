# What is an Interface

An **Interface** is a **blueprint of behavior**.

It defines **WHAT a class must do**, but **not HOW it does it**.

Example:

```java
interface Payment {  
  
    void pay(int amount);  
  
}
```

Here:

pay() → only declared  
no body

---
#  Implementing an Interface
A class implements the interface and provides the **actual logic**.

```java
class CreditCardPayment implements Payment {  
  
    public void pay(int amount) {  
        System.out.println("Paid using Credit Card: " + amount);  
    }  
  
}
```

Another class:

```java
class UpiPayment implements Payment {  
  
    public void pay(int amount) {  
        System.out.println("Paid using UPI: " + amount);  
    }  
  
}
```

# Using Interface

```java
Payment payment = new CreditCardPayment();  
payment.pay(1000);
```

This is called **Runtime Polymorphism**.
# Interface vs Class

|Feature|Class|Interface|
|---|---|---|
|Object creation|Yes|No|
|Methods|Concrete + Abstract|Mostly abstract|
|Fields|Instance variables|Only constants|
|Inheritance|Single|Multiple|

Example:

class → extends  
interface → implements

# IMPORTANT 

Reference must be the interface name while creating the object and the object name that implemented classes.

By default the interface abstract methods are the public if you not put also It will be consider as a public.

When you implemented the interface you enforced to mention public to access every where.

when implemented time if you not put the public means the compile time error will occurs.

```java
Reference → interface  
Object → implementing class
```

# MULTIPLE INHERITENCE

Through this interface we can archive multiple interface by implementing multiple interface in a single class.
Example:
```java
interface A {
    void methodA();
}

interface B {
    void methodB();
}

class C implements A, B {
    public void methodA() {}
    public void methodB() {}
}
```

# Variables 

Interface variables are always public final.

why:
# Variables in Interface are Always `public static final`

In an interface, every variable is **automatically constant**.

```java
interface Test {  
    int x = 10;   // actually: public static final int x = 10;  
}
```

- You **cannot change** `x`.
- It is **shared by all classes**.

```java
class Demo implements Test {  
    public static void main(String[] args) {  
        System.out.println(x);  
    }  
}
```

 Trying to change it will give **compile-time error**.