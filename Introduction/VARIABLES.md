# VARIABLES

Variable is a named memory location used to store data values,  
Before using a variable, it must be declared,  
Use to define to respected datatypes.
## Type:

1. Local variable
2. Instance variable(Non static variable)
3. Class variable(static variable)
# LOCAL VARIABLE:

1. Must be declare inside a method and constructor or block.
2. It doesn’t have a default value
3. It must be initialized before use it
4. You can access via directly calling the variable names.
5. You can’t access outside of the methods
6. Declare in methods parameter also.
7. Local variable cannot have access modifier.

**NOTE:** You have declared but not initialized and you didn’t use that variable anywhere JVM never cares about that variables.

**Key:** But in main methods use can access it. Not directly to the variable via calling that Objects or creating object.  
That object execute that methods codes.

---
# INSTANSE VARIABLE:

Instance variable also known as non-static variable.  
Instance variable is created in the class outside of the method, constructor and blocks.  
Initialization of an instance variable is not mandatory. It has the default value.

Belongs to each object of a class.  
Each object gets its own copy.  
Changing the variable in one object does not affect other objects.

It has the access only by creating object for class.

## What is an Instance Block?

An instance block is a block of code inside a class that runs automatically every time an object is created, before the constructor runs.

Instance blocks as "extra setup code" that always runs before the constructor.

---
# STATIC VARIABLE:

Static variable also called class variables.  
Static variable are similar to instance variable, just before use static keyword for declaration.  
Static variable has only one copy per class.

Belongs to the class itself, not to any individual object.  
Only one copy exists in memory, shared by all objects.  
If one object changes it, the change is reflected for all objects.

## What is a Static Block?

A static block (also called a static initializer block) is a block of code inside a class that is executed only once, when the class is loaded into memory (before any objects are created, and even before the main method runs).

---
# Updated:

The methods always prefers a local variable.  
When It doesn’t declare it will go for instance variable if avalable

---
# JAVA TYPE CASTING

Widening Casting (automatically) - converting a smaller type to a larger type size  
byte -> short -> char -> int -> long -> float -> double

Narrowing Casting (manually) - converting a larger type to a smaller size type  
double -> float -> long -> int -> char -> short -> byte

---
## Widening Casting

Smaller type → Larger type.  
Done automatically by Java.  
No data loss.

byte → short → int → long → float → double  
char → int → long → float → double

Widening casting is done automatically when passing a smaller size type to a larger size type:

---
## Narrowing Casting

Larger type → Smaller type.  
Requires manual casting using (type).  
May cause data loss or overflow.

Narrowing casting must be done manually by placing the type in parentheses () in front of the value:

---

**NOTE:** In a big place we can keep small thinks  
In a small place we can’t keep big thinks  
Different format data types also need casting

---
## 1. Convert between different data sizes (memory bits)

Primitive data types have different sizes:

|Type|Size (bits)|Example Value|
|---|---|---|
|byte|8|-128 to 127|
|short|16|-32,768 to 32,767|
|int|32|-2^31 to 2^31-1|
|long|64|Huge integers|
|float|32|Decimal values|
|double|64|Larger decimal values|
|char|16 (unsigned)|Characters|
|boolean|1 (conceptually)|true/false|

---
# Widening Conversions (Automatic / Implicit Casting)

From → To

byte → short  
short → int  
char → int  
int → long  
long → float  
float → double

---
# Narrowing Conversions (Manual / Explicit Casting)

From → To

int → byte  
long → int  
double → float  
float → int  
char → byte