# Do-while loop
## Concept
Do-while is similar to the `while` loop, but it guarantees that the **code block is executed at least once**. The code block is executed first, and then the condition is checked. If the condition is true, the loop continues. Otherwise, it exists.

```c++
initialization;
do {
    // Code block to be executed repeatedly
    // increment/decrement statement
} while (condition);
```

Here's an example that demonstrates the structure of a `do-while` loop

```c++
#include <iostream>
int main() {
   int i = 0;
   do {
      std::cout << i << " ";
      i++;
   } while (i < 0);
 return 0;
}
```
```
0
```
In this example:

- Initialization: `int i = 0` initializes the loop control variable `i` to 0.
- Loop body: `std::cout << i << " ";`  prints the value of `i` followed by a space.
- Update: `i++` increments the value of `i` by 1.
- Condition: `i < 0` is checked after the first iteration. If the condition is true, the loop body is executed again, and the process repeats. If the condition is false, the loop terminates.

> Note that the `do-while` loop guarantees at least one execution of the loop body, regardless of the initial condition. 
<br> **The code prints 0 before checking the condition.**

## Examples  
- Do-while loop with postfix decrement and break statement.
```c++
#include <iostream>
int main() {
    int i = 5;
    do {
        std::cout << i << " ";
        i--;
        if (i == 2) {
            break;
        }
    } while (i > 0);

    return 0;
}
```
```
5 4 3
```
- Do-while loop with prefix increment and continue statement.

```c++

#include <iostream>
int main() {
    int i = 0;
    do {
        ++i;
        if (i == 2) {
            continue;
        }
        std::cout << i << " ";
    } while (i < 5);

    return 0;
}
```
```
1 3 4 5
```
## Project 
- [Do-while loop](https://github.com/SAFCSP-Team/do-while-loop)
