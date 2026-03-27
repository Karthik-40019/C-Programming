# Predict the output of the following code snippets.
# 1. Increment/Decrement
Code: 1
```c
#include<stdio.h>
int main(){
    int i = 5;
    printf("%d", i++);
    return 0;
}
```
```c
Output: 5
```
Explanation: Post-increment (i++) returns the current value first, then increments the variable.
<br>
<br>
Code: 2
```c
#include<stdio.h>
int main(){
    int i = 5;
    printf("%d", ++i);
    return 0;
}
```
```c
Output: 6
```
Explanation: Pre-increment (++i) increments the variable first, then prints the value. 
<br>
<br>
Code: 3
```c
#include<stdio.h>
int main(){
    int i = 5;
    int j = i++;
    printf("%d %d", i, j);
    return 0;
}
```
```c
Output: 6 5
```
<br>

Code: 4
```c
#include<stdio.h>
int main(){
    int i = 5;
    int j = ++i;
    printf("%d %d", i, j);
    return 0;
}
```
```c
Output: 6 6
```
<br>

Code: 5
```c
#include<stdio.h>
int main(){
    int i = 5;
    printf("%d %d", i++, i);
    return 0;
}
```
```c
Output: 5 6
```
<br>

Code 6:
```c
#include<stdio.h>
int main(){
    int i = 1;
    i = i + 1;
    printf("%d", i);
    return 0;
}
```
```c
Output: 2
```
<br>

Code: 7
```c
#include<stdio.h>
int main(){
    int i = 10;
    printf("%d", i--);
    return 0;
}
```
```c
Output: 10
```
<br>

Code: 8
```c
#include<stdio.h>
int main(){
    int i = 10;
    int j = i--;
    printf("%d %d", i, j);
    return 0;
}
```
```c
Output: 9 10
```
<br>

Code 9:
```c
#include<stdio.h>
int main(){
    int i = 6;
    int j = i++ + ++i;
    printf("%d", j);
    return 0;
}
```
```c
Output: 14
```
Explanation: The expression is i++ (+) ++i  <br>
Step 1: i++ uses current value of i.e i=6 then increments to 7 <br>
Step 2: ++i will increment current value i.e 7 to 8 <br>
Step 3: Perform j = 6+8 = 14 
<br>
<br>
Code: 10
```c
#include<stdio.h>
int main(){
    int i = 3;
    int j = i++ + i++;
    printf("%d", j);
    return 0;
}
```
```c
Output: 7
```
<br>

## 2. Operator Precedence
Priority Order: <br>
1. ( ) <br>
2. ++, -- (Pre/Post Increment & Decrement) <br>
3. *, /, % <br>
4. +, - <br>
5. <, <=, >, >= <br>
6. ==, != <br>
7. && <br>
8. || <br>
9. = <br>

If we face operators with same precedence, then we will solve it from Left to Right. <br>

Code: 11
```c
#include<stdio.h>
int main(){
    int x = 2 + 3 * 4;
    printf("%d", x);
    return 0;
}
```
```c
Output: 14
```
<br>

Code: 12
```c
#include<stdio.h>
int main(){
    int x = 10 - 5 + 2;
    printf("%d", x);
    return 0;
}
```
```c
Output: 7
```
<br>

Code: 13
```c
#include<stdio.h>
int main(){
    int x = 2 * 3 + 4 * 5;
    printf("%d", x);
    return 0;
}
```
```c
Output: 26
```
<br>

Code: 14
```c
#include<stdio.h>
int main(){
    int x = 20 / 5 * 2;
    printf("%d", x);
    return 0;
}
```
```c
Output: 8
```
<br>

Code: 15
```c
#include<stdio.h>
int main(){
    int x = 10 > 5 + 2;
    printf("%d", x);
    return 0;
}
```
```c
Output: 1
```
<br>

Code: 16
```c
#include<stdio.h>
int main(){
    int x = 10 > 5 && 2 < 3;
    printf("%d", x);
    return 0;
}
```
```c
Output: 1
```
<br>

