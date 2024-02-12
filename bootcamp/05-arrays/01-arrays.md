# Arrays
Imagine a scenario where we have two libraries: one is organized, and the other is scattered. In an organized library, the books are systematically arranged and categorized by genre, with each genre having its designated section. On the other hand, in a scattered library, the books are randomly placed without any organization or system. You might find books of different genres randomly mixed together on the shelves.

It is important to note that an organized library significantly improves the ease of dealing with books by providing a structured system for book organization. In contrast, a scattered library lacking such organization creates difficulties and hinders efficient dealing with library resources.

## Concept
In computer programming, in most cases, there is a need to **store a large number of similar data**. for example, books or weekdays. So, instead of using different variable names to represent each value, it is **better to define an array and store all the elements in it** to significantly improve the ease of dealing with data.

`Array`: is a collection of similar data items grouped together.


- Arrays can store **primitive** data types or **non-primitive** data type.
<img width="910" alt="Introduction to Arrays-01" src="https://github.com/SAFCSP-Team/cpp-bootcamp/blob/main/bootcamp/05-arrays/image/array.png">

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

- The `length` of an array refers to the **number of elements** contained within the array.
```C++
 int size =  sizeof(Prices) / sizeof(Prices[0]); // 5
```
We use the **sizeof operator** to get the total size of the array ***(sizeof(array name))*** depending on the data type and **divide it by the size of a single element** ***(sizeof(array name[0]))***. This gives us the number of elements in the array.

> For an alternative method to calculate the length of an array in c++, kindly visit [digitalocean](https://www.digitalocean.com/community/tutorials/find-array-length-in-c-plus-plus)


- The `index` of an array refers to the **position or location of an element** within the array. It represents the **unique numeric** identifier assigned to each element in the array.
- Array indexes start from 0 and increment by 1 for each subsequent element.
```C++
Prices[0]; //1.5
```
- If the size of an array is **n**, the maximum index number is **n-1**.
```C++
Prices[size -1 ]; //5.7
```
To perform any operations on each element of an array, you can use loops. For example, to print all the elements of the **Prices** array.
```c++
cout<<"The elements are: ";
    for(float i : Prices)
    {
    	cout << i << " ";
    }
```
```
The elements are: 1.5 2.7 3.14 4.2 5.7 
```
> A for-each loop iterates over the elements of arrays, vectors, or any other data sets. [digitalocean](https://www.digitalocean.com/community/tutorials/foreach-loop-c-plus-plus#introduction)

## Example 
- Array of integer: 
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
- Array of string:  
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
| Project Title | Deadline |
|:-----------:|:-------------:|
| [Arrays](https://github.com/SAFCSP-Team/arrays) | - | 
