# Print Statement
When developing a program, we mostly need to represent the output of the program as text to the users, such as printing the sum of two numbers on the screen. To do so, we can use a print statement.


## Concept
`Print Statement` is a way of printing text on an output device such as the screen console.

To print a text in `C++`, we can use the `cout` object as follows.

```c++
#include <iostream>

int main() {
  std::cout << "hello from c++";
  return 0;
}
```
Let us take the code one line after another to understand the `C++` structure and the print statement.
- `#include <iostream>` this line of code is used to tell the program that we want to use the `iostream` library, which helps us read and write text from and to the console.
- `main` is a function that every `C++` program must have, it is considered the entry point of running a program.
- `int` is the return type of the `main` function. If the `main` returns **0**, it indicates the program **terminated successfully**. Otherwise, if the return value is **non-zero**, that means an **error occurred**.
- `std::cout` is calling the `cout` object from the `std` namespace, which is a logical collection of elements(ex, objects and methods).
- `std::cout << "hello from c++";` is calling cout and sending it a text to be printed. `cout` represents the output stream which our text will be sent to, and by default it is the screen console. Therefore, this line of code means sending a text to be printed on the screen console.
- `<<` is called **stream insertion operator** which means insert a text into the stream.
- `return 0;` means terminate the program with exit code 0, which means no error occurred.

The output of the above code is,

```
hello from c++
```
> Any line that starts with # is called a preprocessor directive.


Printing on the screen console could be done by printing a single line or multiple lines of text, and here in this section, we will cover both. 


### Print Single Line
To print a single line of text, we can have single or multiple print statements as the following. 

```c++
#include <iostream>

int main() {
  std::cout << "Hello Team";
  return 0;
}
```

```c++
#include <iostream>

int main() {
  std::cout << "Hello " << "Team";
  return 0;
}
```
> Using multiple insertion operators means inserting the first text into the stream and then the second, and so on...

```c++
#include <iostream>

int main() {
  std::cout << "Hello ";
  std::cout << "Team";
  return 0;
}
```

All examples above will have the same output which is,

```
Hello Team
```
> As you might have noticed, having multiple print statements does not mean we will have multiple lines of text on the screen console.

### Print Multiple Lines
Sometimes we might need to print multiple lines of text. Therefore, we need a way to tell the program to print each line of text individually. To do so we can use escape characters such as `\n` or `std::endl` function as the following.

```c++
#include <iostream>

int main() {
  std::cout << "Hello \n";
  std::cout << "Team";
  return 0;
}
```

```c++
#include <iostream>

int main() {
  std::cout << "Hello " << "\n";
  std::cout << "Team";
  return 0;
}
```

```c++
#include <iostream>

int main() {
  std::cout << "Hello " << std::endl;
  std::cout << "Team";
  return 0;
}
```

All multiple lines examples above will produce the following output.

```
Hello 
Team
```

> [Escape characters](https://en.cppreference.com/w/cpp/language/escape) are some special sequences we can use to represent a certain character in strings and characters.

## Examples
- Print "I am learning C++" in a single line.
```c++
#include <iostream>

int main() {
  std::cout << "I am learning C++";
  return 0;
}
```
Output
```
I am learning C++
```

- Print "I am learning C++" in multiple lines.
```c++
#include <iostream>

int main() {
  std::cout << "I am learning\n";
  std::cout << "C++";
  return 0;
}
```
Output
```
I am learning
C++
```

## Projects
- [Print Statement](https://github.com/SAFCSP-Team/print-project/) 