Code: 17
```c
#include<stdio.h>
int main(){
   int x = 5 + 3 > 6 && 2 * 2 == 4;
   printf("%d", x);
    return 0;
}
```
```c
Output: 1
```
<br>

Code: 18
```c
#include<stdio.h>
int main(){
   int x = 5 + (3 > 6 && 2 * 2) == 4;
   printf("%d", x);
    return 0;
}
```
```c
Output: 0
```
<br>

Code: 19
```c
#include<stdio.h>
int main(){
   int x = 10 || 0 && 5;
   printf("%d", x);
    return 0;
}
```
```c
Ouput: 1
```
Note: Logical AND (&&) and Logical OR (||) are same as AND gate and OR gate that we studied in Digital electronics. So, it follows same truth table. <br>

Code: 20
```c
#include<stdio.h>
int main(){
   int x = (10 || 0) && 5;
   printf("%d", x);
    return 0;
}
```
```c
Output: 1
```
<br>

Code: 21
```c
#include<stdio.h>
int main(){
   int x = 5 + (2 > 3 ? 10 : 20);
   printf("%d", x);
    return 0;
}
```
```c
Output: 25
```
<br>

## 3. Pointers (Basic)
Code: 22
```c
#include <stdio.h>
int main()
{
  int a = 10;
  int *p = &a;
  printf("%d", *p);
}
```
```
Output: 10
```
<br>

Code: 23
```c
#include <stdio.h>
int main()
{
  int a = 10;
  int *p = &a;
  *p = 20;
  printf("%d", a);
}
```
```
Output: 20
```
<br>

Code: 24
```c
#include <stdio.h>
int main()
{
  int a = 10;
  int *p = &a;
  printf("%p %d", p, *p);
}
```
```
Output: (Some address) 10
```
<br>

Code: 25
```c
#include <stdio.h>
int main()
{
  int a = 10;
  int *p = &a;
  int *q = p;
  *q = 60;
  printf("%d", a);
}
```
```
Ouput: 60
```
<br>

Code: 26
```c
#include <stdio.h>
int main()
{
  int a = 5, b = 10;
  int *p = &a;
  p = &b;
  printf("%d", *p);
}
```
```
Output: 10
```
<br>

Code: 27
```c
#include <stdio.h>
int main()
{
  int a = 10;
  int *p = &a;
  int **q = &p;
  printf("%d", **q);
}
```
```
Output: 10
```
`**q` is two levels dereference <br>
 `q`  -> Stores address of `p` <br>
`*q`  -> gives p <br>
`**q` -> gives value of a <br>

<br>

Code: 28
```c
#include <stdio.h>
int main()
{
  int a = 5;
  int *p = &a;
  printf("%d ", (*p)++);
  printf("%d", a);
}
```
```
Output: 5 6
```
<br>

Code: 29
```c
#include <stdio.h>
int main()
{
  int a = 5;
  int *p = &a;
  printf("%d ", ++(*p));
  printf("%d", a);
}
```
```
Output: 6 6
```
<br>

Code: 30
```c
#include <stdio.h>
int main()
{
  int a = 5;
  int *p = &a;
  printf("%d ", (*p)+5);
}
```
```
Output: 10
```
<br>

Code: 31
```c
#include<stdio.h>
int main(){
  int a = 10;
  int *p = &a;
  printf("%d", *(p + 1));
  return 0;
}
```
```
Output: Undefined Behaviour
```
<br>

Code: 32
```c
#include<stdio.h>
int main(){
  int arr[] = {1, 2, 3};
  int *p = arr;
  printf("%d", *(p + 2));
  return 0;
}
```
```
Output: 3
```
<br>

Code: 33
```c
#include<stdio.h>
int main(){
  int arr[] = {10,20,30};
  int* p = arr;
  p++;
  printf("%d", *p);
  return 0;
}
```
```
Output: 20
```
Initial pointer will be at 0 and it goes to 1 after `p++`
<br>
<br>
Code: 34
```c
#include<stdio.h>
int main(){
  int arr[] = {10,20,30};
  int* p = arr;
  printf("%d", *p++);
  return 0;
}
```
```
Output: 10
```
According to the operator precedence rule, Post increment will first use the value then it will increment it.







