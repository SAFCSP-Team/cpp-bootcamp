# Introduction to Template

Imagine you're working on a retail store software application that needs to handle and process different types of products, such as electronics, clothing, and groceries. To achieve a generic and reusable solution, you can utilize templates or generics in your implementation.


## Concept

In C++, `templates` , also known as generics, provide a way to create `function` and `class` that can work with different data types without having to write separate implementations for each type. 

Templates enable you to write code that is reusable and generic, allowing you to create algorithms and data structures that are independent of specific data types.

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

## Examples

Templates can also be used with classes, allowing you to create generic data structures. Here's a simple example of a template class for a stack:

Step 1: Define the template class Stack:

* We define the template class `Stack` with a single type parameter T. The class has three private member variables: elements (an array of type T), top (representing the index of the top element), and capacity (the maximum number of elements the stack can hold).

* The class provides a constructor that takes the size of the stack and initializes the capacity and top variables. It also dynamically allocates memory for the elements array using new.

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
}

* The ~Stack() destructor is responsible for deallocating the memory used by elements using delete[].

```cpp
    ~Stack() {     // Destructor
        delete[] elements;
    }
```

* The `push` method adds an item of type T to the stack. It first checks if the stack is full (indicated by top == capacity - 1) and handles the overflow condition if necessary. Otherwise, it increments top and assigns the item to elements[top].

```cpp
    void push(T item) {
        if (top == capacity - 1) {
            // Stack is full, handle the overflow
            return;
        }
        elements[++top] = item;
    }
```
* The `pop` method removes and returns the top element from the stack. It checks if the stack is empty (indicated by top == -1) and handles the underflow condition if necessary. Otherwise, it returns the element at elements[top] and decrements top.

```cpp
    T pop() {
        if (top == -1) {
            // Stack is empty, handle the underflow
            return T();
        }
        return elements[top--];
    }
};

```
Step 2: Use the Stack class with specific types in the main function:

* Create an intStack object of type `Stack<int> `with a capacity of 10. We then push the integers 5 and 10 onto the stack using the push method. Next, we pop an element from the stack using 
  the pop method and store it in the variable poppedInt.
*  Create a doubleStack object of type `Stack<double>` with a capacity of 5. We push the doubles 3.14 and 2.71 onto the stack and pop an element, storing it in the variable poppedDouble.

> Note that the compiler generates separate classes for each instantiation of the Stack template, ensuring type safety and efficient code generation.

```cpp
int main() {
    Stack<int> intStack(10);  // Stack of integers
    intStack.push(5);
    intStack.push(10);
    int poppedInt = intStack.pop();

    Stack<double> doubleStack(5);  // Stack of doubles
    doubleStack.push(3.14);
    doubleStack.push(2.71);
    double poppedDouble = doubleStack.pop();

    return 0;
}
```


## Projects
