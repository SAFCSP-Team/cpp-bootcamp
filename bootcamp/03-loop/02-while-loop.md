# While loop
## Concept
Is used when the **number of iterations is not known beforehand** and **depends on a certain condition**. It repeatedly executes the code block as long as the condition is true. 

```c++
initialization;
while (condition) {
    // Code block to be executed repeatedly
    // increment/decrement statement
}
```
The condition is **checked before each iteration**, and if it evaluates to true, the code block is executed. If the condition is false initially, the code block is never executed.

Here's an example that demonstrates the usage of a while loop:
```c++
#include <iostream>
int main() {
    int i = 0;
    while (i < 5) { 
        std::cout << i << " "; 
        i++;
    }
    return 0;
}
```
```
0 1 2 3 4
```

In this example:

- Initialization: **int i = 0;** initializes the loop control variable `i` to 0.
- Condition: **i < 5** specifies the condition that must be true for the loop to continue executing. **The loop will continue as long as `i` is less than 5.**
- Loop body: **std::cout << i << " ";** prints the value of `i` followed by a space.
- Update: **i++;** increments the value of `i` by 1 in each iteration of the loop.

## Example 
Example 1: Using postfix increment and break statement:
```c++
#include <iostream>
int main() {
    int i = 0;
    while (i < 5) {
        std::cout << i << " ";
        i++;
        if (i == 2) {
            break;
        }
    }
    return 0;
}
```
```
0 1
```

Example 2: Using prefix decrement and continue statement:
```c++
#include <iostream>
int main() {
    int i = 5;
    while (i > 0) {
        --i;
        if (i == 2) {
            continue;
        }
        std::cout << i << " ";
    }
    return 0;
}
```
```
4 3 1 0
```
## Project 

