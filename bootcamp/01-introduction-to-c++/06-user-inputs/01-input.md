# Input
Taking an input from users is a crucial concept to cover, if we do not get any dynamic inputs from users our programs will always run the same way. For example, if we built a calculator that sums 2 and 3 it will always give us 5, and we will have to build a calculator for every possible combination of numbers. Hence, taking the values of first and second numbers from the user to sum will save us from wasting our time and effort.

## Concept
Taking an input from users is relatively similar to the way we display an output in C++. 
By using `cin` object we can tell the program that we want a specific value from the user. 

For example,
```cpp
#include <iostream>

using namespace std;

int main() {
  int num;
  cout << "insert a number: ";
  cin >> num;
  cout << "your number is: " << num << endl;
  return 0;
}
```
output,
```
insert a number: 5
your number is: 5
```
As you can see from above example, by using `cin` we asked for an `int` value from the user. 
> The >> symbol is called extraction operator

### Input Type Check
One thing to note, is that when an unexpected value is entered it will lead to an unexpected behavior. Let us look at our example above, if we sent a string rather than integer we will get the following output.

```
insert a number: hello
your number is: 0
``` 
Since we requested an integer but got a string instead the value was not predicted correctly and no exception occurred. Therefore, to handle type checking we can use `cin.good()`method which will return a boolean value indicating if an issue occurred or not (if true is returned then no issue occurred, if false then their was an issue in the input).

```cpp
#include <iostream>
using namespace std;

int main() {
  int num;
  cout << "insert a number: ";
  cin >> num;
  cout << "your number is: " << num << endl;
  cout << cin.good() << endl; //if good returns true the value 1 will be printed. If false then value of 0 will be printed.
  return 0;
}
```
Correct value type output,
```
insert a number: 2
your number is: 2
1
```
Wrong value type output,
```
insert a number: hello
your number is: 0
0
```
> We can also use `cin.fail()` method to check if an issue occurred while taking a user input
## Example

```cpp
#include <iostream>
using namespace std;

int main() {
  string firstName;
  int age;
  double weight;
  cout << "What is your first name? ";
  cin >> firstName;
  cout << "How old are you? ";
  cin >> age;
  cout << "What is your weight (kg)? ";
  cin >> weight;
  cout << "Hello " << firstName << endl;
  cout << "You are " << age << " years old" << endl;
  cout << "Your weight is " << weight << " kg" << endl;
  
  return 0;
}
```
```
What is your first name? turkey
How old are you? 3
What is your weight (kg)? 14.5
Hello turkey
You are 3 years old
Your weight is 14.5 kg
```

## Projects

| Project Title | Deadline |
|:-----------:|:-------------:|
| [User Inputs in C++](https://github.com/SAFCSP-Team/user-inputs-in-cpp) | - | 
