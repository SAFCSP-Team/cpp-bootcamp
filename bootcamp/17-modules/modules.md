# Modules
In oder to separte the program into multiple files, we need to use modules. By using modules we can split the program into multiple files and use them in the main file.

> There are more than one way to split the code files.

## Concept 
Modules are feature introducted in the C++20 standard tht allow you to organize and reuse code in a way that is cleaner, more efficient, and more scalable than what was possible with header files and the preprocessor.

By using modules we can import cpp files without creating header files.

## Examplee
In this example we will demonstrate how to use modules in C++.

1. Create a file called `greeting.cpp` and add the following code:
**code**
```cpp
// greeting.cpp
export module greeting; // module declaration
 
import <iostream>;        // import declaration
 
export void hello()       // export declaration
{
    std::cout << "Hello world!\n";
}

```

2. Create a file called `main.cpp` which call the function `hello()` from the module `greeting`:
**code**
```cpp
// main.cpp
// main.cpp
import greeting; // import declaration
 
int main()
{
    hello();
}
```

> By writing export we make the function `hello()` visible to other modules. 

## Projects