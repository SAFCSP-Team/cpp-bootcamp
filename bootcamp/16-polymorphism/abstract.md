# Abstract

## Concept
`Abstract class` is a class that is designed to be specifically used as a `base class`. An abstract class contains at least one `pure virtual function`. You declare a **pure virtual function** by using a **pure specifier (= 0)** in the declaration of a virtual member function in the class declaration.


## Implementation

The following is an example of an abstract class:

* Create an abstract class by declaring at least one pure virtual member function. That's a virtual function declared by using the pure specifier (= 0) 
  syntax. Classes derived from the abstract class must implement the pure virtual function or they, too, are abstract classes.
  
```CPP
class Shape {
public:
   virtual double getArea() const = 0;
};
```


  
## Projects
