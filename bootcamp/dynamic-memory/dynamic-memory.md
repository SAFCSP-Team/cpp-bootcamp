# Dynamic memory
It's the concept/process of storing/manipulatin data at compile time.


## Concept

In C++ the momory can be allocated either at compile time or at the run time.

- Static memory allocation.

Is the memory allocated during compile time.

The memory allocated is fixed and cannot be increade or decreased at run time.

The memory is sored in stack.

Let's say we have an array with fixed size:
arr [5] = {1,2,3,4,5}
arr size is allocated at compile time and it's fixed.


- Dynamic memory allocation

Is the process of allocating the memory at the run time (time of execution).

The memory is sored in heap.

Allocated memory can only be accessed through pointers.

It's using two operators:
1. new
The `new` operator is used to allocate memory for a single object dynamically
 
2. delete 
The delete operator is used to deallocate memory that was previously allocated with `new`.


## Example 

Using dynamic memory allocation:

Integer example:
```c++
int main(){
int* p = new int;
};
```
- In the above code, we created a pointer `p` using dynamic memory allocation operator (new).
- Stack is storing the address of `p`.
- Heap is storing the value of `p` .

- `p` value:
```c++
arr[0] = 1;
arr[1] = 2;
arr[2] = 3
```
In the above code, the `p` value is defined at run time and it's 3.

Array example:
```c++
int main(){
int SIZE;
int* arr = new int[SIZE];
};
```
- In the above code we created a arr with the size `SIZE` using dynamic memory allocation operator (new).
- Stack is storing the address of `SIZE`.
- Heap is storing the value of `SIZE` witch will be defined based on the user's input.

- `SIZE` value:
```c++
arr[0] = 1;
arr[1] = 2;
arr[2] = 3
```
In the above code, the `SIZE` value is defined at run time and it's 3.


After running the program, all values in the stack will be deleted, but the values in the heap will not.

Deleting heap values is the programmer responsibitie.

We can use delete operstor to delete values stored in the heap.
```c++
delete p;
delete[] arr;
```


## Projects
