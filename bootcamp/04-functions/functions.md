

functions are blocks of code that perform a specific task and can be reused throughout a program. They provide a way to modularize code and make it more organized and manageable. 


Here's the basic syntax for defining and using functions:

```cpp
returnType functionName(parameterType parameterName) {

    // Code to be executed
    // Optional return statement
}

int main() {
    functionName(argument);  // Function call
    return 0;
}
```

Let's break down the different parts:

- Function Declaration:
  - `returnType` specifies the data type of the value that the function will return (e.g., `int`, `float`, `void` for no return value).
  - `functionName` is the name of the function.
  - `parameterType` specifies the data type of the function's parameter (if any).
  - `parameterName` is the name of the function's parameter (if any).

- Function Body:
  - The function body contains the code that is executed when the function is called.
  - It can include variable declarations, statements, loops, conditionals, and other function calls.
  - Optionally, a function may include a `return` statement to return a value back to the caller.

- Main Function:
  - `int main()` is the entry point of a C++ program.
  - It is a special function that must be present in every C++ program.
  - It serves as the starting point of program execution and can call other functions.

To define a function in C++, you typically place its declaration before the `main` function. The actual function definition (implementation) can be placed before or after the `main` function.





### The two main types of variable scope are local and global.

1. Local Variables:
   - Local variables are declared within a specific block, such as a function or a code block enclosed in curly braces `{}`.
   - They are only accessible within the block they are declared in.
   - Local variables are typically used for temporary storage or for storing data that is relevant only within a specific block of code.
   - Once the execution of the block is complete, local variables are destroyed, and their memory is freed.
   - Local variables can have the same name as variables in other blocks without causing conflicts because each block has its own scope.

2. Global Variables:
   - Global variables are declared outside of any specific block, typically at the beginning of a program.
   - They are accessible from any part of the program, including all functions and code blocks.
   - Global variables have a global scope, meaning they can be accessed from anywhere within the program.
   - Global variables are useful for storing data that needs to be accessed and modified by multiple functions or code blocks.
   - However, using too many global variables can make the program more difficult to understand and maintain.

> It's important to note that local variables take precedence over global variables if they share the same name within a particular scope.
