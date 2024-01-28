# String Input

## Concept
Handling a string input is bit different from numbers, let us look at this example.
```cpp
#include <iostream>
using namespace std;

int main() {
  string fullName;
  cout << "What is your full name? ";
  cin >> fullName;
  cout << "Your full name is: " << fullName << endl;

  return 0;
}
```
output,
```
What is your full name? Alex childs
Your full name is: Alex
```
As you have noticed, in the output only first name was taken and the last name was ignored. This happened because when `cin` read a string input it will store each word in a string variable (words are separated by a whitespace character). To demonstrate the idea let us look at the following example.
```cpp
#include <iostream>
using namespace std;

int main() {
  string firstName;
  string lastName;
  cout << "What is your first and last name? ";
  cin >> firstName; //store the first word encountered in firstName
  cin >> lastName; //store the second word in lastName.
  cout << "Your full name is: " << firstName << " " << lastName << endl;

  return 0;
}
```
output,
```
What is your first and last name? alex childs
Your full name is: alex childs
```

Sometimes, we want to store the entire line that was inserted by the user. To do so we can use `getline()` method as the following. 

```cpp
#include <iostream>
using namespace std;

int main() {
  string fullName;
  cout << "What is your full name? ";
  getline(cin, fullName);
  cout << "Your full name is: " << fullName << endl;

  return 0;
}
```
output,
```
What is your full name? alex childs
Your full name is: alex childs
```
`getline()` takes two arguments. First argument identify where are we getting the input from `cin`. Second, what variable should we store the input in `fullName`.

## Example

```cpp
#include <iostream>
using namespace std;

int main() {
  string fullName;
  int age;
  cout << "what is your full name? ";
  getline(cin,fullName);
  cout << "how old are you? ";
  cin >> age;
  cout << "Hello " << fullName << endl;
  return 0;
}
```
```
what is your full name? Alex childs
how old are you? 32
Hello Alex childs
```

## Projects

| Project Title | Deadline |
|:-----------:|:-------------:|
| [String Inputs in C++](https://github.com/SAFCSP-Team/string-inputs-in-cpp) | - | 
