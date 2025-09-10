# Class

##  Concept

### OOP and Classes
The object-oriented programming **(OOP)** is based on a complex data type known as the **“class”**.


### Class
It's a user-defined source of information. A class is a collection of data and information related to a specific area. The class consists of **properties** (data) and **methods** (functions).

_Class strtucture_

```c++
class ClassName {
    // properties (data members)
    // methods (functions)
};
```

### Properties (data)   
Properties are the **information/data** that a specific area/class could have/has.  
  
Let's take the student as a class and break it down. What information can a student's class have?     
It can have id, name, age, gpa, major... this information should be the class properties (data).    
  
```c++
class Student
{
// Properties (data)
    public: // public is a keyword in c++ indicating an access modifier
    int id;
    string name;
    int age;
    double gpa;
    string major;
};
```
> `public` in the above code means that all the properties below it are `public` and can be accessed outside the class (in the main function or other classes).
Access modifiers are explained in more detail here [Access modifiers](https://github.com/SAFCSP-Team/cpp-bootcamp/blob/main/bootcamp/10-class/02-access-modifiers.md)

### Methods (functions)   
Methods are the **behaviors or actions** that can be performed by the student class.    
   
Let's take the student class we used above. What could the student class do?     
We can write a method that prints the student properties.   
  
```c++
// Methods (functions)
void printInfo() {
        cout << "ID: " << id << endl;
        cout << "Name: " << name << endl;
        cout << "Age: " << age << endl;
        cout << "gpa: " << gpa << endl;
        cout << "major: " << major << endl;
    }

```
  
### Object
While a class is a blueprint, the objects are instances of a class. A class can have multiple objects (instances), and objects allow us to work with the data and functions defined in the class. Each object has its own set of properties and can independently call its methods.  
  
- Create an object of the Student class
```c++
int main(){
Student student1; // create Student object with the name "student1"
Student student2; // create another Student object with the name "student2"
};
```
<br/>     

- Access object properties

```c++
student1.id = 01;
```
<br/>    

- Print object properties
  
```c++
cout << student1.id << endl;
```
<br/>    

- Call object methods
  
```c++
student1.printInfo();  
``` 

## Example
Student class  

```c++
#include <iostream>

using namespace std;

class Student
{
    // Data members
    public:
    int id;
    string name;
    int age;
    double gpa;
    string major;

    // Member functions
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

Use student class in `main`  


```c++
int main()
{
    Student student1;

    student1.id = 01;
    student1.name = "Ahmed";
    student1.age = 17;
    student1.gpa = 4.6;
    student1.major = "Computer Science";

    student1.printInfo();

    return 0;
}
```


```c++
ID: 1
Name: Ahmed
Age: 17
gpa: 4.6
major: Computer Science
```
  
  
## Project 


- [Class project](https://github.com/SAFCSP-Team/cpp-class-project)


