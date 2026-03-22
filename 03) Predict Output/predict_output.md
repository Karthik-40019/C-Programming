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
<br>

