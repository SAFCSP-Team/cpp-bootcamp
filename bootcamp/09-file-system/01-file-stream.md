# File System
The way to store data in a computer is by using files. C++ provides the ability to manage files using the `<fstream>` library.

## Concept 
**fstream** is a class that represents a file stream. By using fstream, we can create, read, write, and delete files.

> `<fstream>` library is used to include the file stream classes. While `<iostream>` is used to include the standard input/output stream classes. 

Like any other class, fstream has a constructor that takes two parameters: file name and mode (optional).
e.g. 
```cpp
fstream file("file_name", mode);
```

The **mode** argument is how we want to open the file and interact with it.

|Mode|Description|
|:-----------|:-------------:|
| ios::in | File opened in reading mode
| ios::out | File opened in write mode
| ios::binary | File opened in binary mode
| ios::ate | Set the initial position at the end of the file
| ios::app | File opened in append mode
| ios::trunc | File opened in truncate mode


There are two other classes that are derived from fstream:

**ifstream**:
Can be used to read from a file only.

```cpp
ifstream file("names.txt");
    for(string line; getline(file2, line);) {
        cout << line << endl;
    }
    file.close();
```

**ofstream**:
Can be used to write to a file only.
```cpp 
ofstream file("names.txt");
    file << "Sara" << endl;
    file.close();
```

## Example 
In this example, we will demonstrate how to work with fstream.

1. Import the fstream library.
```cpp
#include <fstream>
```

2. We will create an object from the fstream class, passing the file name and the mode as parameters.
```cpp
// ios::out - Create/Write a file
fstream file("note.txt", ios::out); // Create a file note.txt
```

3. Check if the file is open.
```cpp
if(file.is_open()) {
    // 
}
```

> * In the **if statement**, we check if the file stream is open, by using the `is_open()` method, which returns **true** if the file is open. If the file is open, we can write to it.
> * We can also use the `fail()` method to check if the file is open or not.

4. Write to the file by using the `<<` operator.
```cpp
if(file.is_open()) {
    file << "Hello, World!" << endl;
}
```
> If we want to write to the file, we can use the `<<` operator to write to the file.
> We can also use the `write()` method to write to the file.

5. Close the file stream.
```cpp
fstream file("note.txt", ios::out);
if(file.is_open()) {
    file << "Hello, World!" << endl;
    file.close(); // close the file stream
}
```

> Its important to close the file stream. So it will not interfere with other file streams.

6. Read from the file.
```cpp
fstream readFile("note.txt", ios::in);    
    if(readFile.is_open()) {
        string line;
        while(getline(readFile, line)) {
            cout << line << endl;
        }
        readFile.close();
    }
```

**Output:**
```
Hello, World!
```

> Above, we have created fstream object with mode `ios::in` to read from the file.



The full implementation of the example is as follows:
```cpp
#include <iostream>
#include <string>
#include <fstream>

using namespace std;

int main() {

    fstream file("note.txt", ios::out);
    if(file.is_open()) {
    file << "Hello, World!" << endl;
    file.close(); 
    }

    fstream readFile("note.txt", ios::in);    
    if(readFile.is_open()) {
    string line;
    while(getline(readFile, line)) {
        cout << line << endl;
    }
    readFile.close();
    }

    return 0;
}
```
**Output:**
```
Hello, World!
```

## Projects

- [File Stream](https://github.com/SAFCSP-Team/file-stream-project) 
