# Access modifiers
The visibility and accessibility of class functions and properties

##  Concept
Functions and properties can have different access modifiers, which control their visibility and accessibility from other parts of the program. 

### Access modifiers types  

1. Public:  
The class functions and properties are accessible with no issues.
They can be accessed by objects of the class or by functions outside the class.
   
2. Private:    
The class functions and properties are only accessible within the class itself.
They cannot be accessed directly by objects of the class or by functions outside the class.


By default, if no access specifier is provided, class members are considered private. Here's an example that demonstrates the use of access modifiers:
  
  
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
