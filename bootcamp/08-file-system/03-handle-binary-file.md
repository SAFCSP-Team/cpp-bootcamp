# Binary File Handling
A binary file is a file that contains data stored in a **sequence of bytes**, which can be represented in various bases such as binary, hexadecimal, decimal, or octal.

Binary files can contain any type of data, such as images, audio, video, or text.

Binary file is not human readable, the file exteions is decide how to seperate the bytes into meaningful data. In this lesson we will use the **.bin** extension to create a binary file.

> Binary files can have any extension, in this lesson we will use **.bin** extension.

## Concept 
In **C++** we can read and write to a binary file using the **<fstream>** library, the same as text file. But we need to open the file in binary mode by adding **ios::binary** flag to the open mode.

To read binary data from a file, we’ll need to do the following steps:
* Import fstream library.
* Create a stream object with pesific mode. 
* Preform the operation on the file. 
* Close the file stream using `close()` function.


## Example
In this example we will write a binary file that contating a string as value and read it.


##### Write a binary file.
```cpp
#include <iostream>
#include <fstream> // Import fstream library
#include <string>
using namespace std;

int main() {

  // create a file stream object with write mode
  fstream wFile("data.bin",
                ios::out |
                    ios::binary); // open a file on write mode in binary format

  if (wFile.is_open()) {
    // when adding a string we must pass the size of the string
    wFile.write("Hello", 5);
  }

  wFile.close();
 
  return 0;
}

```
> In the above example we have write a text into a binary file.

##### Append a binary file.
```cpp
fstream aFile("data.bin", ios::app | ios::binary);

  if(aFile.is_open()) {
    aFile.write(" World", 6);

  }
```

##### Read a binary file.
```cpp

fstream rFile("data.bin", ios::in | ios::binary);
  if(rFile.is_open()) {
    char buffer[100];
    rFile.read(buffer, 100);

    cout << buffer << endl;
    rFile.close();
  }
```

**Output:**
```
Hello World
```

## Projects
| Project Title | Deadline |
|:-----------|:-------------:|
| [Handle Binary File](https://github.com/SAFCSP-Team/binary-file-project) | - | 