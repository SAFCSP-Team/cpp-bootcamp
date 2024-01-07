# Variables

## Concept
**Variable** is a container that stores a value temporarily. It helps us refer to this value later on by a given name and manipulate it during the life-time of a program.
Each variable in C++ can be declared using the following structure.
```cpp
varType varName = varValue;
```
For example, we can store a value of 10 in a variable called `number`.
```cpp
int number = 10;
```
Each variable might be given a type, which determine the value that will be stored in it. In the example above, we gave the variable a type of `int` which stores integers only. 
If we try to store a value of a string `"text"` to the number variable we will get an error since the value does not fit the type.

```cpp
int number = "text"; //error
```
Instead, we must use type `string` to store a text.
```cpp
string text = "text"; //correct
```
### Identifiers / Variable Naming
An identifier is the name of your variable, and to create a variable you have to follow certain conditions.
1. Variable names can contain letters, digits and underscores
2. Variable names must start with a letter or an underscore.
3. Since C++ is case sensitive, variable names are also case sensitive, which means `num` is not the same as `Num`.
Names cannot contain whitespaces or special characters like !, #, %, etc.
A variable name can not be a reserved word such as `class` or `namespace`.

### Data Types
Below, you will see each type in C++ and the values it accepts. 
| Data Type | Value |
|-----------|-------|
| int | stores integer values, which are whole numbers |
| float, double | stores floating point numbers |
| char | stores a single character |
| string | stores a text |
| boolean | stores either `true` or `false` |
### Variable Naming 
to name a variable in `c++` we need to follow a specific rules as follows.
1.
2.
3.


## Example

## Projects