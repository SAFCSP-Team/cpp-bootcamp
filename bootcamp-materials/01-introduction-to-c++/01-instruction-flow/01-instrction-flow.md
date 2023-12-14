# Instruction Flow
All programs are consistent, they follow the same pattern. Each program is a set of instructions that executes in a specific manner. And here in this section we will cover how instructions are listed and executed in programs to help us understand instruction flow in `C++`` language.


## Concept 
A program is usually described as a set of instructions, these instructions are executed sequentially to perform a task. 

For example, a program summing two numbers will follow this pattern of instruction. 
1. initialize the first number `num1`.
2. initialize the second number `num2`.
3. sum `num1` and `num2`.

The above are the list of instructions that a summing program needs, and they get executed one line after another.

We can manipulate the flow that instructions follow by using whats called **control flow** statements that programming language provide to us, such as for loop and if condition statements. 

In `C++`, instructions are executed sequentially one after another unless there is a control flow statement that will jump some instructions or repeat others.


## Example

In the following example we will analyze the output of a simple `Hello world` printer program.

**code** 
```cpp
#include <iostream>

int main() {
  std::cout << "Hello ";
  std::cout << "world ";
}

```

**output** 

```
Hello world 
```
As you can see, tow instructions have been given for the program. 
- Print `Hello`.
- Print `world`. 
And because the program executes the instructions sequentially, `Hello` was printed first.