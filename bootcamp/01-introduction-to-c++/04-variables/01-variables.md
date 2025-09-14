# Variables

## Concept
`Variable` is a container that stores a value temporarily. It helps us refer to this value later on by a given name and manipulate it during the lifetime of a program.
Each variable in C++ can be declared using the following structure.
```cpp
varType varName = varValue;
```
For example, we can store a value of 10 in a variable called `number`.
```cpp
int number = 10;
```
Each variable might be given a type, which determines the value that will be stored in it. In the example above, we gave the variable a type of `int`, which stores integers only. 
If we try to store a value of a string `"text"` in the number variable, we will get an error since the value does not fit the type.

```cpp
int number = "text"; //error
```
Instead, we must use the type `string` to store a text.
```cpp
string text = "text"; //correct
```
### Identifiers / Variable Names
An identifier is the name of your variable, and to create a variable, you have to follow certain conditions.
1. Variable names can contain letters, digits, and underscores.
2. Variable names must start with a letter or an underscore.
3. Since C++ is case sensitive, variable names are also case sensitive, which means `num` is not the same as `Num`.
4. Variable names can not contain whitespace or special characters like %, #, !, ?, etc.
5. A variable name can not be a reserved word, such as `class` or `namespace`.

### Data Types
Here are the most used data types in C++ and the values they accept. 
| Data Type | Value | Example|
|-----------|-------| -------|
| int | stores integer values, which are whole numbers | `int i = 2;`|
| float, double | stores floating point numbers | `float f = 2.4;`, `double d = 74.51428;` |
| char | stores a single character | `char c = 'a';` |
| string | stores a text | `string s = "hello";` |
| boolean | stores either `true` or `false` | `bool b = true;`|


## Example

- A string variable called `greeting`.
```cpp 
#include <iostream>
using namespace std;

int main() {
  string greeting;
  greeting = "Hello Team!";
  cout << greeting;
  
  return 0;
}

```

output,
```
Hello Team!
```


- An integer variable called `num`.
```cpp 
#include <iostream>
using namespace std;

int main() {
  int num = 3;
  cout << num*2;
  
  return 0;
}
```

output,
```
6
```

## Projects
- [Variables in C++ ](https://github.com/SAFCSP-Team/variables-in-cpp)
