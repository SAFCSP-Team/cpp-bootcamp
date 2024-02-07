# Switch Statement



## Concept
Switch statement is used to compare a value with different cases, if a case is met the statements block of that case will be executed. 

Syntax,
```
switch(expression){
    case first-case: 
        // statements
        break;

    case second-case:
        // statements
        break;

    case third-case:
        // statements
        break;

    default:
    // statements
}
```
Each case will be compared with the value of the *switch expression*, if a case is met the statements block of that case will be executed. Once a *break* is encountered during the execution of statements the execution will stop and the compiler will exit the switch statement.

If no case matches the switch expression then the *default* block will be executed.

Let us look at the following example. 

```cpp
#include <iostream>
using namespace std;

int main() {
  int number = 10; 
  switch(number) {
  case 1:
  	cout << "your number is equal to 1";
    break;
  case 10:
    cout << "your number is equal to 10";
    break;
  default:
    cout << "your number is not equal to 1 or 10";
}
  
  return 0;
}
```

output, 

```
your number is equal to 10
```

Since the number value is equal to 10, the block of case 10 was executed.

let us now check the break concept, we said that the `break` is used to exit the switch statement. Then what would happen if I added a block of code after the break? 
```cpp
#include <iostream>
using namespace std;

int main() {
  int number = 10; 
  switch(number) {
  case 1:
  	cout << "your number is equal to 1";
    break;
  case 10:
    cout << "your number is equal to 10" << endl;
    cout << "Before break" << endl;
    break;
    cout << "After break"<< endl;
  default:
    cout << "your number is not equal to 1 or 10";
}
  
  return 0;
}
```
output,
```
your number is equal to 10
Before break
```
As you can see, only those statements before the break were executed since the compiler read them before exiting the switch statement.
Now let us see what happens if we remove the break from the switch. 

```cpp
#include <iostream>
using namespace std;

int main() {
  int number = 10; 
  switch(number) {
  case 1:
  	cout << "your number is equal to 1";
    break;
  case 10:
    cout << "your number is equal to 10" << endl;
    cout << "Before break" << endl;
    cout << "After break" << endl;
  default:
    cout << "your number is not equal to 1 or 10";
}
  
  return 0;
}
```

output,
```
your number is equal to 10
Before break
After break
your number is not equal to 1 or 10
```
All statements after matching a case get executed until the end of the switch statement since we did not tell the compiler when to exit. We have to be careful when using the switch so we don't fall into this type of issue later on. However, we can use it to our advantage as the following.

```cpp
#include <iostream>
using namespace std;

int main() {
  int number = 7; 
  switch(number) {
  case 1:
  case 2:
  case 3:
  case 4:
  case 5:
  	cout << "your number is in the range from 1 to 5" << endl;
    break;
  case 6:
  case 7:
  case 8:
  case 9:
  case 10:
    cout << "your number is in the range from 6 to 10" << endl;
    break;
  default:
    cout << "your number is not in the range from 1 to 10";
}
  
  return 0;
}
```

output, 
```
your number is in the range from 6 to 10
```


## Examples

Take two numbers from the user and apply addition or subtraction based on the user's choice.
```cpp
#include <iostream>
using namespace std;

int main() {
    char op;
    int num1;
    int num2;
    cout << "Enter an operator \n (+)for addition \n (-) for subtraction" << endl;
    cin >> op;
    cout << "Enter your first number: ";
    cin >> num1;
    cout << "Enter your second number: " ;
    cin >> num2;
    cout << endl;
    

    switch (op) {
        case '+':
            cout << num1 << " + " << num2 << " = " << num1 + num2;
            break;
        case '-':
            cout << num1 << " - " << num2 << " = " << num1 - num2;
            break;
        default:
            cout << "No such operator exist";
            break;
    }

    return 0;
}
```

output,

```
Enter an operator 
 (+)for addition 
 (-) for subtraction
+
Enter your first number: 2
Enter your second number: 1
2 + 1 = 3
```
## Projects

| Project Title | Deadline |
|:-----------:|:-------------:|
| [Switch Statement in C++](https://github.com/SAFCSP-Team/switch-statement-in-cpp) | - | 
