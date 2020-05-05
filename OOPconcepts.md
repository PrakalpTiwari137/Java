# Object oriented approach in Java
## Java OOP concepts
### Inheritance
When one object acquires all the properties and behaviors of a parent object, it is known as inheritance. It provides code reusability. It is used to achieve runtime polymorphism.<br/><br/>
### Polymorphism
If one task is performed in different ways, it is known as polymorphism. In Java, we use method overloading and method overriding to achieve polymorphism.<br/><br/>
### Abstraction
Hiding internal details and showing functionality is known as abstraction. In Java, we use abstract class and interface to achieve abstraction.<br/><br/>
### Encapsulation
Binding (or wrapping) code and data together into a single unit are known as encapsulation. A java class is the example of encapsulation.<br/><br/>
### Coupling
Coupling refers to the knowledge or information or dependency of another class. In Java, we use private, protected, and public modifiers to display the visibility level of a class, method, and field.<br/><br/>

**Note:** Object-based programming language follows all the features of OOPs except Inheritance.<br/>

### Java class
Synatx to declare a class.
```java
class <class_name> {
    field;
    method;
}
```
<br/>**Instance variable in Java:** A variable which is created inside the class but outside the method is known as an instance variable. Instance variable doesn't get memory at compile time. It gets memory at runtime when an object or instance is created. That is why it is known as an instance variable.<br/>
<br/>**new keyword in Java:** The new keyword is used to allocate memory at runtime. All objects get memory in Heap memory area.<br/>

```java
class Student{  
    int id;  
    String name;  
} 
class TestStudent1{  
    public static void main(String args[]){  
        Student s1 = new Student();  
        System.out.println(s1.id);  
        System.out.println(s1.name);  
    }  
}
```
<br/>**Constructor Overloading in Java:** In Java, a constructor is just like a method but without return type. It can also be overloaded like Java methods.<br/>
Constructor overloading in Java is a technique of having more than one constructor with different parameter lists.
```java
class Student5{  
    int id;  
    String name;  
    int age;  
    //creating two arg constructor  
    Student5(int i,String n){  
        id = i;  
        name = n;  
    }  
    //creating three arg constructor  
    Student5(int i,String n,int a){  
        id = i;  
        name = n;  
        age=a;  
    }
}
```
### Java Static keyword
The static can be:<br/>
1. Variable (also known as a class variable)<br/>
2. Method (also known as a class method)<br/>
3. Block<br/>
4. Nested class<br/>

**1. Static variable:** The static variable can be used to refer to the common property of all objects (which is not unique for each object), for example, the company name of employees, college name of students, etc. The static variable gets memory only once in the class area at the time of class loading.<br/><br/>
**2. Static method:** A static method belongs to the class rather than the object of a class. A static method can be invoked without the need for creating an instance of a class. A static method can access static data member and can change the value of it.<br/>
```java
//Java Program to demonstrate the use of a static method.  
class Student{  
     int rollno;  
     String name;  
     static String college = "ITS";  
     //static method to change the value of static variable  
     static void change(){  
        college = "BBDIT";  
     }    
}  
public class TestStaticMethod{  
    public static void main(String args[]){  
    Student.change();   //calling change method  
    Student s1 = new Student();    
}  
```
**Note:** There are two main restrictions for the static method. They are:<br/>
1. The static method can not use non static data member or call non-static method directly.<br/>
2. this and super cannot be used in static context.<br/><br/>

### this keyword in Java
Usage:
```java
class Student{  
    int rollno;  
    String name;  
    float fee;  
    // 1. To refer current class instance variable
    Student(int rollno,String name,float fee){  
        this.rollno=rollno;  
        this.name=name;  
        this.fee=fee;  
    }
    
    // 2. To invoke current class method
    void m(){System.out.println("hello m");} 
    this.m();
    
    // 3. To invoke current class constructor 
    // used in constructor chaining
    Student(int rollno,String name,String course,float fee){  
        this(rollno,name,course);//reusing constructor  
        this.fee=fee;  
    }  
    
    // 4. To pass as an argument in the method
    // mainly used in event handling
    void m(Student obj){  
        System.out.println("method is invoked");  
    }  
    void p(){  
        m(this);  
    }
    
    // 5. To return current class instance
    Student getStudent(){  
        return this;  
    }  
}  
```

<br/><br/>

## Inheritance
```java
class Subclass-name extends Superclass-name  
{  
   //methods and fields  
}  
```
### Aggregation
```java
class Operation{  
    int square(int n){  
        return n*n;  
    }  
}  

class Circle{  
    Operation op;//aggregation  
    double pi = 3.14;  

    double area(int radius){  
        op=new Operation();  
        int rsquare = op.square(radius);  //code reusability 
        return pi*rsquare;  
    }
}
```

<br/><br/>

## Method Overriding
Rules for Java Method Overriding:<br/>
1. The method must have the same name as in the parent class.<br/>
2. The method must have the same parameter as in the parent class.<br/>
3. There must be an IS-A relationship (inheritance).<br/>
```java
class Bank{  
    int getRateOfInterest(){return 0;}  
}  
//Creating child classes.  
class SBI extends Bank{  
    int getRateOfInterest(){return 8;}  
}  
  
class ICICI extends Bank{  
    int getRateOfInterest(){return 7;}  
}
```
<br/>**Why can we not override static method?**<br/>
It is because the static method is bound with class whereas instance method is bound with an object. Static belongs to the class area, and an instance belongs to the heap area.<br/><br/>

## Runtime polymorphism
Runtime polymorphism or Dynamic Method Dispatch is a process in which a call to an overridden method is resolved at runtime rather than compile-time.<br/>
In this process, an overridden method is called through the reference variable of a superclass. The determination of the method to be called is based on the object being referred to by the reference variable.<br/>
If the reference variable of Parent class refers to the object of Child class, it is known as **upcasting**.<br/>
```java
class Animal{  
    void eat(){
        System.out.println("animal is eating...");
    }  
}  
class Dog extends Animal{  
    void eat(){
        System.out.println("dog is eating...");
    }    
}  
class BabyDog1 extends Dog{  
    public static void main(String args[]){  
        Animal a=new BabyDog1();  
        a.eat();    // output: Dog is eating 
    }
}
```

<br/><br/>

## 
