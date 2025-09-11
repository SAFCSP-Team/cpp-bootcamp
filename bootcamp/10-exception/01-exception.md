# Exception 
An exception is an error that occurs during the execution of a program. When an exception occurs, the program execution is terminated. 

To let the program continue execution after an exception occurs, we can use **exception handling**.

## Concept
An exception is a way used to manage errors in a program. By handling errors effectively, we can allow the program to continue running regardless of the error, or we can display a meaningful message to the user.

### Exception Keywords

**try**: is used to wrap the code that might throw an exception.

```cpp
try{
    // code that might throw an exception
}
```
**catch**: is a block of code that will be executed if there is an exception in the try block. 
 
```cpp
try{
    // code that might throw an exception
} catch(exception e) {
    // code to handle the exception
}
```
> The exception e is the object that will hold the error message.

**throws**: is a keyword that is used to specify the error type that might be thrown.

```cpp
try{
    // code that might throw an exception
    throw "Error Message";
} catch(exception e) {
    // code to handle the exception
}
```
> The "Error Message" is the message that will be printed if the exception is thrown.


## Example

- Try-catch block without throw or specify the error type.

```cpp
#include <iostream>
using namespace std;

int main() {
    try {
      string name = "ahmed";
      cout << name.at(8)  << endl;
    }

    catch(...) {
      cout << "Error" << endl;
    }

}
```
**OUTPUT**

```
Error
```
> catch(...) will catch any error that might occur in the try block.

- Custom error handling using throw.

```cpp
#include <iostream>
using namespace std;

int main() {
    try {
       string name = "Abdulmalik";
       if(name.length() > 5) {
           throw "Name is too long";
       }
       cout << name << endl;
    }

    catch(const char* e) {
        cout << "Error: " << e << endl;
    }
}
```
**OUTPUT**

```
Error: Name is too long
```

- Handling multiple exceptions. 

```cpp
#include <iostream>
using namespace std;

int main() {
    try {
        int *array = new int[999999999999999]; 
    }

    catch(bad_alloc &e) {
        cout << "Exception: " << e.what() << endl;
    }

    catch(exception &e) {
        cout << "Exception: " << e.what() << endl;
    }

    catch(...) {
        cout << "Other Exception" << endl;
    }
}
```
**OUTPUT**

```
Exception: std::bad_alloc
```

> * bad_alloc is the one that will be invoked because we are trying to allocate a huge memory.
> * If none of the exception is matched the catch(...) will be invoked.


## Projects
- [Exception](https://github.com/SAFCSP-Team/exception-project-cpp)  
