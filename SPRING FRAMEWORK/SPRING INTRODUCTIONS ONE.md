# Spring Framework

## What is Spring in Java?

Spring is a Java framework that helps you build enterprise-level applications easily.  

**In short:**  
**Spring = makes Java development simpler, cleaner, and more flexible**

It mainly helps with:  
- Object creation  
- Dependency management  
- Database access  
- Web applications  
- Security  
- Microservices  

Spring bean (object) creation can be configured using XML, Java configuration, or annotations. XML is optional and mostly legacy.  

---

### Spring Bean Creation (XML-based)

In Spring Framework, when using XML-based configuration, object (bean) definitions are written in the XML file.

- ✔ Spring Framework can create objects  
- ✔ Objects are called beans  
- ✔ Beans are defined using `<bean>` tags  
- ✔ Beans are created in JVM heap memory  
- ✔ Spring IoC container manages them  
- ✔ XML configuration is a valid and correct approach  

---

### Objects (Beans)

Spring-created objects are stored in JVM heap memory, and the `ApplicationContext` manages them by maintaining references and lifecycle information.

- Before Spring, you controlled object creation using `new`.  
- With Spring, the framework controls object creation and wiring (IoC).  