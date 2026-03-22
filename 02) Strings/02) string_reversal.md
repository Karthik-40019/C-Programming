# Reverse a String
## 1. Using Character Swapping
```c
#include<stdio.h>
int main(){
  char str[100];
  
  gets(str);
  int size=0;
  int k=0;
  while(str[k] != '\0'){
    size++;
    k++;
  }

  for(int i=0,j=size-1;i<=j;i++,j--){
    char temp = str[i];
    str[i] = str[j];
    str[j] = temp;
  }
  puts(str);
}
```
## 2. Reverse Printing
```c
#include<stdio.h>
int main(){
  char str[100];
  
  scanf("%[^\n]s",str);
  int size=0;
  int k=0;
  while(str[k] != '\0'){
    size++;
    k++;
  }
  for(int i=size-1; i>=0; i--){
    printf("%c",str[i]);
  }
  return 0;
}
```
Note: "%[^\n]s" is basically used to scan full string. But this is not clear approach to scan any string.

## 3. Recursion
```c
#include<stdio.h>

void reverse(char str[],int i){
  if(str[i] == '\0') return;
  reverse(str, i+1);
  printf("%c", str[i]);
}

int main(){
  char str[100];
  gets(str);
  
  reverse(str, 0);
  return 0;
}
```
