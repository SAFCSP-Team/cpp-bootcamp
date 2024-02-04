# Functions

## Concept

`functions` are **blocks of code** that perform a specific task and can be reused throughout a program.

Here's the basic syntax for defining and using functions:

```c++
returnType functionName(parameterType parameterName)
{

    //  Function body: code to be executed
}

int main() {
    functionName(argument);  // Function call
    return 0;
}
```

Let's break down the different parts:

- Function declaration:
  - `returnType` specifies the **data type of the value** that the function **will return** (e.g., int, float, void for no return value).
  - `functionName` is the **name of the function**.
  - `parameterType` specifies the **data type** of the function's **parameter** (if any).
  - `parameterName` is the **name** of the function's **parameter** (if any).

- Function body:
  - The function body contains the **code that is executed** when the function is called.
  - Optionally, a function may include a `return` statement to return a value to the caller.

- Main function:
  - `int main()` is a special function that **must be present in every C++ program**.
  - It serves as the s**tarting point of program execution** and can call other functions.
  
Here's an examples that demonstrates the usage of a function:
#### Example 1:
```c++
#include <iostream>
void print() {
    std::cout << "Hello world!" << std::endl;
}

int main() {
    print(); // Function call
    return 0;
}

```
In this example:

 Function declaration:
   - returnType: void, which means it doesn't return any value. 
   - functionName:  print().
   - parameterType: The function does not have parameters. 
   - parameterName: The function does not have parameters. 

Function body: 
   - print **Hello World** statement.

#### Example 2:
```c++
int addNumbers(int a, int b) {
    return a + b;
}

int main() {
    int result = addNumbers(3, 5);
    std::cout << "The result is: " << result << std::endl;
    return 0;
}

```
In this example:

 Function declaration:
  - returnType: int, which means the function returns an integer value.
  - functionName:  addNumbers().
  - parameterType: two integer values.
  - parameterName:  a, b.

Function body:
 - add two numbers and return the result.
  

The **order in which functions are defined**, whether before or after the `main` function, **does not affect the program's functionality**. But when a function is defined after the main function, you must provide a function declaration (prototype) before the main function to inform the compiler about the function's existence.

```c++
// Function declaration and definition

int main() {
    // Function call
    return 0;
}

```
```C++
// Function declaration (prototype)

int main() {
    // Function call
    return 0;
}

// Function definition (implementation)

```
The **functions define their own scope**, and **variables declared within a function** have local scope o**nly accessible within the function** where they are declared. 

The `scope of a variable` determines w**here it can be accessed and used within a program**, and there are two main types of variable scope `local` and `global`.
### Types of variable scope.

1. Local Variables:
   - Local variables are **declared within a specific block**, such as a function or a code block enclosed in curly braces `{}`.
   - They are only **accessible within the block they are declared in.**
   - Once the execution of the **block is complete, local variables are destroyed**, and their memory is freed.

 > Local variables can have the same name as variables in other blocks without causing conflicts because each block has its own scope.

2. Global Variables:
   - Global variables are **declared outside of any specific block**, typically at the beginning of a program.
   - They are **accessible and modified from any program part**, including all functions and code blocks.

> It's important to note that local variables take precedence over global variables if they share the same name within a particular scope.

<br>

### Function overloading
This means that you can have **multiple functions with the same name**, but **each function has unique parameter** types and/or numbers. 

> The return type of the function does not determine function overloading.

If you have two functions with the same name and the same parameter types and numbers but with different return type, the compiler will throw an error, as it cannot distinguish between them.
```C++
void test(int a) {
    std::cout << "the test number: " << a << std::endl;
}
int test(int a) {
   return a;
}
```
**Overloading is solely based on the parameters** of the functions. The compiler determines which function to call based on the number, types, and order of the arguments passed to the function.
```C++
#include <iostream>

// Function with one integer parameter
void printNumber(int num) {
    std::cout << "Integer number: " << num << std::endl;
}

// Function with one double parameter
void printNumber(double num) {
    std::cout << "Double number: " << num << std::endl;
}

// Function with two integer parameters
void printNumber(int num1, int num2) {
    std::cout << "Sum of two numbers: " << num1 + num2 << std::endl;
}

// Function with two double parameters
int printNumber(double num1, double num2) {
    return num1 * num2;
}

int main() {
    printNumber(10);            // Calls the function printNumber(int)
    printNumber(3.14);          // Calls the function printNumber(double)
    printNumber(4, 5);          // Calls the function printNumber(int, int)
    std::cout << " Multiply of two numbers: " << printNumber(4.0, 5.0) << std::endl; // Calls the function printNumber(double, double)

    return 0;
}
```
As you can see, each function is called based on the argument types that match the function's parameter. Notice that the return types of all these functions are not the same. Overloaded functions may or may not have different return types but they must have different arguments. 

## Example

- `multiplyValues` function that multiplies two global integer values and then prints the result.
```C++
#include <iostream>

// Global variables
int fristValue = 10;
int secondValue = 20;

void multiplyValues() {
    int result = fristValue * secondValue;
    std::cout << "The result of multiply is: " << result << std::endl;
}

int main() {
    multiplyValues();
    return 0;
}
```

- `factorial` The function takes an integer as a parameter and returns an integer value to the main function. 

```c++
#include <iostream>

int factorial(int n);

int main() {
    int number;
    std::cout << "Enter a positive integer: ";
    std::cin >> number;

    int result = factorial(number);
    std::cout << "The factorial of " << number << " is: " << result << std::endl;

    return 0;
}

int factorial(int n) {
    int result = 1;

    for (int i = 1; i <= n; ++i) {
        result *= i;
    }

    return result;
}
```

## Project 
| Project Title | Deadline |
|:-----------:|:-------------:|
| [Functions](https://github.com/SAFCSP-Team/functions) | - | 
