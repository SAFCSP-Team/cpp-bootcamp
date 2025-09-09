# Else If Statement


## Concept
Else-if statement enables us to test different scenarios or cases using a chain of conditions.

Syntax,
```
if(first-condition){
    // statements

}else if(second-condition){
    // statements

}else{
    // statements
}
```

If the first condition has not been met, the second condition will be tested, if also the second condition has not been met the `else` block will be executed. 

Let us look at the following example. 

```cpp
#include <iostream>
using namespace std;

int main() {
  int number = 10; 
  if(number < 0 ){ 
  	cout << number << " is less than zero";
    
  }else if( number > 0){
    cout << number << " is greater than zero";
    
  }else{
    cout << number << " is equal to zero";
  }
  
  return 0;
}
```

Output

```
10 is greater than zero
```
As you can see, the output is `10 is greater than zero`, this happened because the program first checks the first condition, is `number` less than 0? the result of this comparison is false since 10 is not less than 0. Then the second condition is tested, is 10 greater than zero? the result of the second condition is true. Hence, the statements in the second block will be executed.

> You can have multiple else-if as needed by your program.

## Examples

```cpp
#include <iostream>
using namespace std;

int main() {
  bool isAdult = false;  // is the user an adult?
  bool isPassed = false; //did the user pass the driving test?
  if(isAdult && isPassed ){
  	cout << "Great, you can have your driving license now!" ;
    
  }else if(!isAdult && !isPassed){
  	cout << "You have to be an adult and to pass the test to get your license.";
    
  }else if(!isAdult){
  	cout << "You have to be an adult to get your license.";
    
  }else if(!isPassed){
  	cout << "You have to pass your driving license test.";
    
  }else{
  	cout << "an issue occurred";
    
  }
  
  return 0;
}
```

Output 
```
You have to be an adult and to pass the test to get your license.
```
Copy the example above and test it with different values.

## Projects
- [Else-If in C++](https://github.com/SAFCSP-Team/else-if-in-cpp)

