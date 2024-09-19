## Day 1: Object-Oriented Programming (OOP) in Java
# Classes and Objects:

- Class: Blueprint for objects, containing fields and methods.
- Object: Instance of a class, representing real-world entities.
- Practice: Create a Car class with fields like color, make, model, and methods like start(), stop().

```public class Car {
    String color;
    String make;
    String model;

    public void start() {
        System.out.println("Car started.");
    }

    public void stop() {
        System.out.println("Car stopped.");
    }
}

public class Main {
    public static void main(String[] args) {
        Car myCar = new Car();
        myCar.color = "Red";
        myCar.start();
    }
}
```

#  1. Encapsulation:
- Concept: Bundling of data (fields) and methods into a single unit (class), and restricting access using access modifiers (private, public, protected).
- Practice: Use private for fields and provide public getter and setter methods for them.
```
public class Car {
    private String color;

    public String getColor() {
        return color;
    }

    public void setColor(String color) {
        this.color = color;
    }
}
```


# 2.Inheritance:

Concept: Allows one class to inherit fields and methods from another class.
```public class SportsCar extends Car {
    public void turboBoost() {
        System.out.println("Turbo boost activated!");
    }
}

public class Main {
    public static void main(String[] args) {
        SportsCar myCar = new SportsCar();
        myCar.start();
        myCar.turboBoost();
    }
}
```



#  3. Polymorphism:

- Method Overloading: Multiple methods with the same name but different parameters.
- Method Overriding: A subclass provides its specific implementation of a method already defined in the superclass.
- Practice: Overload the start() method in the Car class and override it in SportsCar.
```
public abstract class Vehicle {
    abstract void start();
    abstract void stop();
}

public class Car extends Vehicle {
    public void start() {
        System.out.println("Car started.");
    }

    public void stop() {
        System.out.println("Car stopped.");
    }
}

```

# 4.Abstraction:

- Concept: Hiding complex details and showing only the essentials.
- Practice: Create an abstract Vehicle class with abstract methods like start() and stop().

```
// Base class
class Animal {
    void speak() {
        System.out.println("Some animal sound");
    }
}

// Derived class Dog
class Dog extends Animal {
    @Override
    void speak() {
        System.out.println("Woof!");
    }
}

// Derived class Cat
class Cat extends Animal {
    @Override
    void speak() {
        System.out.println("Meow!");
    }
}

// Test class
public class Main {
    public static void makeAnimalSpeak(Animal animal) {
        animal.speak();
    }

    public static void main(String[] args) {
        Animal myDog = new Dog();
        Animal myCat = new Cat();
        
        makeAnimalSpeak(myDog);  // Output: Woof!
        makeAnimalSpeak(myCat);  // Output: Meow!
    }
}

```



# Day 2: Java Core Concepts

## Data Types, Variables, and Operators:

- Data Types: Primitive types (int, char, boolean, float, etc.), non-primitive types (arrays, classes).
Variables: Store data values.
- Operators: Arithmetic, relational, logical, bitwise, etc.
Practice: Declare variables, perform arithmetic operations, and use logical operators in a simple program.

```
public class Main {
    public static void main(String[] args) {
        int a = 10, b = 20;
        int sum = a + b;
        boolean isEqual = (a == b);

        System.out.println("Sum: " + sum);
        System.out.println("Are a and b equal? " + isEqual);
    }
}

```
## 2.Control Structures:

- If-Else Statement: Decision-making structure.
- Switch Statement: Select one of many code blocks to execute.
- Loops: for, while, do-while for repetition.
- Practice: Write a program to find if a number is even or odd using if-else and a program to print the first 5 natural numbers using a loop.
```
// If-Else Example
public class Main {
    public static void main(String[] args) {
        int number = 5;
        if (number % 2 == 0) {
            System.out.println(number + " is even.");
        } else {
            System.out.println(number + " is odd.");
        }
    }
}

// Loop Example
public class Main {
    public static void main(String[] args) {
        for (int i = 1; i <= 5; i++) {
            System.out.println(i);
        }
    }
}
```

# 3.Arrays:

- Definition: An array is a collection of similar types of data stored in a contiguous memory location.
- Practice: Declare and initialize an array, and write a program to print all elements of an array.

```
public class Main {
    public static void main(String[] args) {
        int[] numbers = {1, 2, 3, 4, 5};

        for (int number : numbers) {
            System.out.println(number);
        }
    }
}
```

 # 4.String Handling:

- String Methods: Learn methods like length(), substring(), toUpperCase(), etc.
- Practice: Write a program to manipulate a string (e.g., reversing a string).

```
public class Main {
    public static void main(String[] args) {
        String str = "Hello World";
        String reversed = new StringBuilder(str).reverse().toString();
        System.out.println("Reversed String: " + reversed);
    }
}
```
# 5.Wrapper Classes and Autoboxing/Unboxing:

- Concept: Wrapper classes (Integer, Double, etc.) provide a way to use primitive data types as objects.
- Autoboxing: Automatic conversion of primitive types to their corresponding object wrapper.
- Unboxing: Converting wrapper objects back to primitive types.
- Practice: Write code that demonstrates autoboxing and unboxing.