# Inheritance
 
 
### Ex:
 
```java
public class Y extends W{}
```
 
- Class Y is a subclass (child class) of W, which is a superclass (parent class)
- Methods and fields are copied at runtime
- Classes cannot have more than one parent (no multiple inheritance)
 
 
### Ex:
 
```java 
class A {
    private int x;
    
    public A() {
        x = 8;
    }
    
    public A(int b) {
        x = b;
    }
    
    pulbic int getX() {
        return x;
    }
    
    public void setX(int b) {
        x = b;
    }
 
}
 
 
class B extends A{}
 
 
// Located in a runner class
 
A one = new A();
sout(one.getX());
one = new B();
sout(one.getX());
```
 
- The class contains 2 Constructors, 4 Methods, 1 Accessor Method, 1 Modifier Method, 1 Instance Variable
- Parent class can contain the child class; however, the children classes cannot contain the parent class
- All members containing `public` can be accessed by child classes, super classes, and other classes; however, if it contains `private`, it cannot
- These access modifier keywords are used to hide and show methods and fields
- A default constuctor is added to class B since a constructor was not specified (the constructor called `super()`)
 
### This and Super
 
#### Ex:
```java
class C extends A {
    private int y;
    
    public B(int b, int c) {
        super(b);
        y = c;
    }
    
    public int doSomething() {
        return super.getX() + 12;
    }
}
```
- `this` refers to the current class
- `super` refers to the parent class
- `super` always comes first in a constructor
- `super` is automatically called if not called directly
- Cannot access members of a grandparent directly from a grandchild class
 
### Overriding
 
- When you extend a class, you inherit all methods and instance variables
- You can override the original methods by defining a method with the same signature as one of the original methods located in the parrent class
- `super` calls are required to call the original method from the parent if the method in the child class is overriden


