# Inheritance

Imagine a series of classes to describe two kinds of polygons: rectangles and triangles. These two polygons have certain common properties, such as the values needed to calculate their areas: they both can be described simply with a height and a width (or base).

The Polygon class would contain members that are common to both types of polygon. In our case: width and height. Rectangle and Triangle would be its derived classes, with specific features that are different from one type of polygon to the other.

## Concept

`Inheritance` is one of the key features of object-oriented programming in C++, it allows us to create a new class (derived class) from an existing class (base class), and the derived class inherits the features **properties and characteristics** from the base class and can have additional features of its own.

`Inheritance` involves a `base class` and a `derived class`: The **derived class** `inherits` the members of the **base class**, on top of which it can add its own members.

The inheritance relationship of two classes is declared in the `derived class`. 
- Derived classes definitions use the following syntax:

```cpp
class derived_class_name: public base_class_name
{

 };

```
> For more information about access modifiers of the base class.  [Access control of base class](https://www.ibm.com/docs/en/i/7.2?topic=only-access-control-base-class-members-c)

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
* Two derived classes are defined `Rectangle` and `Triangle`, both derived classes inherit publicly from the `Polygon` base class.
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
Output 
```
20
10
```
* One derived class `Square` can inherit publicly from more than one base class `Rectangle` and `Polygon`.
```cpp
class Square: public Rectangle{
public:
    int area() {
        return width * width;
    }
};

int main() {
    Square square;

    square.setvalues(4,4);
    cout << "Area of square: " << square.area() << '\n';

    square.setvalues(4,5);
    cout << "Area of rectangle: " << square.Rectangle::area() << '\n';

    return 0;
}
```
Output
```
Area of square: 16
Area of rectangle: 20

```
By inheriting from `Rectangle`, the `Square` class automatically inherits the properties and methods of both `Rectangle` and `Polygon`.

* Derived class `ManagerAssistant` inherits publicly from `Employee` and `Manager`

```cpp
#include <iostream>
using namespace std;

// Base class: Employee
class Employee {
protected:
    string name;
    int id;

public:
    Employee(string n, int i) : name(n), id(i) {}

    void displayInfo() {
        cout << "Name: " << name << endl;
        cout << "ID: " << id << endl;
    }
};

// Base class: Manager
class Manager {
protected:
    string department;

public:
    Manager(string dep) : department(dep) {}

    void displayDepartment() {
        cout << "Department: " << department << endl;
    }
};

// Derived class: ManagerAssistant
class ManagerAssistant : public Employee, public Manager {
public:
    ManagerAssistant(string n, int i, string dep) : Employee(n, i), Manager(dep) {}

    void displayDetails() {
        displayInfo();          // Accessing member of Employee
        displayDepartment();    // Accessing member of Manager
    }
};

int main() {
    ManagerAssistant assistant("Mouhannd", 12345, "Sales");

    assistant.displayDetails();

    return 0;
}
```

Output
```
Name: Mouhannd
ID: 12345
Department: Sales
```

## Examples

* `Animal` class is the base class, it has all attributes of the `Animal`.
  
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
* The `Dog` class is derived from the `Animal `class. Since `Dog` is derived from `Animal`, members of `Animal` are accessible to `Dog`.

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
Output
```
I can eat!
I can sleep!
I can bark! Woof woof!!

```
  
## Project 

- [Inheritance](https://github.com/SAFCSP-Team/inheritance-cpp) 


