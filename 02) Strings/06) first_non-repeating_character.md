# First Non-Repeating Character
```c
#include<stdio.h>
int main(){
  char str[100];
  gets(str);

  int freq[256]={0};
  for(int i=0; str[i]!='\0'; i++){
    freq[str[i]]++;
  }
  for(int i=0; str[i]!='\0';i++){
    if(freq[str[i]]==1){
      printf("%c",str[i]);
      break;
    }
  }
  return 0;
}
```
```c
Input: aabbcdde
Output: c
```
