# Introduction to Text File Handling
A text file is a file that contains a sequence of characters. For example, a text file may contain letters, numbers, and symbols. Using C++ we can read and write to a text file.

> The extension of a text file is **.txt**

## Concept 
In **C++** we can read and write to a file using the **<fstream>** library.
In order to read/write to a file, we need to use a stream.
Stream is a sequence of data. We need to create an input stream. If we want to write to a file, we need to create an output stream. If we want to do both, we need to create an input/output stream.


## Example
The stpes of reading a character sequence from a text file, we’ll need to perform the following steps:

* Create a stream object. 
* Connect it to a file on disk. 
* Read the file’s contents into our stream object. 
* Close the file


##### Write a text file.
```cpp

#include <fstream>
#include <iostream>
#include <string>
#include <list>

using namespace std;

int main() {

  list<string> names;
  names.push_back("Sara");
  names.push_back("Fahad");
  names.push_back("Majed");
  
  fstream wFile("names.txt", ios::out); // open a file on write mode
  
  if(wFile.is_open()) {
    for(string name : names) {
      wFile << name << endl;
    }
  }

  wFile.close();

  return 0;
}
```

##### Append to a text file.
```cpp

fstream aFile("names.txt", ios::app); // open a file on append mode

  if (aFile.is_open()) {
  
    aFile << "Ahmed" << endl;
  }

  aFile.close();
```


##### Read a file and print it to the console.
```cpp

fstream rFile("names.txt", ios::in); // open a file on read mode

  if (rFile.is_open()) {

    string line;

    while (getline(rFile, line)) {
      cout << line << endl;
    }
  }

  rFile.close();

```


## Projects
| Project Title | Deadline |
|:-----------|:-------------:|
| [Handle Text File](https://github.com/SAFCSP-Team/print-pointer-value) | - | 
