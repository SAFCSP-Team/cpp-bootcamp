# Template

Imagine you're working on a retail store software application that needs to handle and process different types of products, such as electronics, clothing, and groceries. To achieve a generic and reusable solution, you can utilize templates or generics in your implementation.


## Concept

In C++, `template`, also known as generic, provide a way to create `function` and `class` that can work with different data types without having to write separate implementations for each type. 

`Template` enable you to write code that is reusable and generic, allowing you to create algorithms and data structures that are independent of specific data types.

### Function template

* Here is a simple template function that adds two numbers:

```cpp
#include <iostream>
using namespace std;

template <typename T>
T add(T num1, T num2) {
   return (num1 + num2);
}
```

* `T` is the type parameter representing the generic type. 
* The `typename` keyword is used to indicate that T is a type parameter. 
* The `add` function takes two variables (a and b) of type T.
* To use the `add` function, you can call it with arguments of any compatible type:

```cpp

int main() {

    int result1;
    double result2;
    /* calling with int parameters */
    result1 = add<int>(2, 3);
    cout << result1 << endl;

    /* calling with double parameters */
    result2 = add<double>(2.2, 3.3);
    cout << result2 << endl;

    return 0;
} 
```
The output is
```
5
5.5
```

### Class template

Template can also be used with classes, allowing you to create generic data structures.

* Here is a simple template to define the template class `Number` with a single type parameter T :

```cpp
#include <iostream>
using namespace std;

/* Class template */
template <class T>
class Number {
   private:
    /* Variable of type T */
    T num;

   public:
    Number(T n) : num(n) {}   // constructor

    T getNum() {
        return num;
    }
};

```

 The `Number` class with specific types in the main function:

```cpp
int main() {

    /* create object with int type */
    Number<int> numberInt(7);

    /* create object with double type */
    Number<double> numberDouble(7.7);

    cout << "int Number = " << numberInt.getNum() << endl;
    cout << "double Number = " << numberDouble.getNum() << endl;

    return 0;
}
```


The output is 
```
int Number = 7
double Number = 7.7
```
## Examples

*  We define a template function `maximum()` that takes two parameters of the same type `T` and returns the maximum of the two values.
 ```cpp
#include <iostream>

/* Template function to find the maximum of two values */
template<typename T>
T maximum(T a, T b) {
    return (a > b) ? a : b;
}
```

* The `main()` function, we demonstrate the use of the template function. We first call `maximum()` with two int values (num1 and num2) and then print the result. Next, we call maximum() with two double values (num3 and num4) and print the result.

```cpp
int main() {
    int num1 = 10;
    int num2 = 20;
    std::cout << "Maximum of " << num1 << " and " << num2 << " is: " << maximum(num1, num2) << std::endl;

    double num3 = 3.14;
    double num4 = 2.71;
    std::cout << "Maximum of " << num3 << " and " << num4 << " is: " << maximum(num3, num4) << std::endl;

    return 0;
}

```

The output is 

```
Maximum of 10 and 20 is: 20
Maximum of 3.14 and 2.71 is: 3.14
```

* We define a template class `Pair` that represents a generic pair of two values. The class has two private data members: first of type T1 and second of type T2.

```cpp
#include <iostream>

/* Template class for a generic Pair */
template<typename T1, typename T2>
class Pair {
private:
    T1 first;
    T2 second;

public:
    Pair(T1 f, T2 s) : first(f), second(s) {}

    T1 getFirst() const {
        return first;
    }

    T2 getSecond() const {
        return second;
    }

    void display() const {
        std::cout << "(" << first << ", " << second << ")";
    }
};
```
* In the `main()` function, we demonstrate the use of the template class. We create two instances of the `Pair` class: p1 with an int and double pair, and p2 with a string and char pair. We then use the getter methods to retrieve the values and print them using std::cout.

```cpp

int main() {
    Pair<int, double> p1(10, 3.14);
    std::cout << "First: " << p1.getFirst() << ", Second: " << p1.getSecond() << std::endl;

    Pair<std::string, char> p2("Hello", 'A');
    std::cout << "First: " << p2.getFirst() << ", Second: " << p2.getSecond() << std::endl;

    return 0;
}
```

The output
```
First: 10, Second: 3.14
First: Hello, Second: A
```

## Project 
| Project Title | Deadline |
|:-----------:|:-------------:|
| [Template](https://github.com/SAFCSP-Team/template) | - | 


