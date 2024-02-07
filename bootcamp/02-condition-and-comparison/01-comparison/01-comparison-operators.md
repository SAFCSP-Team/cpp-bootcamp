# Comparison Operators
In programming languages, we have several types of operators, for example, arithmetic operators are +, -, *, etc. Comparison or relational operators (>, <, ==, !=, >=, <=), Assignment operator (=) and more.
> For more operators information in c++ read [cplusplus.com](https://cplusplus.com/doc/tutorial/operators/)


## Concept
Comparison operators are used to compare two expressions or values and return either `true` or `false` which determine if the comparison was correct or not. For example, comparing the value of **20** and **5** by saying "is 20 greater than 5?" will result in true. so the following code will print 1 which is the value of true.

```cpp
#include <iostream>
using namespace std;

int main() {
  bool result = 20 > 5; // check if 20 is greater than 5 and return true if yes. Otherwise, return false.
  cout << result;
  
  return 0;
}
```
output,
```
1
```

Each operator has its own meaning.

|operator|	description| example |
|:--------:|-------------|--|
|==	|equal to| `10 == 12` |
|!=	|not equal to| `10 != 12` |
|<	|less than| `10 < 12`|
|>	|greater than| `10 > 12` |
|<=	|less than or equal to| `10 <=  12`|
|>=	|greater than or equal to| `10 >= 12` |

> Logical operators (&&, ||, !) can be used with comparison operators.
[udacity.com](https://www.udacity.com/blog/2021/06/understanding-c-logical-operators.html)
## Examples

- Check if 7 is greater than or equal to 7.
```cpp
#include <iostream>
using namespace std;

int main() {
  int a = 7;
  int b = 7;
  bool result = a <= b;
  cout << result;
  
  return 0;
}
```
```
1
```

- Check if 7 is greater than (3+4).
```cpp
#include <iostream>
using namespace std;

int main() {
  int a = 7;
  int b = 3 + 4;
  bool result = a > b;
  cout << result;
  
  return 0;
}
```
```
0
```
- Check if the character value of variable `a` is the same as the value of variable `b`.

```cpp
#include <iostream>
using namespace std;

int main() {
  char a = 'a';
  char b = 'a';
  bool result = a == b;
  cout << result;
  
  return 0;
}
```

```
1
```


## Projects

| Project Title | Deadline |
|:-----------:|:-------------:|
| [Comparison in C++](https://github.com/SAFCSP-Team/comparison-in-cpp) | - | 
