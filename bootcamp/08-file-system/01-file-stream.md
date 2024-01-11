# File System
C++ have a rich library for file system to handle files and directories. 


## Concept 
The I/O system of C++ contains a set of classes which define the file handling methods. These include ifstream, ofstream and fstream classes. These classes are derived from fstream and from the corresponding iostream class. These classes, designed to manage the disk files, are declared in fstream and therefore we must include this file in any program that uses files.

> `<fstream>` library is used to include the file stream classes. while `<iostream>` is used to include the standard input/output stream classes. 


## Example
In this example we will reuqest input from the user and store it in a file called `nameList.txt` and then we will read the file and print the output.

### **code**


```cpp

#include <iostream>
#include <fstream> 

using namespace std;

int main() {

    cout << "Enter your name: ";

    string userInput;
    cin >> userInput;

    ofstream writeFile("nameList.txt"); 

    writeFile << userInput;

    writeFile.close();
  
    ifstream readFile("nameList.txt");

    string userOutput;

    readFile >> userOutput;

    cout << userOutput << endl;

    readFile.close();

    return 0;
}

```
