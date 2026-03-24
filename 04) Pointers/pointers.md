# Pointers in C
A pointer is a variable that holds the memory address of another variable.
<br>

## Printing the Value
```c
#include<stdio.h>
int main(){
  int a = 5;
  printf("%d", a);
  return 0;
}
```
```
Output: 5
```
## Printing the Address
```c
#include<stdio.h>
int main(){
  int a = 5;
  printf("%p", &a);
  return 0;
}
```
```
Output: 0x7ffef4883dd4
```
👉 %p is a format specifier specifically used to print memory addresses, usually represented in hexadecimal form. <br>
Note: The address that is there above will change everytime, as computer allocates a random address everytime. <br>


## Storing address 
```c
#include<stdio.h>
int main(){
  int a = 5;
  int* ptr = &a;
  printf("%p\n", &a);
  printf("%p", ptr);
  return 0;
}
```
```
Output:
0x7ffeca38529c
0x7ffeca38529c
```
👉 int* declares a pointer that holds the memory address of an int type variable.
