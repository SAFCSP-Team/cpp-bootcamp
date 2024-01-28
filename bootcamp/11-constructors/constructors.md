# Constructors
Imagine you have a special toy called "Toy Builder." When you want to create a new toy, you use this toy builder. The toy builder has a magic button called a constructor.

Now, this constructor is like a set of instructions that tells the toy builder how to create the new toy. It knows what the toy should look like and what features it should have.

In programming, constructors work similarly. They are special instructions inside a program that tell the computer how to create objects, just like the toy builder creates new toys. When you use a constructor in your program, it automatically sets the initial values of the object's properties, like the color and size of the toy.

## Concept
A `Constructor` is a special function of a class that shares the same name as the class and is called by the compiler when the object of the class is created.

Constructors play a crucial role in object initialization and ensure that objects start with valid and meaningful values. By defining and using constructors.

### Constructor Characteristics:
   - Constructors have the same name as the class and do not have a return type, not even "void".
   - Constructors may have parameters to assign values during object creation.
   - Constructors can be overloaded, meaning you can have multiple constructors with different parameter lists, just like any function.

### Types of Constructors:
1. Default Constructors
```c++
ClassName() {
       // Constructor body
   }
```
- The default constructor takes no arguments and may or may not perform any initialization.
- It is typically used when you want to initialize the object's data with default values.
- If a class does not have any constructors defined, the compiler provides a default constructor.  
>  If you define any other constructor (parameterized or copy constructor) in a class, the compiler will not generate a default constructor unless you define one.


2. Parameterized Constructors
```c++
ClassName(parameters) {
       // Constructor body
   }
```
- Copy Constructors
 ```c++
ClassName(const ClassName& NameofObject ) {
       // Constructor body
   }
```


Constructors intro

Reference Variable and Argument (&)

