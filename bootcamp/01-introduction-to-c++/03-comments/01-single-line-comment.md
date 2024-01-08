# Single Line Comment
In our daily life, we sometimes write a note of what we need to do as a reminder, or write an explanation of a specific text in a book. These notes are also called comments. Same thing we do in programs, to not forget what a function does or to explain it as a documentation for other developers on the project, we use the concept of comments.

## Concept
Single line comment is a note provided by the program developer that can fit in a single line.
> Comments are ignored by the compiler when running a program.

## Example
To write a single line comment in C++ we use `//` character.

```cpp
#include <iostream>

using namespace std;

int main(){
    // print Hello World.
    cout << "Hello ";
    cout << "World";
    return 0;
}
```

we can also add the comment at the end of a line.
```cpp
#include <iostream>

using namespace std;

int main(){
    cout << "Hello "; // print Hello.
    cout << "World";  // print World.
    return 0;
}
```

## Projects