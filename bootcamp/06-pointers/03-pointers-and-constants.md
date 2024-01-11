# Pointers 
Pointers can be used with constant by referencing a constant variable, or by making a pointer constant to reference an address and never get updated to reference another address.

## Concept
A `pointer` is a reference variable that stores a memory address. And a `constant` is constant variable that will not change once it is initialized.

And by the use of these two concepts we can create a set of privileges to manage the access of pointers values and the value of what they reference to.

1. Non-constant pointer reference a non-constant variable.
2. Non-constant pointer reference a constant variable. 
3. Constant pointer reference a non-constant variable.
4. Constant pointer reference a constant variable.

<!-- Constant and pointers combined together gives us the ability or flexibility to manage how the program or a specific function can access a variable data. It enabled us to define a set privileges as the following.  -->

### Non-constant pointer reference a non-constant variable
This type will enable the program or a function to modify a pointer address and the value of what the pointer references. It is the least privilege from all other combinations and it is the same as what we used in our earlier topics.

To demonstrate the ides, look at the following example.

**Example by directly accessing pointers and its referenced value.**

```cpp
#include <iostream>
using namespace std;


int main() {
    int num1 = 20, num2 = 16;
    int* pointer = &num1; 
    
    cout << "num1 before updating: " << num1 << endl;
    cout << "pointer before updating: " << pointer << endl;
    
    *pointer = num1*2; //update the value of what pointer reference to.
    pointer = &num2; //update the pointer value.
    
    cout << "num1 after updating: " << num1 << endl;
    cout << "pointer after updating: " << pointer << endl;
    
    return 0;
}
```

```
num1 before updating: 20
pointer before updating: 0x7ffd1e88fed4
num1 after updating: 40
pointer after updating: 0x7ffd1e88fed0
```

### Non-constant pointer reference a constant variable. 
A non-constant pointer reference a constant variable means we will make the variable that a pointer points to as a constant, So you can not update the variable value through the pointer. let us take an example. 

```cpp
#include <iostream>
using namespace std;

int main() {
    int num1 = 20, num2 = 16;
    const int* pointer = &num1; 
    
    *pointer = 10; //error: assignment of read-only location '* pointer'
    
    return 0;
}

```
### Constant pointer reference a non-constant variable.
This means the pointer value can not change but the value it reference to can.

```cpp
#include <iostream>
using namespace std;

int main() {
    int num1 = 20, num2 = 16;
    int* const pointer = &num1; 
    
    *pointer = 10;
    pointer = &num2; //error: assignment of read-only variable 'pointer'
    
    return 0;
}

```

### Constant pointer reference a constant variable.
Both the value of the pointer and the value that it reference to can not be changed.

```cpp
#include <iostream>
using namespace std;

int main() {
    int num1 = 20, num2 = 16;
    const int* const pointer = &num1; 
    
    *pointer = 10; //error: assignment of read-only location '*(const int*)pointer'
    pointer = &num2; //error: assignment of read-only variable 'pointer'
    
    return 0;
}

```


## Examples
A function that updates both the pointer value and the variable value referenced by the pointer.

```cpp
#include <iostream>
using namespace std;

void updateNumAndPointer(int* ptr, int** ptrAddress){
    *ptr = 0; // num1 = 0;
    *ptrAddress = 0; // pointer = 0;
}

int main() {
    int num1 = 20, num2 = 16;
    int* pointer = &num1; 
    
    cout << "num1 before updating: " << num1 << endl;
    cout << "pointer before updating: " << pointer << endl;
    
    updateNumAndPointer(pointer, &pointer);
    
    cout << "num1 after updating: " << num1 << endl;
    cout << "pointer after updating: " << pointer << endl;
    
    return 0;
}
```

```
num1 before updating: 20
pointer before updating: 0x7ffcef799428
num1 after updating: 0
pointer after updating: 0
```



## Projects
 - Develop a function that allow you to update the value of the pointer but not the value of the reference variable. 
    - Non-constant pointer with a constant variable.