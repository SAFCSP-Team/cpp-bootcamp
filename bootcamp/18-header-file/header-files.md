# Header Files
To organize code, we can split the program into multiple files, to achive that we neeed to use **header files**. 

## Concept
In order to use function or class from another file, we need to use header files.

When using a function or class from other files, the file which we want to use the function or class from, needs to have a declaration of what the file contains. This is declaration file is called **header file**. 

**Build process**
1. Preprocessor: 
    - The preprocessor will replace the `#include` directive with the content of the header file.
2. Compiler:
    - The compiler will compile the code.
3. Linker:
    - The linker will link the object files together.

## Example
In this example we will demonstrate how to use header files in C++.

1. Create a file called second.cpp and add the following code:
```cpp
// second.cpp
#include "second.h"

int Second::add(int a, int b) {
    return a + b;
}

double Second::multiply(double a, double b) {
    return a * b;
}

```

2. Create a header file with the same name as the previous file, but with the extension `.h` and add the following code:
```cpp
// second.h
#ifndef SECOND_H
#define SECOND_H

class Second {
    public:
    int add(int a, int b);
    double multiply(double a, double b);

};

#endif
```

3. Finally we need to call the functions from the header file in the main file:
```cpp
// main.cpp
#include <iostream>
#include "second.h"

int main() {
    Second second;
    std::cout << second.add(1, 2) << std::endl;
    std::cout << second.multiply(1.5, 2.5) << std::endl;
}
```

## Projects
- [Header Files](https://github.com/SAFCSP-Team/header-file-project)
