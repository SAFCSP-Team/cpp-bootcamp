# If-Else Statement



## Concept
If-else is the same as if statement, the difference is that we can handle other cases if the condition have not been met.

Syntax,

```
if(condition){
    // execute if condition is true.
}else{
    // execute if condition is false.
}
```

## Examples
```cpp
#include <iostream>
using namespace std;

int main() {
  bool isAdult = true;  // is the user an adult?
  bool isPassed = false; //did the user pass the driving test?
  if(isAdult && isPassed ){
  	cout << "Great, you can have your driving license now!" ;
  }else{
  	cout << "Sorry, you can not have your driving license yet."
  }
  
  return 0;
}
```

output, 

```
Sorry, you can not have your driving license yet.
```

```cpp
#include <iostream>
using namespace std;

int main() {
  int number = 10;
  if(number < 0 ){
  	cout << "Your number is negative." ;
  }else{
  	cout << "Your number is positive.";
  }
  
  return 0;
}
```

output,

```
Your number is positive.
```

## Projects

| Project Title | Deadline |
|:-----------:|:-------------:|
| [If-Else in C++](https://github.com/SAFCSP-Team/if-else-in-cpp) | - | 