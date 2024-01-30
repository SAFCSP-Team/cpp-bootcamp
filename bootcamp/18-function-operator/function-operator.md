# Operator Functions
We know that the operators such as `+`, `-`, `*`, `/`, `%`, `++`, `--`, `<<`, `>>`, `==`, `!=`, `>`, `<`, `>=`, `<=`, `&&`, `||`, `!`, `&`, `|`, `^`, `~`, `+=`, `-=`, `*=`, `/=`, `%=`, `<<=`, `>>=`, `&=`, `|=`, `^=`, `[]`, `()`, `->`, `->*` are used to perform operations on the variables and values.

What if we want to perform different operations on the variables and values? For example, we want `<<` operator to perform print variable of type list. We can do this by **overloading** the operator `<<` to perform print operation on the variable of type list.

# Concept
In C++ we can overload the operators to perform different operations on the variables and values. The overloaded operators are called **operator functions**. The operator functions are the functions that are declared with the keyword `operator` followed by the operator to be overloaded. The operator functions can be declared as member functions or non-member functions.

```cpp
ostream& operator<<(ostream& os, const list<T>& list) {
    for (auto& i : list) {
        os << i << " ";
    }
    return os;
}
```


# Example
In this example we will overload the += operator to perform addition on the list variables.
`numList += 10;`.

```cpp
#include <iostream>
#include <list>
using namespace std;

// overload += operator for list<int>
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