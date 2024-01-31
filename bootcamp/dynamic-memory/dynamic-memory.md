# Dynamic memory
It's the concept/process of storing/manipulating data at compile time.


## Concept

In C++ the memory can be allocated either at **compile time (Static memory allocation)** or at **the run time (Dynamic memory allocation)**. 
<br/>
<br/>
  
1. Static memory allocation

- It's the memory allocation during compile time.
- The memory allocated is fixed and cannot be increased or decreased at run time.
- The memory is stored in the stack.
  
Let's say we have an array with a fixed size:
```c++ 
arr [5] = {1,2,3,4,5}
```
arr size is allocated at compile time and it's fixed.
<br/>
<br/>
  
2. Dynamic memory allocation

- Is the process of allocating the memory at the run time (time of execution).
- The memory is stored in the heap.
- Allocated memory can only be accessed through pointers.

- It uses two operators:
1. **new** operator is used to allocate memory for a single object dynamically
 
2. **delete** operator is used to deallocate memory that was previously allocated with **new**.

<br/>
<br/>
<br/>

## Example 

Using dynamic memory allocation:

<br/>

Integer example:
```c++
int main(){
int* p = new int;
};
```
- In the above code, we created a pointer `p` using the dynamic memory allocation operator (new).
- Stack is storing the address of `p`.
- Heap is storing the value of `p` which will be defined based on the programmer input.

- `p` value:
```c++
*p = 5;
```
In the above code, the `p` value is defined at run time and it's 5.

<br/>
<br/>

Array example:
```c++
int main(){
int SIZE;
int* arr = new int[SIZE];
};
```
- In the above code we created an array with the size `SIZE` using the dynamic memory allocation operator (new).
- Stack is storing the address of `SIZE`.
- Heap stores the value of `SIZE` which will be defined based on the programmer input.

- `SIZE` value:
```c++
arr[0] = 1;
arr[1] = 2;
arr[2] = 3
```
In the above code, the `SIZE` value is defined at run time.

<br/>
<br/>

After running the program, all values in the stack will be deleted, but the values in the heap will not.

Deleting heap values is the programmer's responsibility.

We can use the **delete** operator to delete values stored in the heap.
```c++
delete p;
delete[] arr;
```


## Projects


Project Title | Deadline |
|:-----------:|:-------------|
[Tree with non-primitive data types](https://github.com/SAFCSP-Team/dynamic-memory-project) | -







