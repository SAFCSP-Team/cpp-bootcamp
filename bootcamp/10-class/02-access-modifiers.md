# Access modifiers
The visibility and accessibility of class functions and properties

##  Concept
Functions and properties can have different access modifiers, which control their visibility and accessibility from other parts of the program. 

### Access modifiers types  

1. Public:  
The class functions and properties are accessible anywhere (in the class it-self, main function, ...).  
They can be accessed by objects of the class or by functions outside the class.

```c++
#include <iostream>

using namespace std;

class Student {
public:
  int id;
};

int main() {
  Student student1;
  student1.id = 01;
  cout << student1.id << endl;
  return 0;
};
```
  
Output
```c++
01
```

<br/>
<br/>

2. Private:    
The class functions and properties are only accessible within the class itself.
They cannot be accessed directly by objects of the class or by functions outside the class.
   
```c++
class Student
{
private:
int id;
};

int main()
{
Student student1;
student1.id = 01;
cout << student1.id << endl;
return 0;
};
```
  
Output
```c++
Error: member "Student::id" (declared at line 10) is inaccessible
```
<br/>
By default, if no access modifier is provided, class properties are considered private. 


## Example
Student class:  

```c++

class Student
{
// Properties (data members)
    int id;
    string name;
    int age;
    double gpa;
    string major;

// Methods (functions)
void printInfo()
    {
        cout << "ID: " << id << endl;
        cout << "Name: " << name << endl;
        cout << "Age: " << age << endl;
        cout << "gpa: " << gpa << endl;
        cout << "major: " << major << endl;
    }
};
```

 
## Project 

| Project Title | Deadline |
|:-----------:|:-------------:|
| [Access modifier](https://github.com/SAFCSP-Team/access-modifier) | - |





