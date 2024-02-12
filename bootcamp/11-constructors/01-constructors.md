# Constructors
Imagine you have a special toy called "Toy Builder." When you want to **create a new toy, you use this toy builder**. The toy builder has a magic button called a `constructor`.

Now, this **constructor is like a set of instructions that tells the toy builder how to create the new toy**. It knows what the toy should look like and what features it should have.

In programming, constructors work similarly. They are special instructions inside a program that tell the computer how to create objects, just like the toy builder creates new toys. When you use a constructor in your program, it automatically sets the initial values of the object's properties, like the color and size of the toy.

## Concept
A `Constructor` is a **special function** of a class that shares the **same name as the class** and is **called by the compiler when the object of the class is created**.

Constructors play a crucial role in object initialization and ensure that objects start with valid and meaningful values, by defining and using constructors.

### Constructor Characteristics
   - Constructors have the **same name as the class** and **do not have a return type**, not even "void".
   - Constructors **may have parameters** to assign values during object creation.
   - Constructors **can be overloaded**, just like regular functions, by having different parameter lists.
   - Constructors can be defined both **inside and outside the class declaration**, just like regular [functions](https://www.prepbytes.com/blog/cpp-programming/member-function-in-cpp-and-types/). 


### Types of Constructors
1. Default Constructors
```c++
ClassName() {
       // Constructor body
   }
```
- The default constructor **takes no arguments** and may or may not perform any initialization.
- It is typically **used when you want to initialize the object's data with default values**.
- If a class does not have any constructors defined, the **compiler provides a default constructor**.  
>  If you define any other constructor (parameterized or copy constructor) in a class, the compiler will not generate a default constructor unless you define one.


2. Parameterized Constructors
```c++
ClassName(parameters) {
       // Constructor body
   }
```
- A parameterized constructor is a constructor that **takes one or more parameters**.
- A parameterized constructor allows you to **initialize the object's data with values provided during object creation**.
- Parameterized constructors are useful when you want to **initialize an object with different values each time**.

3. Copy Constructors
 ```c++
ClassName(const ClassName& NameofObject ) {
       // Constructor body
   }
```
- The copy constructor is a **special constructor** that **creates a new object as a copy of an existing object**.
- If a class does not provide a copy constructor explicitly, **the compiler generates a default copy constructor**.
- Pass object by Reference: By **using a reference variable as a parameter** in a constructor, you can pass arguments by reference. This means that **any changes made to the parameter within the constructor will affect the original argument passed to the constructor.**
- The `const` Keyword is optional with Reference Variables to show that the **reference is fixed and should not be modified within the constructor**.


### Initialization List

The initialization list (a.k.a initialized list) allows you to **initialize variables directly before the constructor's body is executed**. 
   - Both default constructors and parameterized constructors can use initialization lists.
   - **Initialization lists are specified after the colon (`:`)** following the constructor's parameter list.

The syntax of an initialization list

```c++
ClassName(parameters) : variable1 (value1), variable2 (value2), ..., variableN(valueN) {
    // Constructor body 
}
```
- `parameters` represents the list of parameters the constructor accepts, if any.
- `variable1`, `variable2`, ..., `variableN` are the names of the class variables you want to initialize.
- `value1`, `value2`, ..., `valueN` are the values that you want to assign to the corresponding variables.

## Example
```c++
#include <iostream>

class Triangle {
private:
    double side1;
    double side2;
    double side3;

public:
// Constructor declaration (prototype) to implement outside the class 
Triangle(double s1, double s2);

    // Default constructor
    Triangle() {
        side1 = 0.0;
        side2 = 0.0;
        side3 = 0.0;
    }

    // Parameterized constructor
    Triangle(double s1, double s2, double s3) {
        side1 = s1;
        side2 = s2;
        side3 = s3;
    }
    
    // Parameterized constructor using the initialization list
    Triangle(double s1) : side1(s1), side2(7.7), side3(6.2) {}


    // Copy constructor
    Triangle(const Triangle& object) {
        side1 = object.side1;
        side2 = object.side2;
        side3 = object.side3;
    }



    // function to print the sides of the triangle
    void printSides() {
        std::cout << "Side 1: " << side1 << std::endl;
        std::cout << "Side 2: " << side2 << std::endl;
        std::cout << "Side 3: " << side3 << std::endl;
    }
};

    // Parameterized constructor definition (implementation) outside the class 
    Triangle::Triangle(double s1, double s2) {
        side1 = s1;
        side2 = s2;
        side3 = 5.5;
    }


int main() {
    // Using default constructor
    Triangle triangle1;
    std::cout << "Triangle 1 (default constructor):" << std::endl;
    triangle1.printSides();

    // Using parameterized constructor
    Triangle triangle2(3.0, 4.0, 5.0);
    std::cout << "Triangle 2 (parameterized constructor):" << std::endl;
    triangle2.printSides();
  
    // Using a Parameterized constructor that using an initialization list
    Triangle triangle3(3.0);
    std::cout << "Tringle 3 (parameterized constructor):" << std::endl;
    triangle3.printSides();

    // Using a parameterized constructor that is outside the class
    Triangle triangle4(3.0, 2.0);
    std::cout << "Tringle 4 (parameterized constructor):" << std::endl;
    triangle4.printSides();

    // Using copy constructor
    Triangle triangle5(triangle2);
    std::cout << "Triangle 5 (copy constructor - copied from Triangle 2):" << std::endl;
    triangle5.printSides();

    // Using copy constructor
    Triangle triangle6 = triangle3;
    std::cout << "Triangle 6 (copy constructor - copied from Triangle 3):" << std::endl;
    triangle6.printSides();
    
    return 0;
}
```
```
Triangle 1 (default constructor):
Side 1: 0
Side 2: 0
Side 3: 0
Triangle 2 (parameterized constructor):
Side 1: 3
Side 2: 4
Side 3: 5
Tringle 3 (parameterized constructor):
Side 1: 3
Side 2: 7.7
Side 3: 6.2
Tringle 4 (parameterized constructor):
Side 1: 3
Side 2: 2
Side 3: 5.5
Triangle 5 (copy constructor - copied from Triangle 2):
Side 1: 3
Side 2: 4
Side 3: 5
Triangle 6 (copy constructor - copied from Triangle 3):
Side 1: 3
Side 2: 7.7
Side 3: 6.2
```
- Triangle 5: uses direct initialization syntax, where the copy constructor is explicitly called with parentheses `Triangle triangle5(triangle2);`.
- Triangle 6: uses copy initialization syntax with the assignment operator and the equals sign `Triangle triangle6 = triangle3;`.
  
Both approaches achieve the same result of creating a new object by copying the data from an existing object.

## Project 
| Project Title | Deadline |
|:-----------:|:-------------:|
| [Constructors](https://github.com/SAFCSP-Team/constructors) | - | 


