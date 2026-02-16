## What is Access modifier?

Access modifiers are keywords that define the visibility (scope of accessibility) of classes, methods, variables, and constructors.

## Types of access modifier

1. Public  
2. Private  
3. Protected  
4. Default  

---
## Public Access Modifier

Access anywhere outside of the class and outside of the packages.
## Private Access Modifier

More restrictive accessible only within the class.
## Protected Access Modifier

Accessible within the dame package.  
Visible in the subclass (The subclass from other packages also accessible).
## Default

If you don’t specify any access modifier It’s a package private  
Accessible only within the packages.

---
## Tricky

### 1. Private Members and Inheritance

Trick: Private members are inherited but not visible to subclasses.

```java
class Parent {
private int num = 10;
}

class Child extends Parent {
void show() {
// System.out.println(num); ❌ Error
}
}
```

Why means: inheritance means everything is accessible” — but private means “inherit only physically, not logically.
### 2. Protected Outside Package

Trick: Protected members are accessible in subclasses only through inheritance, not through object references outside the package.

```java
package pack1;
public class Parent {
    protected int data = 10;
}

package pack2;
import pack1.Parent;
class Child extends Parent {
    void show() {
        System.out.println(data); // ✅ Works via inheritance
    }
}

class Test {
    public static void main(String[] args) {
        Parent p = new Parent();
        // System.out.println(p.data); ❌ Error outside package
    }
}
```
