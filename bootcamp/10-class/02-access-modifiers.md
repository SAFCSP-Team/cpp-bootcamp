# Access modifiers
The visibility and accessibility of class functions and properties

##  Concept
Functions and properties can have different access modifiers, which control their visibility and accessibility from other parts of the program. 

### Access modifiers types  

1. `Public`
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
1
```

<br/>
<br/>

2. `Private`   
The class functions and properties are only accessible within the class itself.
They cannot be accessed directly by objects of the class or by functions outside the class.
   
```c++
#include <iostream>

using namespace std;

class Student {
private:
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
error: 'id' is a private member of 'Student'
```

<br/>
<br/>

3. `Protected`   
The class functions and properties are only accessible within the class itself, as well as in its derived classes.   
They cannot be accessed directly by objects of the class or by functions outside the class.  
Members declared as protected can be accessed by the class that defines them and by any derived classes.
   
```c++
#include <iostream>

using namespace std;

class Student {
protected:
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
error: 'id' is a protected member of 'Student'
```
<br/>
By default, if no access modifier is provided, class properties are considered private. 


## Example

When we write an access modifier in the code for example `private`, all the properities/functions below the access modifier become `private`, and the same rule applies for `public` and `protected`.   
   
Student class

```c++

#include <iostream>

using namespace std;

class Student {

    // Properties (data members)

private:
    int id;

public:
    string name;
    int age;
    double gpa;
    string major;

    /*
    To access private properties in main function,
    we can create set(value) and get() functions
    */

    /*
    set(value) is for updating and changing the id value
    */
    void setId(int value)
    {
        id = value;
    }

    /*
    get() is for getting and returning id value
    */
    int getId()
    {
        return id;
    }

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

int main() {

    Student student;

    // assign a value to the private property (id)
    student.setId(15);

    // assign a value to the public properties
    student.name = "Mohammed";
    student.age = 21;
    student.major = "Computer Science";

    // print the value to the private property (id)
    cout << "Student id: " << student.getId() << endl;

    // print all students properties
    student.printInfo();
}
```


```c++
Student id: 15
ID: 15
Name: Mohammed
Age: 21
gpa: 0
major: Computer Science
```

 
## Project 

| Project Title | Deadline |
|:-----------:|:-------------:|
| [Access modifier](https://github.com/SAFCSP-Team/access-modifier) | - |





