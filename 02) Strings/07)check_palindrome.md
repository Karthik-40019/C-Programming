# Check Palindrome
## Approach: 2 Pointers
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
  
  int i=0, j=size-1;
  int flag=1;
  while(i<j){
    if(str[i]!=str[j]){
      flag=0;
      printf("Not a Palindrome");
      break;
    }
    i++;
    j--;
  }
  if(flag){
    printf("Palindrome");
  }
  return 0;
}
```
