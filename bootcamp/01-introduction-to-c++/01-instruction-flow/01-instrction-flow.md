# Instruction Flow
All programs are consistent, they follow the same pattern. Each program is a set of instructions that executes in a specific manner. And here in this section we will cover how instructions are listed and executed in programs to help us understand instruction flow in `C++` language.


## Concept 
A program is usually described as a set of instructions, these instructions are executed sequentially to perform a task. 

For example, a program summing two numbers will follow this pattern of instruction. 

1. Initialize the first number `num1`.
2. Initialize the second number `num2`.
3. Sum `num1` and `num2`.

The above is the list of instructions that a summing program needs, and they get executed one line after another.

We can manipulate the flow that instructions follow by using what's called **control flow** statements that programming language provides to us, such as for loop and if condition statements. 

In `C++`, instructions are executed sequentially one after another unless there is a control flow statement that will jump some instructions or repeat others.


## Example

In the following example, we will analyze the output of a simple `Hello world` printer program.

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
As you can see, two instructions have been given for the program. 

1. Print `Hello`.
2. Print `world`.

And because the program executes the instructions sequentially, `Hello` was printed first.

Here is another example of converting our summing program instructions into a program in `C++`. 

**code**

```c++
#include <iostream>


int main() {
  int num1 = 3;
  int num2 = 2;
  std::cout << num1 + num2; // print the sum result
}

```
> You can remove the usage of **std::** if you import the namespace std in your file.

**output**

```
5
```

