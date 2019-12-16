# C++ developer Guide

 ### Prerequisite ###
 1. How Computer works
 2. Number System
 3. What is a program
 4. Low-Level vs High-Level Program
 5. Compiler vs Interpreter
 6.  Operating System
 7. What is a Algorithm
 8. What is Flow chart

  ### C++ Basic ###

#### Skeleton of C++ ####

```cpp
#include<iostream>

int main() {

    return 0;
}
```

##### Basic example #####

```cpp
#include<iostream>
using namespace std;

int main() {

    string str;
    cout<<"May i know your Name?";
    cin>>str;
    cout<<"Hello"<<str;
    return 0;
}
```
Here to get input from user we used `cin` instead that we can use `getline`. The difference between `cin` and `getline` is if we are using in `cin` then while typing if we give a space between words it take only first word, where as `getline` take input untill user press enter!

 ##### Basic example Unsing getline #####

 ```cpp
#include<iostream>
using namespace std;

int main() {

    string str;
    cout<<"May i know your Name?";
    getline(cin,str);
    cout<<"Hello"<<str;
    return 0;
}
```

#### Data Types ####

Primitive | User Defined | Derived   |
----------| -------------|-----------|
Int       | Enum         | Array     |
Char      | Structure    | Pointer   |
Boolean   | Unoin        | Reference |
Float     | class        |           |
Double    |              |           |

##### need add a pic explaning size and Range alest for one data type #####

#### Operators and Expressions ####

 ```cpp
Arthimetic       +, -, *, /, %
Relational       <, >, <=, >=, == 
Logical          &&, ||, !
Bitwise          &, !, ~, ^
Increment        ++
Decrement        --
Assignment       =

```
Operator | Precedence| 
----------| ---------|
( )       | 3        |
*, /, %   | 2        |
+, -      | 1        |


example 
 (-b+-√b^2-4ac) / 2a in c++

 (-b+ sqrt(b*b - 4*a*c))/(2*a)