# What is an Interface

An **Interface** is a **blueprint of behavior**.

It defines **WHAT a class must do**, but **not HOW it does it**.

Example:

interface Payment {  
  
    void pay(int amount);  
  
}

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