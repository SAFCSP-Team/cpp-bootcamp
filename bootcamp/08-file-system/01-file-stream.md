# File System
We can use C++ to create, read, write, and delete files and directories.

In Computer there are two types of files:
* Text files are files that contain sequences of characters. 
* Binary files are files that contain sequences of bytes.

C++ handles both types text file and binary file.

## Concept 
In C++ we can manage files using the `<fstream>` library.
**fstream** is a class that represents file stream. By using fstream, we can create, read, write, and delete files.

> `<fstream>` library is used to include the file stream classes. while `<iostream>` is used to include the standard input/output stream classes. 

Like any other class, fstream has a constructor that takes two parameters: file name and mode (optional).
e.g. 
```cpp

fstream file("file_name", mode);

```

The mode argument is how we want to open the file and interact with the file.

|Mode|Description|
|:-----------|:-------------:|
| ios::in | File opened in reading mode
| ios::out | File opened in write mode
| ios::binary | File opened in binary mode
| ios::ate | Set the initial position at the end of the file
| ios::app | File opened in append mode
| ios::trunc | File opened in truncate mode

```cpp 
fstream file ("file_name", mode);
```

There are two other classes that are derived from fstream:
**ifstream**
Can be used to read from a file only.

```cpp

ifstream file("names.txt");
    for(string line; getline(file2, line);) {
        cout << line << endl;
    }
    file.close();
```

**ofstream**
Can be used to write to a file only.
```cpp 

ofstream file("names.txt");
    file << "Sara" << endl;
    file.close();
```

## Example 
in this example we will create a file and write to it, finally we will read from it.
```cpp
// ios::out - Create/Write a file
    fstream file("note.txt", ios::out); // Create a file note.txt
    file << "Hello, World!" << endl; // Write to the file
    cout << file << endl; // Print the file
    file.close(); // Close the file
```



