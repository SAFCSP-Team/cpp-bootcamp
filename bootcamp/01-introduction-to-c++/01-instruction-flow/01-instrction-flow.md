# Instruction Flow
All programs are consistent, they follow the same pattern. Each program is a set of instructions that executes in a specific manner. And here in this section we will cover how instructions are listed and executed in programs to help us understand instruction flow in `C++` language.


## Concept 
A program is usually described as a set of instructions, these instructions are executed sequentially to perform a task. 

For example, a program summing two numbers will follow this pattern of instruction. 

```
1. initialize the first number `num1`.
2. initialize the second number `num2`.
3. sum `num1` and `num2`.
```

The above is a list of instructions of a summing program. These instructions get executed one line after another until the program complete.

> We can manipulate the flow that instructions follow by skipping or repeating some instructions.

### Statements and Instructions

Although we have our instructions that we need to build a summing program, we can not just give it to a computer and expected it to be executed. Computers are not that inelegant to understand simple english, that is why we as programers exists; To translate these instructions into `statements` using programming languages such as `Java` and `C++` so computers can handle, understand,  and execute. 


### C++ Instruction Flow

In `C++`, same as other languages, instructions are executed sequentially one after another unless there is a control flow statement that will jump some instructions or repeat others.

### Conclusion 

Program's statements are written in a specific syntax for computers to handle and understands, and they are executed sequentially unless we manipulate the flow.

Therefore, in this bootcamp we will cover C++ syntax to write complete and correct statements, and control flow statements that will helps us control the execution of a program.


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