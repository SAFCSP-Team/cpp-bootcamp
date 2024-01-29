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

* Derived Classes with Overridden Functions:

> Class Circle and Square, which inherit publicly from the `Shape` base class. Both derived classes override the `draw()` function with their own specific implementations.
 
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

* Polymorphic Usage:


```cpp

int main() {
    Shape* shape1 = new Circle();
    Shape* shape2 = new Square();

    shape1->draw();  // Calls the draw() function of Circle
    shape2->draw();  // Calls the draw() function of Square

    delete shape1;
    delete shape2;

    return 0;
}
```

## Examples


  
## Projects

