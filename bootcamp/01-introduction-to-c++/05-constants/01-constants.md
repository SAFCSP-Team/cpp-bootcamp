# Constants

## Concept
Constants are same as variables, they hold a value but this value can not be changed once its initialized. They can be declared using the keyword `const`.
> Constants are read-only variables.

```cpp
const varType varName = varValue;
```
For example,
```cpp
const int num = 7;
```

## Example

```cpp
#include <iostream>

using namespace std;

int main() {
  const int num = 7; //initialize num constant with the value of 7.
  cout << num*2; //print the value multiplied by 2.
  
  return 0;
}
```
Above, we initialized a constant, and printed its value multiplied by 2. It worked since we only read the constant value and we did not try to change it. If we try to change a constant value we will get an error.

```cpp
#include <iostream>

using namespace std;

int main() {
  const int num = 7;
  num = 3; //error: assignment of read-only variable ‘num’
  
  return 0;
}
```

## Projects

| Project Title | Deadline |
|:-----------:|:-------------:|
| [Constants in C++](https://github.com/SAFCSP-Team/constants-in-cpp) | - | 
