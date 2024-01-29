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
   - Constructors can be overloaded, just like regular functions, by having different parameter lists.
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
- A parameterized constructor is a constructor that takes one or more parameters.
- A parameterized constructor allows you to initialize the object's data with values provided during object creation.
- Parameterized constructors are useful when you want to initialize an object with different values each time.

3. Copy Constructors
 ```c++
ClassName(const ClassName &NameofObject ) {
       // Constructor body
   }
```
4. Copy Constructor:
- The copy constructor is a special constructor that creates a new object as a copy of an existing object.
- If a class does not provide a copy constructor explicitly, the compiler generates a default copy constructor
- Pass object by Reference: By using a reference variable as a parameter in a constructor, you can pass arguments by reference. This means that any changes made to the parameter within the constructor will affect the original argument passed to the constructor.
- The const Keyword is optional with Reference Variables to show that the reference is immutable and should not be modified within the constructor.


### Initialization List:

The initialization list allows you to initialize member variables directly, before the body of the constructor is executed. 
   - Both default constructors and parameterized constructors can use initialization lists.
   - Initialization lists are specified after the colon (`:`) following the constructor's parameter list.

The syntax of an initialization list

```c++
ClassName(parameters) : variable1 (value1), variable2 (value2), ..., variableN(valueN) {
    // Constructor body 
}
```

## Examples
## Project

