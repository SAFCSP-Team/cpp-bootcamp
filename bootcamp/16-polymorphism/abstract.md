# Abstract

## Concept
`Abstract class` is a class that is designed to be specifically used as a `base class`. An abstract class contains at least one `pure virtual function`. You declare a **pure virtual function** by using a **pure specifier (= 0)** in the declaration of a virtual member function in the class declaration.


## Implementation

The following is an example of an abstract class:

* Create an abstract class by declaring at least one pure virtual member function. That's a virtual function declared by using
  the pure specifier (= 0) 
  syntax. Classes derived from the abstract class must implement the pure virtual function or they, too, are abstract classes.
  
```CPP
class Shape {
public:
   virtual double getArea() const = 0;
};
```

If the constructor for an abstract class calls a pure virtual function, either directly or indirectly, the result is undefined. However, constructors and destructors for abstract classes can call other member functions.


## Example
* In this example, the `Shape` class is an `abstract` base class that defines pure virtual functions for calculating the area, perimeter, and printing details of a shape. It serves as an abstraction for any general shape.
* The `Rectangle` and `Circle` classes inherit from `Shape` and provide concrete implementations of these virtual functions.
  
```cpp
#include <iostream>
#include <cmath>

// Abstract base class for shapes
class Shape {
public:
    virtual double getArea() const = 0; /* Pure virtual function */
    virtual double getPerimeter() const = 0; /* Pure virtual function */
    virtual void printDetails() const = 0;  /* Pure virtual function */
};

/* Concrete derived class for a rectangle */
class Rectangle : public Shape {
private:
    double length;
    double width;

public:
    Rectangle(double length, double width) : length(length), width(width) {}

    double getArea() const override {
        return length * width;
    }

    double getPerimeter() const override {
        return 2 * (length + width);
    }

    void printDetails() const override {
        std::cout << "Rectangle: Length = " << length << ", Width = " << width << std::endl;
    }
};

/* Concrete derived class for a circle */
class Circle : public Shape {
private:
    double radius;

public:
    Circle(double radius) : radius(radius) {}

    double getArea() const override {
        return M_PI * radius * radius;
    }

    double getPerimeter() const override {
        return 2 * M_PI * radius;
    }

    void printDetails() const override {
        std::cout << "Circle: Radius = " << radius << std::endl;
    }
};
```
* In the main function, we create instances of `Rectangle` and `Circle` and store their addresses in Shape pointers (shape1 and shape2). This allows us to call the virtual functions getArea, getPerimeter, and printDetails on these pointers, which dynamically dispatches the appropriate function based on the actual object type.
```cpp

int main() {
    Rectangle rectangle(5.0, 3.0);
    Circle circle(2.5);

    Shape* shape1 = &rectangle;
    Shape* shape2 = &circle;

    shape1->printDetails();
    std::cout << "Area: " << shape1->getArea() << ", Perimeter: " << shape1->getPerimeter() << std::endl;

    shape2->printDetails();
    std::cout << "Area: " << shape2->getArea() << ", Circumference: " << shape2->getPerimeter() << std::endl;

    return 0;
}

```
  
## Projects
