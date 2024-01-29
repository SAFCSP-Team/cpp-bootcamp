# Class
User-defined source of information

##  Concept

### OOP and Classes:
The object-oriented-programming **(OOP)** is based on a complex data type known as the **“class”**


### Class
It's a user-defined source of information. Class is a collection of data and information on specific areas. The class consists of `properties` (data members) and `methods` (functions).

_Class strtucture_:

```c++
class ClassName {
    - properties (data members)
    - methods (functions)
};
```
<br/> 
<br/> 
 
1. Properties (data members)   
`Properties` are the **information/data** that a specific area/class could have/has.  
  
Let's take the student as a class and break it down, let's ask ourselves what information a student class has.     
It can have id, name, age, gpa, major.. this information should be the class `properties` (data members).    
  
```c++

class Student
{
// Properties (data members)
    public:
    int id;
    string name;
    int age;
    double gpa;
    string major;
}
```
<br/> 
<br/> 
  
2. Methods (functions)   
`Methods` are the **behaviors or actions** that can be performed on a student's class.    
   
Let's take the student class we used above, what could the student class do?     
We can write a `method` that prints the student properties.   
  
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
<br/> 
<br/> 
  
### Object
Objects are instances of a class. Objects allow us to work with the data and functions defined in the class. Each object has its own set of `properties` and can independently call the `methods`.  
  
- Create an object of Student class:  
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
