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

 ```cpp
 (-b+-√b^2-4ac) / 2a in c++

 (-b+ sqrt(b*b - 4*a*c))/(2*a)

```

#### Example of Conditional Statement ####

 ```cpp

#include<iostream>
using namespace std;

int main() {

    int a,b,c;
    cout<<"Enter 3 no's";
    cin>>a>>b>>c;
    if(a>b && a>c) {
        cout<<a<<endl;
    } else {
        if(b>c) {
            cout<<b<<endl;
        } else {
            cout<<c<<endl;
        }
    }
    return 0;
}

```

```cpp

#include<iostream>
using namespace std;

int main() {

    int day;
    cout<<"Enter day number";
    cin>>day
    if(day == 1) {
        cout<<"Mon"<<endll;
    } else if (day == 2) {
        cout<<"Tue"<<endl;
    } else if (day ==3) {
        cout<<"Wed"< <endl;
    }
    ""
    ""
    ""
    else {
        cout<<"Invalid day";
    }
    return 0;
}

```

#### Example of Short Circuit ####


```cpp

#include<iostream>
using namespace std;

int main() {

    int a,b,c;
    cout<<"Enter 3 no's ";
    cin>>a>>b>>c;
    if(a>b && a>c) {
        cout<<"a"<<endl;
    }
    return 0;
}

```
In the above exmaple if we used `&&` - `AND` operator where both the condtions sholud be true to enter inside the for loop, but here while checking this condtion there is possibility of Short circuit i.e while execting this condition `a>b && a>c` the program first check the first condtion i.e `a>b` here if we get false then the program will not execute the next condtion i.e `a>c` it automatically skip...   


#### Example of Dynamic Declartion ####

```cpp

#include<iostream>
using namespace std;

int main() {

    int a =10, b=5;

    if(int c =a+b;c>10) {
        cout<<c<<endl;
    }
    return 0;
}

```

Here the variable `c` is declared in if condition,where it's scope is within if condition 

#### Switch case Skeleton  ####

```cpp

#include<iostream>
using namespace std;

int main() {

    Switch(expression) {
        case 1: ______
                breark;
         case 2: ______
                breark;  
                ""
                ""
        default: ______             
    }
    return 0;
}

```

#### Loops ####

In C++ we have `while loop`, `for loop`, `do while loop`, `nested loop`

##### while loop #####

```cpp

#include<iostream>
using namespace std;

int main() {

   int a = 10;
   while( a < 20 ) {
      cout << "value of a: " << a << endl;
      a++;
    return 0;
}

```

##### for loop #####

```cpp

#include<iostream>
using namespace std;

int main() {

   for( int a = 10; a < 20; a = a + 1 ) {
      cout << "value of a: " << a <<endl;
   }
    return 0;
}

```

##### do while loop #####

```cpp

#include<iostream>
using namespace std;

int main() {

  int a = 10;
   do {
      cout << "value of a: " << a << endl;
      a = a + 1;
   } while( a < 20 );
    return 0;
}

```

```cpp

#include<iostream>
using namespace std;

int main() {

   int i, j;
   for(i = 2; i<100; i++) {
      for(j = 2; j <= (i/j); j++)
         if(!(i%j)) break; // this can be used if you have only one line after in if statement
         if(j > (i/j)) cout << i << " is prime\n";
   }
    return 0;
}

```

#### Arrays ####

#### Pointers ####

#### Functions ####