# String
It is a data type that represents text as a series of characters enclosed in double quotes `(" ")`.


## Concept 
In **C++** strings are sequences of characters stored in a char array.
**C++** does not have a built-in string type. Instead, it relies on the standard library to provide this functionality through a class called `string`.

> A char array is an array of type char that stores a sequence of characters.

Strings in **C++** can be stored either using:

* The std::string class (from the C++ Standard Library).
* C-style character arrays (an array of char).

> string is more commonly used becuase they can be used with standard operations, and more memeory can be allocated at run time. std::string is slower compared to C-style character arrays.

## Example
In the following example, we will demonstrate how to initialize two variables that hold a text value, by using the **string** and the **C-style character arrays**. 

* #### The string class.
  
```cpp
#include <iostream>
#include <string> // Include string from standard library
using namespace std;


int main () {

    string strVal = "Hello From String";

     cout << strVal << endl;
    
    strVal = "I\'m String";
    
    cout << strVal << endl;
    
    return 0;
}
```

**Output** 

```
Hello From String
I'm String
```


* #### The C-style character arrays.

```cpp
#include <iostream>
#include <cstring> // Include this library for strcpy function
using namespace std;

int main () {
    char charVal[] = "Hello From Char Array";

    cout << charVal << endl;
    
    return 0;
}
```

**Output** 

```
Hello From Char Array
```

## String functions
With the help of string functions, we can manipulate the string.

1. `string::length`
   
- The string function returns the length of the string.

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    string strVal = "abc"; // Length = 3
    cout << strVal.length() << endl;

    return 0;
}
```

**Output**

```
3
```

2. `string::compare`
- Compares two strings, and returns 0 if they're equal, and -1 if not.
```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    string strVal = "abc";
    cout << strVal.compare("abc") << endl;

    return 0;
}
```

**Output**

```
0
```

3. `string::substr`
- The string substring function extracts a substring from a string.
```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    string str = "Hi C++";
    str = str.substr(3, 3); // Extract substring starting at index 3 with length 3
    cout << str << endl;

    return 0;
}
```

**Output**
```
C++
```

3. `string::empty`
The string empty function returns 1 if the string is empty, and 0 if not.
```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    string name = ""; // Empty string

    cout << name.empty() << endl;

    return 0;
}
```

**Output**
```
1
```

> To know more about the string functions, visit this [article](https://blog.hubspot.com/website/c-string-functions).

## Projects

- [String Project](https://github.com/SAFCSP-Team/cpp-string-project)
