# Count total No.of Vowels in a String
```c
#include<stdio.h>
int main(){
  char str[100];
  gets(str);
  int v=0;
  
  int size=0;
  int k=0;
  while(str[k] != '\0'){
    size++;
    k++;
  }
  for(int i=0;i<size;i++){
    char ch=str[i];
    if(ch=='a' || ch=='e' || ch=='i' || ch=='o' || ch=='u' ||
       ch=='A' || ch=='E' || ch=='I' || ch=='O' || ch=='U'){
         v++;
    }
  }
  printf("Total Vowels: %d",v);
  return 0;
}
```
