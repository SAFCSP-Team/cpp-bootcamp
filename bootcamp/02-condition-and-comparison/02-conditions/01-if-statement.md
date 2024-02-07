# If Statement
If the statement is used to control the flow of our program by checking if a condition is correct or not.

## Concept
If the statement is used to make a decision to execute a block of code based on a condition.
The syntax of writing an if statement in C++ is as follows. 
```
if(condition){
    //code to be executed if the condition is true.
}
```
The condition eventually should return a boolean value. You can use `bool` data type in the condition or an expression that will return a `true` or `false` value.
To demonstrate the idea, look at the examples below.

*Display a message to indicate if a `number` is greater than 10.*
```cpp
#include <iostream>
using namespace std;

int main() {
  int number = 12; 
  if(number > 10){
  	cout << "number is greater than 10 ";
  }
  
  return 0;
}
```

output,

```
number is greater than 10 
```

*Check if the two names are equal or not.*

```cpp
#include <iostream>
using namespace std;

int main() {
  string name = "ahmed"; 
  if(name !=  "sara"){
  	cout << name << " is not equal to sara" ;
  }
  
  return 0;
}
```

output,

```
ahmed is not equal to sara
```

*If a boolean variable `isTrue` is true, execute a print statement*

```cpp
#include <iostream>
using namespace std;

int main() {
  bool isTrue = false;
  if(isTrue){
  	cout << "Hi!" ;
  }
  
  return 0;
}
```
No output will be printed since the boolean value is false. Therefore, the condition is always false and the statements inside the if block will never be executed.

## Examples

- If the user age is 18 or above, then he is an adult.
```cpp
#include <iostream>
using namespace std;

int main() {
  int age = 20; 
  if(age >= 18){
  	cout << "you are an adult";
  }
  
  return 0;
}
```

output,
```
you are an adult
```

- If a user is an adult and passed his driving test, then he can have a driving license.

```cpp
#include <iostream>
using namespace std;

int main() {
  bool isAdult = true;  // is the user an adult?
  bool isPassed = true; //did the user pass the driving test?
  if(isAdult && isPassed ){
  	cout << "Great, you can have your driving license now!" ;
  }
  
  return 0;
}
```

output,

```
Great, you can have your driving license now!
```

## Projects

| Project Title | Deadline |
|:-----------:|:-------------:|
| [If Statement in C++](https://github.com/SAFCSP-Team/if-statement-in-cpp) | - | 
