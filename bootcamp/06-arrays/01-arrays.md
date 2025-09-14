# Arrays
In computer programming, in most cases, there is a need to **store a large number of similar data**. for example, books or weekdays. So, instead of using different variable names to represent each value, it is **better to define an array and store all the elements in it** to enhance the way of dealing with data.
## Concept
`Array` : is a collection of similar data items grouped together.

- Arrays can store **primitive** data types or **non-primitive** data type.

Suppose you need to store prices for five items. You can simply create an array of five float numbers called `prices` 
<img width="910" alt="Introduction to Arrays-01" src="https://github.com/SAFCSP-Team/cpp-bootcamp/blob/main/bootcamp/06-arrays/image/array-in-cpp.png">

```c++
#include<iostream>
using namespace std; 
int main() {
    float Prices[5];  // Declaration

    Prices[0] = 1.5f;  // Initialization
    Prices[1] = 2.0f;
    Prices[2] = 3.14f;
    Prices[3] = 4.2f;
    Prices[4] = 5.7f;

   return 0;
}
```
Explanation:
- `float Prices[5]` declares an array named Prices, consisting of five float numbers.
- `Prices[x] =` access each element of the array and initialize its value.

### Access the array elements
To access an element in the array, you must use its `index`.
- The `index` of an array refers to the **position or location of an element** within the array. It represents the **unique numeric** identifier assigned to each element in the array.
- Array indices in C++ start from 0, so `Prices[0]` refers to the first element, and `Prices[4]` refers to the last one in this case.
```C++
Prices[0]; //1.5
```
- If the size of an array is **n**, the maximum index number is **n-1**.
```C++
Prices[5 -1 ]; //5.7
```

### Array size 
The `size` of an array refers to the **number of elements** contained within the array.
```C++
 int size =  sizeof(Prices) / sizeof(Prices[0]); // 5
```

We use the **sizeof operator** to determine the total size of the array by using `sizeof(array_name)`. To find the number of elements in the array, we divide this total size by the size of a single element, which can be given with `sizeof(array_name[0])`. This calculation gives us the total number of elements in the array.

> For an alternative method to calculate the length of an array in c++, kindly visit [digitalocean](https://www.digitalocean.com/community/tutorials/find-array-length-in-c-plus-plus)


### Array operations 

To perform any operations on each element of an array, you can use loops. For example, to print all the elements of the **Prices** array.
```c++
cout<<"The elements are: ";
    for(float i : Prices)
    {
    	cout << i << " ";
    }
```
```
The elements are: 1.5 2.0 3.14 4.2 5.7 
```
> A for-each loop iterates over the elements of arrays, vectors, or any other data sets. [digitalocean](https://www.digitalocean.com/community/tutorials/foreach-loop-c-plus-plus#introduction)

## Example 
- Array of integers
```c++
#include <iostream>
int main() {
    int numbers[] = {1, 7, 9, 1, 5};
    int count = sizeof(numbers) / sizeof(numbers[0]);
    int secondElement = numbers[1];

    std::cout << "The count = " << count << std::endl;
    std::cout << "The secondElement = " << secondElement << std::endl;
    return 0;
}
```
```
The count = 5
The secondElement = 7
````
- Array of strings 
```c++
#include <iostream>
#include <string>

int main() {
    std::string names[] = {"Alaa", "Amal", "Ahlam", "Manal"};

    int count = sizeof(names) / sizeof(names[0]);
    std::string secondName = names[1];

    std::cout << "The count = " << count << std::endl;
    std::cout << "The secondName = " << secondName << std::endl;

    return 0;
}
```
```
The count = 4
The secondName = Amal
````

## Project 
- [Arrays](https://github.com/SAFCSP-Team/arrays)
