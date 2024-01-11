# String
Strings are used to store text. They are also used to store data, such as numbers and other types of information. 

It is a data type that represents text as a series of characters enclosed in double quotes `(" ")`.


## Concept 
In **C++** strings are sequences of characters stored in a char array.
**C++** does not have a built-in string type. Instead, it relies on the standard library to provide this functionality through a class called `std::string`.


Strings in **C++** can be stored either using:

* **The std::string class**.
* **The C-style character arrays**.

## Example

In the following example, we will print the string `Hello From String` using the `std::string` class, and then we will print the `Hello From Char Array` using the C-style character arrays.

### **code**

* #### The std::string class.
Using the `std::string` class declare a std::string variable and print it.

```cpp

#include <iostream>

int main () {

    std::string strVal = "Hello From String";

    std:: cout << strVal << std::endl;
    
    strVal = "I\'m String";
    
    std::cout << strVal << std::endl;
    
    return 0;
}

```

**output** 

```
Hello From String

I'm String
```

<hr>

* #### The C-style character arrays.
Using the C-style character arrays declare a char array variable and print it.


```cpp

#include <iostream>
#include <cstring> // Include this library for strcpy function

int main () {
    char charVal[] = "Hello From Char Array";

    std::cout << charVal << std::endl;

    strcpy(charVal, "I\'m Char Array");

    std::cout << charVal << std::endl;

    return 0;
}

```

**output** 

```
Hello From Char Array

I'm Char Array
```


## Projects
1. Create a string variable using the `std::string` class and print it.
2. Append a string to the string variable.
3. Create a char array variable and print it.
