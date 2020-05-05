## Java variables
```java
class A {
    int data = 50;  // instance variable  
    static int m = 100; // static variable
    void method() {
        int n = 90; // local variable
    }
}
```
**Instance variable:** Value is instance specific and not shared among instances.<br/>
**Static variable:** Value is static and is shared among all the instances.<br/>
**Local variable:** Declared inside a method andvisible only to that method.<br/><br/>

**Note:** Narrowing is also called as typecasting.<br/><br/>

## Java data types
### 1. Primitive datatype
boolean, byte, char, short, int, long, float, double<br/>
### 2. Non-primitive datatype
Classes, Interfaces, Arrays<br/><br/>

## Java conditional
**If-else statements**
```java
if(condition) {
    ...
}
else {
    ...
}
```
```java
// if-else using ternary operator
(number%2==0) ? "Even number" : "Odd number";
```
