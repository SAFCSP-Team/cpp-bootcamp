# Inheritance

Imagine a series of classes to describe two kinds of polygons: rectangles and triangles. These two polygons have certain common properties, such as the values needed to calculate their areas: they both can be described simply with a height and a width (or base).

The Polygon class would contain members that are common for both types of polygon. In our case: width and height. And Rectangle and Triangle would be its derived classes, with specific features that are different from one type of polygon to the other.

## Concept

Creating new classes which retain characteristics of the `base class`. This process, known as `inheritance`, involves a `base class` and a `derived class`: The **derived class** `inherits` the members of the **base class**, on top of which it can add its own members.

The inheritance relationship of two classes is declared in the `derived class`. Derived classes definitions use the following syntax:

```cpp
class derived_class_name: public base_class_name
{

 };

```
## Implementation

* The code defines a base class called `Polygon` with the protected access specifier. It has two member variables, width and height, and a member function `setvalues()` to set the values of width and height.
```cpp
#include <iostream>
using namespace std;

class Polygon {
  protected:
    int width, height;
  public:
    void setvalues (int a, int b)
      { width=a; height=b;}
 };
```
* Two derived classes are defined: `Rectangle` and `Triangle`. Both derived classes inherit publicly from the `Polygon` base class.
```cpp
class Rectangle: public Polygon {
  public:
    int area ()
      { return width * height; }
 };

class Triangle: public Polygon {
  public:
    int area ()
      { return width * height / 2; }
  };
  
int main () {
  Rectangle rect;
  Triangle trgl;
  rect.setvalues (4,5);
  trgl.setvalues (4,5);
  cout << rect.area() << '\n';
  cout << trgl.area() << '\n';
  return 0;
}
```
## Examples


* Animal class is the base class it's have all attributes for Animal
```cpp

#include <iostream>
using namespace std;

/* base class */
class Animal {

   public:
    void eat() {
        cout << "I can eat!" << endl;
    }

    void sleep() {
        cout << "I can sleep!" << endl;
    }
};
```
* `Dog class` is derived from the Animal class. Since Dog is derived from Animal, members of Animal are accessible to Dog.

```cpp
/* derived class */
class Dog : public Animal {
 
   public:
    void bark() {
        cout << "I can bark! Woof woof!!" << endl;
    }
};

int main() {
    // Create object of the Dog class
    Dog dog1;

    // Calling members of the base class
    dog1.eat();
    dog1.sleep();

    // Calling member of the derived class
    dog1.bark();

    return 0;
}
```
  
## Projects

