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
We have to write cout statement manually 5 times. Now imagine you have to write it 100 times, it would be hectic to re-write the same statement again and again, and it would surely take more time to write it. So, rather than we can use `loops` to repeat the same statement

## Concept
`Loops` are **control structures** that allow you to **execute a block of code repeatedly** until a certain condition is met.

#### The key components of the loop in C++ :
1. Initialization:

Before entering the loop, you need to **initialize a counter variable** to a specific value. This is typically done before the loop starts.

2. Condition:

- The loop continues executing as long as a specific condition remains true.
- The condition is **checked in each iteration** to determine if the loop should continue or terminate.

3. increment/decrement statement:

After each iteration of the loop, **the counter variable is incremented or decremented** to ensure progress towards the termination of the loop. 

You can use both `prefix` and `postfix` increment/decrement operators within a loop. The choice between them **depends on whether you want to update the variable before or after its usage** in the loop. 
```
1. Prefix Increment/Decrement :
         The value of the variable is incremented or decremented **before it is used** in the expression.

2. Postfix Increment/Decrement :
         The value of the variable is incremented or decremented **after it is used** in the expression.
```
4. Loop Body:

It defines the **actions or operations** that need to be performed during each iteration.




## Types of loops:

##### For loop:
 
```c++
for (initialization; condition; increment/decrement) {
    // Code block to be executed repeatedly
}
```

##### While loop:

```c++
while (condition) {
    // Code block to be executed repeatedly
    // increment/decrement statement
}
```

##### Do-while loop:
```c++
do {
    // Code block to be executed repeatedly
    // increment/decrement statement
} while (condition);
```

## Examples
Print “Hello World!” 5 times using types of loop.

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
