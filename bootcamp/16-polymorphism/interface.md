# Interface
An interface is a class that is designed to be specifically used as a base class or parent class. In order to restrict the use of a class as a base class, and most importantly, to make the code loosely coupled.

Think of an interface as a class that only knows the name of the methods and their signatures. It does not know the implementation of the methods. The implementation is done by the derived classes or child classes. 

## Concept
Before dividing in interface, you must konw that pure virtual functions.

**Pure virtual functions** are function with no implementaiton block. 

e.g.
```cpp
virtual void foo() = 0;
```
By writing virtual and declare it as 0, you are telling the compiler that this function is a pure virtual function.

**Interface** is a class that only has **pure virtual functions**, and no **attributes**.

And if we defined a none pure virtual function in an interface, it will be no longer an interface, but an **abstract class**.

## Implementation
In this example, we will demonstrate how to create an interface, and how to use it.


1. Create an interface that has a pure virtual function.
```cpp
#include <iostream>
using namespace std;

// Interface
class IPerson {
    public:
    virtual void action() = 0; // pure virtual function
};
```

Now we have an interface called IPerson, and it has a pure virtual function called action().

2. Create two class that implements the interface.
```cpp
class Student : public IPerson {
    public:
    string name;
    string major;
    void action() {
        cout << "Study " << major << endl;
    }
};

class Teacher : public IPerson {
    public:
    string name;
    string major;
    void action() {
        cout << "Teach " << major << endl;
    }

};
```

3. Finally, we can test our code in main function.
```cpp
int main() {

    Student *student = new Student();
    student->major = "Computer Science";
    student->action();
    
    Teacher *teacher = new Teacher();
    teacher ->major = "Computer Science";
    teacher ->action();

    return 0;
}

```

**OUTPUT:**
```
Study Computer Science
Teach Computer Science

```