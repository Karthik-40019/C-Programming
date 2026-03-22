# Remove Duplicates
## Approach Used: Frequency array 
```c
#include<stdio.h>
int main(){
  char str[100];
  gets(str);

  int freq[256]={0};
  for(int i=0; str[i]!='\0'; i++){
    if(freq[str[i]]==0 && str[i]!='\n'){
      printf("%c",str[i]);
      freq[str[i]]++;
    }
  }
  return 0;
}
```
