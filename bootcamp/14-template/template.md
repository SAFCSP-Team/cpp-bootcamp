# Introduction to Template

Imagine you're working on a retail store software application that needs to handle and process different types of products, such as electronics, clothing, and groceries. To achieve a generic and reusable solution, you can utilize templates or generics in your implementation.


## Concept

In C++, `templates` , also known as generics, provide a way to create `function` and `class` that can work with different data types without having to write separate implementations for each type. 

Templates enable you to write code that is reusable and generic, allowing you to create algorithms and data structures that are independent of specific data types.

### Function template
* Here is a simple template function that swaps two values:

```cpp
template <typename T>
void Values(T& a, T& b) {
    T temp = a;
    a = b;
    b = temp;
}
```

* `T` is the type parameter representing the generic type. 
* The `typename` keyword is used to indicate that T is a type parameter. 
* The `swapValues` function takes two references (a and b) of type T and swaps their values using a temporary variable.

 * To use the `swapValues` function, you can call it with arguments of any compatible type:

```cpp
int main() {
    int x = 5, y = 10;
    swapValues(x, y);  // Swaps the values of x and y

    std::string a = "Hello", b = "World";
    swapValues(a, b);  // Swaps the values of a and b

    std::cout << "x: " << x << ", y: " << y << std::endl;
    std::cout << "a: " << a << ", b: " << b << std::endl;

    return 0;
}

```

### Class template
Templates can also be used with classes, allowing you to create generic data structures. Here's a simple example of a template class for a stack:

* Here is a simple template to define the template class `Stack` with a single type parameter T :

The class has three private member variables: elements (an array of type T), top (representing the index of the top element), and capacity (the maximum number of elements the stack can hold).

```cpp
template <typename T>
class Stack {
private:
    T* elements;
    int top;
    int capacity;

public:             // Constructor
    Stack(int size) : capacity(size), top(-1) {
        elements = new T[capacity];
    }

    ~Stack() {     // Destructor
        delete[] elements;
    }
    void push(T item) {
        if (top == capacity - 1) {
            // Stack is full, handle the overflow
            return;
        }
        elements[++top] = item;
    }
    T pop() {
        if (top == -1) {
            // Stack is empty, handle the underflow
            return T();
        }
        return elements[top--];
    }
};

```

####  Use the Stack class with specific types in the main function:

* Create an intStack object of type `Stack<int>` with a capacity of 10.
```cpp
int main() {
    Stack<int> intStack(10);  // Stack of integers
    intStack.push(5);
    intStack.push(10);
    int poppedInt = intStack.pop();
    return 0;
}
```

*  Create a doubleStack object of type `Stack<double>` with a capacity of 5.
```cpp
int main() {
    Stack<double> doubleStack(5);  // Stack of doubles
    doubleStack.push(3.14);
    doubleStack.push(2.71);
    double poppedDouble = doubleStack.pop();

    return 0;
}
```

> Note that the compiler generates separate classes for each instantiation of the Stack template, ensuring type safety and efficient code generation.

## Examples



## Projects
