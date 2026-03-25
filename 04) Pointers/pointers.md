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
👉 `%p` is a format specifier specifically used to print memory addresses, usually represented in hexadecimal form. <br>
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
👉 `int*` declares a pointer that holds the memory address of an int type variable.

<p align="center">
  <img src="images/pointer.png" width="400">
</p>
<br>

## Modifying a Value Using a Pointer
```c
#include<stdio.h> 
int main(){ 
  int a = 5; 
  int* ptr = &a; 
  *ptr = 7; 
  printf("%d", a); 
  return 0; 
}
```
```
Output: 7
```
👉 Using `*ptr`, the value at the stored address is modified, updating `a` from `5` to `7`.
<br>
<br>

## Swap 2 numbers using pointers
```c
#include<stdio.h>
void swap(int* x,int* y){
  int temp = *x;
  *x = *y;
  *y = temp;
  return;
}
int main(){
  int a = 2;
  int b = 9;
  
  swap(&a, &b);
  printf("Value of a: %d\n",a);
  printf("Value of b: %d",b);
  return 0;
}
```
```
Output:
Value of a: 9
Value of b: 2
```
<p align="center">
  <img src="images/swap.png" width="700"><br>
  <b>Pointer Value Update Representation</b>
</p>
