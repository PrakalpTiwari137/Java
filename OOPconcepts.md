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
