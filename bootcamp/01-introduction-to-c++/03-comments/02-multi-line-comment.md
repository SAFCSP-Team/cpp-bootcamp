# Multiline Comment

## Concept
Multiline comment is a note provided by the program developer that can be expanded to multiple lines.

## Example
To write a multiline comment in C++ we  will wrap the comment in `/*` and `*/` characters.

```cpp
#include <iostream>

using namespace std;

int main(){
    /* 
    Note:
    print Hello World. 
    */
    cout << "Hello ";
    cout << "World";
    return 0;
}
```
```cpp
#include <iostream>

using namespace std;

int main(){
    /* print Hello World. */
    cout << "Hello ";
    cout << "World";
    return 0;
}
```

## Projects
- Write a multiline comment to explain what does the following program do in general. 

```cpp
#include <iostream>
using namespace std;

int main(){
    cout << "Hello ";
    cout << endl;
    cout << "World";
    return 0;
}
```