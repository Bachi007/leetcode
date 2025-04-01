# Object-Oriented Programming in Java

## 1. Introduction
Object-Oriented Programming (OOP) is a programming paradigm based on the concept of objects.

## 2. Pillars of OOP
1. **Encapsulation** - Wrapping data and methods into a single unit.
2. **Inheritance** - Acquiring properties from a parent class.
3. **Polymorphism** - Having multiple forms (Method Overloading & Overriding).
4. **Abstraction** - Hiding implementation details.

## 3. Example Code

```java
class Parent {
    void show() {
        System.out.println("This is Parent Class");
    }
}

class Child extends Parent {
    void show() {
        System.out.println("This is Child Class");
    }
}

public class Main {
    public static void main(String[] args) {
        Parent obj = new Child();
        obj.show();  // Output: This is Child Class
    }
}
