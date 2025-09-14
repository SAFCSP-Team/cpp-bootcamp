# Introduction to Text File Handling
A text file is a file that contains a sequence of characters. 

For example, a text file may contain letters, numbers, and symbols. 

We can read and write into a text file using C++.

> It's common to use **.txt** extension for storing a text file.

## Concept 
In **C++** we can read and write to a file using the `<fstream>` library.
In order to read/write from/to a file, we need to use a stream.
A stream is a sequence of data. We need to create an input stream for reading from a file. If we want to write to a file, we need to create an output stream. If we want to do both, we need to create an input/output stream.


## Example
For reading a character sequence from a text file, we’ll need to perform the following steps:

* Create a stream object. 
* Connect it to a file on disk. 
* Read the file’s contents into our stream object. 
* Close the file


##### Write a text file.
```cpp

#include <fstream> // Import fstream to open and interact with the file
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
  
  // check if the file is open
  if(wFile.is_open()) {
    // if the file is open, insert the names list into the file names.txt
    for(string name : names) {
      wFile << name << endl;
    }
  }

  wFile.close(); // close the file steam 

  return 0;
}
```
> [!NOTE]
> For compiling and running range-based for loops `for(string name : names)` execute this command on the terminal `g++ -std=c++11 Main.cpp -o Main`.

##### Append to a text file.
```cpp

fstream aFile("names.txt", ios::app); // open a file on append mode

  if (aFile.is_open()) {
    // add Ahmed to names.txt
    aFile << "Ahmed" << endl;
  }

  aFile.close(); // always closing the fstream object
```
> Append will add content to the file.

##### Read a file and print it to the console.
```cpp

fstream rFile("names.txt", ios::in); // open a file on read mode

  if (rFile.is_open()) {

    string line; // Define a string line that will represent a line in the names.txt file

    while (getline(rFile, line)) {
      cout << line << endl;
    }
  }

  rFile.close();
```
Output
```
Sara
Fahad
Majed
Ahmed
```


## Projects

- [Handle Text File](https://github.com/SAFCSP-Team/handle-text-file-project)

