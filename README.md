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
      cout << "value of a is : " << a <<endl;
   }
    return 0;
}

```

```cpp

#include<iostream>
using namespace std;

int main() {

    int a[5] = {1,2,3,4,5}
   for( auto c: a) {
      cout << "value of a is: " << c <<endl;
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

##### Nested loop #####

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

#### Arrays  ####

`collection of items stored at contiguous memory locations`


1. Linear Search

A linear search scans one item at a time, without jumping to any item .

The worst case `complexity is  O(n)`, sometimes known an O(n) search
Time taken to search elements keep increasing as the number of elements are increased.

2. Binary Search 

`Condition`: To use Binary Search, the element in the array must me sorted order
binary search cut down your search to half as soon as you find middle of a sorted list.
The middle element is looked to check if it is greater than or less than the value to be searched.
Accordingly, search is done to either half of the given list `complexity is  O(log n)`

##### Linear Search Example #####

```cpp
#include<iostream>
using namespace std;

int main() {

   int a[5] = {6,7,23,45,23};
   int key;
   cout<< "Enter the Key Search";
   cin>>key;

   for(int i=0;i<10;i++>) {
       if(key == a[i]) {
           cout<<"Elemnt found at "<<i;
           exit(0);
       }
   }
   cout<<"Key Elemnt not found";
    return 0;
}

```

##### Binary Search Example #####

```cpp
#include<iostream>
using namespace std;

int main() {

   int a[5] = {6,7,23,45,23};
   int l=0,h=4,key,mid;
   cout<< "Enter the Key Search";
   cin>>key;
    while (l<=h) {
        mid = (l+h)/2;
        if (key == a[mid]) {
            cout<<"Element found at "<<mid;
            exit(0);
        } else if (key < a[mid]) {
            h = mid -1;
        } else {
            l = mid + 1;
        }
    }
   cout<<"Key Elemnt not found";
    return 0;
}

```

#### Pointers ####

`pointer is used to store the address of the varible`

Variable --->  1. data variable
               2. Address varibale

Declaration     : int *p
Initialization  : p
Dereferencing   : cout<<*p

Value    |  Address       
---------|-------------|
10       |  200/201    | 
200      |  300/301    |

```cpp

 int x = 10  // data varibale
 int *p      // Address varibale
 p= &x;
 
cout<<x;     // 10

cout<<&x;    // 200

cout<<p;     // 200

cout<<&p;   // 300

cout<<*p;   // 10

```
pointer Arithmetic

```cpp
int a[5] = {2,5,6,8,1};   // address start from 200
int *p =a;
int *q = &a[3]

p++    //  202

p--    // 198

p+=2     // 200

p=-2   // 300

d =p-q  // 200 - 208

```
Problems while using Pointers

1. Uninitialized Pointer
2. Memory leak
3. Dangling Pointer
 
#### Reference Example ####

```cpp
#include<iostream>
using namespace std;

int main() {
    int x=10;
    int &y=x;

    y++;
    x++;
    cout<<x<<endl; // 12
    cout<<y<<endl; // 12  
    return 0;
} 

```

#### Pointer to Function Example ####

```cpp
#include<iostream>
using namespace std;

void display() { // function
    cout<<"Hello";
}
int main() {

    void (*fp)();  // declaration
    fp=display;    // initializiton
    (*fp)();       // calling function
    return 0;
}

```

#### Functions ####

Function Overloading  means were we can write more than one function with same name but a different argument list

##### Function Overloading Example #####

```cpp
#include<iostream>
using namespace std;
int sum(int a,int b) {
    return a+b;
}

float sum(float a,float b) {
    return a+b;
}

int sum(int a,int b,int c) {
    return a,b,c;
}

int main() {
    cout<<sum(10,5)<<endl;
    cout<<sum(12.5f,3.4f)<<endl;
    cout<<sum(10,20,3)<<endl;
    return 0;
}

```

##### Function Template Example #####

1. Function template are used for defining generic functions
2. They work for multiple datatypes
3. Datatype is decided based on the type of value passed
4. Datatype is a template variable
5. Function can have multiple template variables

```cpp
#include <iostream>
using namespace std;
template<class T>
T maxim(T a,T b) {
    return a>b?a:b;
}

int main() {
cout<<maxim(12,14)<<endl;
cout<<maxim(2.3,1.4)<<endl;
cout<<maxim(2.3f,5.6f)<<endl;
return 0;

}
```

##### Function Default Arguments #####

1. Parameters of a function can have default values
2. Default values to parameters must be given from right side parameter
3. Default values to parameters must be given from right side parameter

```cpp

#include <iostream>
using namespace std;
int sum(int a,int b,int c=0) {
    return a+b+c;
}

int main() {
    cout<<sum(10,20,3)<<endl;
    return 0;
}

```

##### Parameter Passing Methods #####

1. Pass by Value
2. Pass by Address
3. Pass by Refernce

Pass-By-Value : values of Actual parameters are passed to formal parameters. Actual
parameters cannot be modified by function

###### Pass by Value Example ######

```cpp

void swap(int a, int b) {
    int temp;
    temp=a;
    a=b;
    b=temp;
}

int main() {
    int x=10, y=20;
    swap(x,y);
    cout<<x<<y;
    return 0;
}

```
Pass-By-Address: Address of Actual Parameters are passed to a function, formal
parameters must be pointers. Function can indirectly access actual parameters.

###### Pass by Address Example ######

```cpp

void swap(int *x, int *y) {
    int temp;
    temp=*x;
    *x=*y;
    *y=temp;
}

int main() {
    int a=10, b=20;
    swap(&a,&b);
    cout<<a<<b;
    return 0;
}

```

Pass-By-Reference: Actual parameters are passed as reference to formal parameters,
function can modify actual parameters.

###### Pass by Reference Example ######

```cpp

void swap(int &a, int &b) {
    int temp;
    temp=a;
    a=b;
    b=temp;
}

int main() {
    int x=10, y=20;
    swap(x,y);
    cout<<x<<y;
    return 0;
}

```
###### Return by Address ######

1. A function can return address of memory
2. It should not return address of local variables, which will be disposed after function ends
3. It can return address of memory allocated in heap

###### Return by Address Example ######

```cpp
int * fun(int n) {
    int *p=new int[n];
    for(int i=0;i<n;i++)
    p[i]=i+1;
    return p;
}

int main() {
    int *ptr=fun(5);
    for(int i=0;i<5;i++)
    cout<<i<<endl;
}

```
###### Return by Reference Example ######

```cpp
int & fun(int &a) {
    cout<<a;
    return a;
}

int main() {
    int x=10;
    fun(x)=25;
    cout<<x;
}

```

###### Oops ######

Features of OOPS
1. Abstraction
2. Encapsulation
3. Inheritance
4. Polymorphism

###### Classes ######

Class is a blue print of an object.Many object can be created from same class.Object consumes memory equal to sum of sizes of all data members.Member functions don’t occupy memory. Dot operator is used for accessing members of object.Memory allocated for object is also called as instance.

```cpp
Class Rectangle {
    public:
        int length;
        int breadth;
        int area() {
        return length*breadth;
        }

        int perimeter() {
        return 2*(length+breadth);
        }
};
```
###### Pointer to an Object ######

1. A pointer of type class can be created
2. A pointer can point on existing object
3. A new object can be created in heap using pointer
4. Arrow operator is used for accessing members of an object using pointer

Data Hiding
1. Data members of a class class are usually declared as Private or Protected,
2. They can be accessed only inside the class and child classes
3. Data finding protects data from mishandling

###### Constructors ######

1. Constructor is a member function of a class
2. It will have same name as class name
3. It will not have return type
4. Its should be public
5. It can be declared as private also in some cases
6. It is called when object is created
7. It is used for initialising an object
8. It can be overloaded
9. If its not defined then class will have a default constructor
10 .Constructor can take default arguments

Types of constructors
1. Non-argument constructor
2. Parameterised constructor
3. Copy constructor

###### All types of Member Functions ######

1. Constructors - called when object is created
2. Accessors - used for knowing the value of data members
3. Mutators - used for changing value of data member
4. Facilitator - actual functions of class
5. Enquiry - used for checking if an object satisfies some condition
6. Destructor - used for releasing resources used by object

###### Example ######

```cpp
#include<iostream>
using namespace std;
class Student {
    private:
    int roll;
    string name;
    int mathMarks;
    int phyMarks;
    int chemMarks;
    public:
    Student(int r,string n,int m,int p,int c) {
        roll=r;
        name=n;
        mathMarks=m;
        phyMarks=p;
        chemMarks=c;
    }

    int total() {
        return mathMarks+phyMarks+chemMarks;
    }

    char grade() {
        float average=total()/3;
        if(average > 60)
        return 'A';
        else if(average>=40 && average<60)
        return 'B';
        else
        return 'C';
    }
};
int main() {
    int roll;
    string name;
    int m,p,c;
    cout<<"Enter Roll number of a Student: ";
    cin>>roll;
    cout<<"Enter Name of a Student:";
    cin>>name;
    cout<<"Enter marks in 3 subjects";
    cin>>m>>p>>c;
    Student s(roll,name,m,p,c);
    cout<<"Total Marks:"<<s.total()<<endl;
    cout<<"Grade of Student:"<<s.grade()<<endl;
}
```

##### Operator Overloading #####

1. Operators can be overloaded on our classes
2. We can define operator for our own classes
3. Operators can be overloaded using member functions or friend functions
4. Global functions can also access private and protected members of an object if they are declared as friend inside a class

###### Example ######

```cpp
class Complex {
    private:
    int real;
    int img;
    public:
    Complex(int r=0,int i=0) {
    real=r;
    img=i;
    }

    void display() {
    cout<<real<<“+i”<<img<<endl;
    }

    Complex operator+(Complex c) {
    Complex temp;
    temp.real=real+c1.real;
    temp.img=img+c1.img;
    return temp;
    }
};
int main() {
    Complex c1(5,3),c2(10,5),c3;
    c3=c1+c2;
    c3.display();
}

```

##### Operator Overloading using Friend Functions #####
```cpp
#include <iostream>
using namespace std;
class Complex {
    private:
    int real;
    int img;
    public:
    Complex(int r=0,int i=0) {
    real=r;
    img=i;
    }

    void display() {
    cout<<real<<“+i”<<img<<endl;
    }

    friend Complex operator+(Complex c1,Complex c2);
};
Complex operator+(Complex c1,Complex c2) {
    Complex temp;
    temp.real=c1.real+c2.real;
    temp.img=c1.img+c2.img;
    return temp;
}

int main() {
    Complex c1(5,3),c2(10,5),c3;
    c3=c1+c2;
    c3.display();
}

```