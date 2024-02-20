# String
It is a data type that represents text as a series of characters enclosed in double quotes `(" ")`.


## Concept 
In **C++** strings are sequences of characters stored in a char array.
**C++** does not have a built-in string type. Instead, it relies on the standard library to provide this functionality through a class called `string`.

> Char array is an array of type character 

Strings in **C++** can be stored either using:

* **The std::string class**.
* **The C-style character arrays**.

> string is more commonly used becuase they can used with standard operations, and more memeory can be allocated at run time. However string is slower than char array.

## Example
In the following example, we will demonstrate how to initialize two variables that hold a text value, by using the **string** and the **C-style character arrays**. 

* #### The string class.
Using the **string class** in.

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

**output** 

```
Hello From String
```

<hr>

* #### The C-style character arrays.
Using the C-style character arrays declare a char array variable and print it.


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

**output** 

```
Hello From Char Array
```

## String functions
With the help of string functions we can maniuplate the string.

1. string::length
The sring function returns the length of the string.

```cpp
    string strVal = "abc"; // 3
    cout << strVal.size() << endl;
```

**OUTPUT:**

```
3
```

2. compare 
The string comparison function compares two strings, and return 0 if its equal, and -1 if not.
```cpp
    string strVal = "abc";
    cout << strVal.compare("abc") << endl;
```

**OUTPUT:**

```
0
```

3. substr
The string substring function extracts a substring from a string.
```cpp
    string str = "Hi C++";
    str = str.substr(3, 6);  // Replaces the substring "World" with "Universe"
    cout << str << endl;
```

**OUTPUT:**
```
C++
```

3. empty
The string empty function returns 1 if the string is empty, and 0 if not.
```cpp
  string name = "";

  cout << name.empty() << endl;
```

**OUTPUT:**
```
1
```

> To know more about the string functions visit this [article](https://blog.hubspot.com/website/c-string-functions).

## Projects
|Title|Deadline|
|:--|:--|
|[String Project](https://github.com/SAFCSP-Team/cpp-string-project)|
