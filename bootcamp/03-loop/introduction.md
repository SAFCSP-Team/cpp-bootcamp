# Introduction
In many scenarios, you may encounter situations where you need to execute a specific block of code multiple times. This repetitive execution can be achieved using loops. In general, when statements are executed sequentially, each statement is followed by the next one linearly.

For example: Suppose we want to print “Hello World!” 5 times. This can be done in the following code:
```c++
#include <iostream>
int main(){
 std::cout << "Hello world!";
 std::cout << "Hello world!";
 std::cout << "Hello world!";
 std::cout << "Hello world!";
 std::cout << "Hello world!";
 return 0;
}
```
We have to write cout statement manually 5 times. Now imagine you have to write it 100 times, it would be really hectic to re-write the same statement again and again, and it would surely take more time to write it. So, rather than we can use loops to repeat the same statement

## Concept
`Loops` Loops are control structures that allow you to execute a block of code repeatedly until a certain condition is met.

#### C++ offers three main types of loops:

1. `for` Loop:
Is commonly used when you know the **number of iterations in advance** or when iterating over a range. It consists of three parts: **initialization, condition, and increment/decrement**. 

```c++
for (initialization; condition; increment/decrement) {
    // Code block to be executed repeatedly
}
```

The initialization part initializes the loop control variable, the condition is checked before each iteration, and the increment/decrement statement is executed after each iteration.

2. `while` Loop:
Is used when the **number of iterations is not known beforehand** and **depends on a certain condition**. It repeatedly executes the code block as long as the condition is true. 

```c++
while (condition) {
    // Code block to be executed repeatedly
    // increment/decrement statement
    // Condition must eventually become false to exit the loop
}
```

The condition is **checked before each iteration**, and if it evaluates to true, the code block is executed. If the condition is false initially, the code block is never executed.

3. `do-while` Loop:
Is similar to the `while` loop, but it guarantees that the **code block is executed at least once**, even if the condition is initially false. 

```c++
do {
    // Code block to be executed repeatedly
    // increment/decrement statement
} while (condition);
```

The code block is executed first, and then the condition is checked. If the condition is true, the loop continues; otherwise, it exits.

## Examples
print “Hello World!” 5 times using types of loop.

1. For Loop:
```c++
#include <iostream>
int main() {
    for (int i = 0; i < 5; ++i) {
         std::cout << "Hello world!" << endl;
    }
    
    return 0;
}
```

2. while Loop:
   
```c++
#include <iostream>
int main() {
    int count = 0;
    while (count < 5) {
        std::cout << "Hello world!" << endl;
        count++;
    }
    return 0;
}
```

3. Do-While Loop:

```c++
#include <iostream>
int main() {
    int count = 0;
    
    do {
        std::cout << "Hello world!" << endl;
        count++;
    } while (count < 5);
    
    return 0;
}
```


## Projects
