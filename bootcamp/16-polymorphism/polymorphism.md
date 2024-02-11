# Polymorphism
Imagine that you have a base class called `Animal`, and you want to model different types of animals such as dogs, cats, and birds. Each animal can make a sound, but their sound is specific to their type. Polymorphism allows us to treat these different types of animals uniformly through a common base class interface.

## Concept

`Polymorphism` is a fundamental concept in OOP that allows objects of different types to be treated as objects of a common base type. It enables code to be written more generically and flexibly, facilitating code reuse and extensibility.


## Implementation

 `Polymorphism` is achieved through the use of `virtual functions ` and `pointers` or references to `base class` objects. Here's how it works:

* Base Class with `Virtual Functions`:
  
> The virtual keyword indicates that this function may be overridden by derived classes.
```cpp
class Shape {
public:
    virtual void draw() {
        /* Base implementation */
    }
};
```


* Derived Classes `Circle` and `Square` with Overridden Functions:
  
 Class `Circle` and `Square`, which inherit publicly from the `Shape` base class, are Both derived classes that override the `draw()` function with their own specific implementations.
 
```cpp
class Circle : public Shape {
public:
    void draw() override {
        // Implementation specific to Circle
    }
};

class Square : public Shape {
public:
    void draw() override {
        // Implementation specific to Square
    }
};
```


* Polymorphic Usage

 Create two pointers of type Shape* that can point to objects of derived classes. We initialize shape1 to point to a `Circle` object and shape2 to point to a `Square` object.

 When we call the `draw()` function on shape1 and shape2, the appropriate overridden function based on the actual object type is called. This is known as dynamic or runtime binding, where the function to be called is determined at runtime based on the actual object type.


```cpp

int main() {
    Shape* shape1 = new Circle();
    Shape* shape2 = new Square();

    shape1->draw();  /* Calls the draw() function of Circle */
    shape2->draw();  /* Calls the draw() function of Square */

    delete shape1;
    delete shape2;

    return 0;
}
```
This example showcases how polymorphism allows us to write code that can work with different derived class objects through a common base class interface. It provides flexibility, code reusability, and the ability to handle varying types of objects in a unified way.

## Examples

Create the `Animal` base class and the derived classes `Dog`, `Cat`, and `Bird`. Each derived class overrides the `makeSound() `function with its specific implementation.

```cpp
#include <iostream>

class Animal {
public:
    virtual void makeSound() {
        std::cout << "Animal makes a generic sound." << std::endl;
    }
};

class Dog : public Animal {
public:
    void makeSound() override {
        std::cout << "Dog barks." << std::endl;
    }
};

class Cat : public Animal {
public:
    void makeSound() override {
        std::cout << "Cat meows." << std::endl;
    }
};

class Bird : public Animal {
public:
    void makeSound() override {
        std::cout << "Bird chirps." << std::endl;
    }
};
```
In the main method create pointers of type Animal* that can point to objects of derived classes. We initialize animal1 to point to a Dog object, animal2 to point to a Cat object, and animal3 to point to a Bird object and call the `makeSound()` function on each object.
```cpp
int main() {
    Animal* animal1 = new Dog();
    Animal* animal2 = new Cat();
    Animal* animal3 = new Bird();

    animal1->makeSound(); 
    animal2->makeSound();  
    animal3->makeSound();  

    delete animal1;
    delete animal2;
    delete animal3;

    return 0;
}
```

The output is

```
Dog barks.
Cat meows.
Bird chirps.
```
  
## Project 
| Project Title | Deadline |
|:-----------:|:-------------:|
| [Polymorphism](https://github.com/SAFCSP-Team/polymorphism-cpp) | - | 



