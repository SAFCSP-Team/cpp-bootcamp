# Operator Function
We know that the operators such as `+`, `-`, `*`, etc. are used to perform operations on the variables and values.

What if we want to perform different operations on the variables and values? For example, we want the `<<` operator to print a variable of the type list. We can do this by **overloading** the operator `<<` to perform the print operation on the variable of the type list.

# Concept
In C++, we can overload the operators to perform different operations on the variables and values. The overloaded operators are called **operator functions**. These functions are declared with the keyword `operator`, followed by the overloaded operator `symbol`. 

> Operator functions can be defined either as member functions of a class or as non-member functions.


### Syntax
```
class ClassName {
    public: 
        <returnType> operator<symbol-operator>(<arguments>) {
           // define what the operator does
           return <value>;
        } 
};
    
```

# Example
In this example, we will overload the `+=` operator to add a new element to the end of the list variable.
```cpp
#include <iostream>
#include <list>
using namespace std;


// Overload '+=' operator to add a new element to the end of the list
list<int>& operator+=(list<int>& list1, int num) {
    list1.push_back(num);
    return list1;
}

int main() {

    list<int> numbers;

    // calling overloaded += operator
    numbers+=10;
    numbers+=20;
    numbers+=30;

    for(int i : numbers) {
        cout << i << endl;
    }

    return 0;
}
```

**OUTPUT:**
```
10
20
30
```

# Project
- [Operator Function](https://github.com/SAFCSP-Team/operator-function-project/blob/main/README.md) 
