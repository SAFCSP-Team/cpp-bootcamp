# Header Files
To organize code, we can split the program into multiple files, to achive that we neeed to use **header files**. 

## Concept
To use exterinal code in C++, we do several steps, the exterinal c++ file that we want to use in main file should have a file called **header file**. 

A header file is used to declare the functions and classes that we want to use in the main file. 

The header file has the extension `.h` and contains the declaration of the functions and classes. The main file includes the header file using the `#include` directive.

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
4. In the terminal, run the following commands:
```bash
g++ -c second.cpp
```
> The `-c` flag is used to compile the file into an object file.

5. To link the object file with the main file and create an executable file called main, run the following command:
```bash
g++ -o main main.cpp second.o
```
> The `-o` flag is used to specify the name of the output file.

6. Finally, run the following command to execute the program:
```bash
./main
```
```
**OUTPUT:**
```
3
3.75
```

## Projects
- [Header Files](https://github.com/SAFCSP-Team/header-file-project)
