# Exception 
Exception is an error that occurs during the execution of a program. When an exception occurs, the program execution is terminated. 

To let the program continue execution after an exception occurs, we can use exception handling.

before we start with exception let's see type of errors in C++:
-  Compile-time errors: Errors found by the compiler. syntax errors. Example: missing semicolon or the variable is not declared.

```cpp

cout << "Hello World!" << endl // compile time error due to missing semicolon

```

-  Run-time errors: Errors found by checks in a running program. Also called exceptions. Example: dvivde by zero, excpetion occur at run time.

```cpp

cout << 5/0 << endl; // run time error

```

## Exception concept
In C++ exceptions are handled using three keywords: try, catch, and throw.

**try**: is a block of code that is used to handle the error or exception that might occur in the program. 

**catch**: is a block of code that will be executed if there is an exception in the try block. 

**throw**: is a keyword that categorize the error or exception.

> let's say you excpet mathmatical error in try block then you can use throw mathmatical to handl the mathmatical error.

## Example

### Handling exception without using throw

```cpp

try {
    string name "ahmed";

    cout << name[8] << endl;
}
catch(...) {
    
        cout << "Error" << endl;
    
    }

```

### Handling multiple exception

```cpp

try {

    int *array = new int[99999999999]; 

}
catch(bad_alloc &e) {

    cout << "Exception: " << e.what() << endl;

}
catch(exception &e) {

    cout << "Exception: " << e.what() << endl;

}
catch(...) {

    cout << "Other Exception" << endl;

}

```



Practices
- Practice 1: handle mathmatical error using throws mathmatical.
- Practice 2: handle array out of bound error using throws array out of bound.