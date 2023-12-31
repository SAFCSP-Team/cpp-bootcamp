# String
In **C++**, does not have a built-in string type. Instead, it relies on the standard library to provide this functionality through a class called `std::string`.

## Concept 
**C++** strings are sequences of characters stored in a char array.

Strings are used to store text. They are also used to store data, such as numbers and other types of information. Strings in **C++** can be defined either using the std::string class or the C-style character arrays.

Char arrays are also used to store strings in **C++**.

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


int main () {
    char charVal[] = "Hello From Char Array";

    std:: cout << charVal << std::endl;

    return 0;
}

```

**output** 

```
Hello From Char Array
```


