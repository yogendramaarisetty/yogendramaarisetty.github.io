
# 1-D


An array is a sequential collection of elements of same data type and stores data elements in a continuous memory location. The elements of an array are accessed by using an index. The index of an array of size N can range from  0  to  N−1. For example, if your array size is  5, then your index will range from 0 to 4 (5-1). Each element of an array can be accessed by using  arr[index].

Consider following array. The size of this array is  5. If you want to access  12, then you can access it by using arr[ 1 ] i.e.  12.

![enter image description here](https://he-s3.s3.amazonaws.com/media/uploads/58ceb07.png)

**Array declaration**

Declaring an array is language-specific.

For example, in C/C++, to declare an array, you must specify, the following:

-   Size of the array: This defines the number of elements that can be stored in the array.
    
-   Type of array: This defines the type of each element i.e. number, character, or any other data type.
    

A C++ example would be:

```cpp
int arr[5];
```

This is a static array and the other kind is dynamic array, where type is just enough for declaration. In dynamic arrays, size increases as more elements are added to the array.

**Array Initialization:**

Array can be initialized either at the time of declaration or after that.

The sample format if an array is initialized at the time of declaration is

```cpp
type arr[size] = {elements}
```

The sample format of an array that is initialized in C++, is

```cpp
int arr[5] = {4, 12, 7, 15, 9};
```

An array can be initialized after declaration by assigning values to each index of the array as follows

```cpp
 type arr[size]
 arr[index] = 12
```

C++ example:

```cpp
int arr[5];
arr[0] = 4;
arr[1] = 12;
```

**Processing an Array:**

The most basic form of processing an array is to loop over the array and print all its elements.

A sample of processing an array by looping over the array and printing its elements is as follows:

```cpp
type arr[size] = {elements}
for idx from 0 to size
    print arr[idx]
```

C++ example:

```cpp
#include <iostream>
using namespace std;

int main()
{
    // Array declaration and initialization
    int arr[5] = {4, 12, 7, 15, 9};
    // Iterate over the array
    for(int idx=0; idx<5; idx++)
    {
        // Print out each element in a new line
        cout << arr[idx] << endl;
    }
    return 0;
}
```


# 1-D


An array is a sequential collection of elements of same data type and stores data elements in a continuous memory location. The elements of an array are accessed by using an index. The index of an array of size N can range from  0  to  N−1. For example, if your array size is  5, then your index will range from 0 to 4 (5-1). Each element of an array can be accessed by using  arr[index].

Consider following array. The size of this array is  5. If you want to access  12, then you can access it by using arr[ 1 ] i.e.  12.

![enter image description here](https://he-s3.s3.amazonaws.com/media/uploads/58ceb07.png)

**Array declaration**

Declaring an array is language-specific.

For example, in C/C++, to declare an array, you must specify, the following:

-   Size of the array: This defines the number of elements that can be stored in the array.
    
-   Type of array: This defines the type of each element i.e. number, character, or any other data type.
    

A C++ example would be:

```cpp
int arr[5];
```

This is a static array and the other kind is dynamic array, where type is just enough for declaration. In dynamic arrays, size increases as more elements are added to the array.

**Array Initialization:**

Array can be initialized either at the time of declaration or after that.

The sample format if an array is initialized at the time of declaration is

```cpp
type arr[size] = {elements}
```

The sample format of an array that is initialized in C++, is

```cpp
int arr[5] = {4, 12, 7, 15, 9};
```

An array can be initialized after declaration by assigning values to each index of the array as follows

```cpp
 type arr[size]
 arr[index] = 12
```

C++ example:

```cpp
int arr[5];
arr[0] = 4;
arr[1] = 12;
```

**Processing an Array:**

The most basic form of processing an array is to loop over the array and print all its elements.

A sample of processing an array by looping over the array and printing its elements is as follows:

```cpp
type arr[size] = {elements}
for idx from 0 to size
    print arr[idx]
```

C++ example:

```cpp
#include <iostream>
using namespace std;

int main()
{
    // Array declaration and initialization
    int arr[5] = {4, 12, 7, 15, 9};
    // Iterate over the array
    for(int idx=0; idx<5; idx++)
    {
        // Print out each element in a new line
        cout << arr[idx] << endl;
    }
    return 0;
}
```

# Multi-dimensional


A multi-dimensional  **array**  is an array of arrays. 2-dimensional arrays are the most commonly used. They are used to store data in a tabular manner.

Consider following 2D array, which is of the size  3×5. For an array of size  N×M, the rows and columns are numbered from  0  to  N−1  and columns are numbered from  0  to  M−1, respectively. Any element of the array can be accessed by  arr[i][j]  where  0≤i<N  and  0≤j<M. For example, in the following array, the value stored at  arr[1][3]  is  14.

![enter image description here](https://he-s3.s3.amazonaws.com/media/uploads/873c255.png)

**2D array declaration:**

To declare a 2D array, you must specify the following:  
Row-size: Defines the number of rows  
Column-size: Defines the number of columns  
Type of array: Defines the type of elements to be stored in the array i.e. either a number, character, or other such datatype. A sample form of declaration is as follows:

```cpp
type arr[row_size][column_size]
```

A sample C++ array is declared as follows:

```cpp
int arr[3][5];
```

**2D array initialization:**  
An array can either be initialized during or after declaration. The format of initializing an array during declaration is as follows:

```cpp
type arr[row_size][column_size] = {{elements}, {elements} ... }
```

An example in C++ is given below:

```cpp
int arr[3][5] = {{5, 12, 17, 9, 3}, {13, 4, 8, 14, 1}, {9, 6, 3, 7, 21}};
```

Initializing an array after declaration can be done by assigning values to each cell of 2D array, as follows.

```cpp
type arr[row_size][column_size]
arr[i][j] = 14
```

A C++ example of initializing an array after declaration by assigning values to each cell of a 2D array is as follows:

```cpp
int arr[3][5];
arr[0][0] = 5;
arr[1][3] = 14;
```

This is quite naive and not usually used. Instead, the array elements are read from STDIN.

**Processing 2D arrays:**  
The most basic form of processing is to loop over the array and print all its elements, which can be done as follows:

```cpp
type arr[row_size][column_size] = {{elements}, {elements} ... }
for i from 0 to row_size
    for j from 0 to column_size
        print arr[i][j]
```

A C++ example of looping over the array and printing all its elements is as follows:

```cpp
#include <iostream>
using namespace std;

int main()
{
    // Array declaration and initialization
    int arr[3][5] = {{5, 12, 17, 9, 3}, {13, 4, 8, 14, 1}, {9, 6, 3, 7, 21}};
    // Iterate over the array
    for(int i=0; i<3; i++)
    {
        for(int j=0; j<5; j++)
        {
            // Print out each element
            cout << arr[i][j];
        }
        // Print new line character after the row is printed in above loop
        cout << endl;
    }
    return 0;
}
```