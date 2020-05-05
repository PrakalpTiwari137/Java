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
if(condition1) {
    ...
}
else if(condition2){
    ...
}
...
else {
    ...
}
```
```java
// if-else using ternary operator
(number%2==0) ? "Even number" : "Odd number";
```

<br/>**switch-case statement**
```java
switch(expression) {
    case value1:
        ...
        break; // optional
    case value2:
        ...
        break; // optional
    .....
    default:
        ...
}
```
**Note:** Java allows us to use strings in switch expression. The case statement should be a string literal.<br/>
**Note:** Java allows us to use enum in switch statement.<br/><br/>

## Java Loops
Java loops are like C-loop in syntax.<br/>
We only see the special cases here:<br/><br/>

**Java for-each Loop:**<br/>
The for-each loop is used to traverse array or collection in java. It is easier to use than simple for loop because we don't need to increment value and use subscript notation. It works on elements basis not index. It returns element one by one in the defined variable.
```java
int arr[]={12,23,44,56,78};  
for(int i:arr) {  
    System.out.println(i);  
}  
```

<br/>**do-while Loop**
```java
do {
    ...
} while(condition);
```


