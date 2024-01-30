# For loop

## Concept
Is commonly used when you know the **number of iterations in advance** or when iterating over a range. It consists of three parts: **initialization, condition, and increment/decrement**. 

```c++
for (initialization; condition; increment/decrement) {
    // Loop body
}
```

Here's an example that demonstrates the usage of a `for` loop:

```c++
#include <iostream>

int main() {
    for (int i = 0; i < 5; i++) {
        std::cout << "Iteration: " << i << std::endl;
    }

    return 0;
}
```
```
Iteration: 0
Iteration: 1
Iteration: 2
Iteration: 3
Iteration: 4
```

In this example:
- The initialization statement **int i = 0** initializes the loop control variable `i` to 0.
- The condition **i < 5** is evaluated before each iteration.
- The update statement **i++** increments the loop control variable `i` by 1 at the end of each iteration.
- The loop body **std::cout << "Iteration: " << i << std::endl;** prints the current iteration number.

The `for` loop executes five times, printing the iteration number from 0 to 4. Once the condition becomes false (`i < 5` is no longer true), the loop terminates.

## Examples  

Example 1: Printing numbers from 1 to 10 without number 3 (Postfix increment).

```c++
#include <iostream>
int main() {
    for (int i = 1; i <= 10; i++) {
         if (i == 3) {
            continue; // Exit the loop when i becomes 3
         }
         std::cout << i << " ";
    }
    return 0;
}
```
```
1 2 4 5 6 7 8 9 10
```

Example 2: Iterating through an array (Prefix increment).
```c++
#include <iostream>
int main() {
    int numbers[] = {1, 2, 3, 4, 5};
    for (int i = 0; i < 5; ++i) {
        std::cout << numbers[i] << " ";
     }
     return 0;
}
```
```
1 2 3 4 5
```
Example 3: Computing the factorial of a number (prefix decrement).
```c++
#include <iostream>

int main() {
    int factorial = 1;

    for (int n = 5; n > 0; --n) {
        factorial *= n;
    }

    std::cout << "Factorial of 5 is: " << factorial << std::endl;

    return 0;
}
```
```
Factorial of 5 is: 120
```

Example 4: Printing numbers in reverse order (postfix decrement).
```c++

#include <iostream>
int main() {
    for (int i = 5; i > 0; i--) {
        std::cout << i << " ";
    }
    return 0;
}
```
```
5 4 3 2 1
```

## Project 

| Project Title | Deadline |
|:-----------:|:-------------:|
| [For Loop](https://github.com/SAFCSP-Team/for-loop) | - | 
