# Check Anagram
```c
#include<stdio.h>
int main(){
  char s1[100];
  char s2[100];
  
  gets(s1);
  gets(s2);
  
  int freq[256]={0};
  for(int i=0; s1[i]!='\0'; i++){
    if(s1[i] !='\n'){
      freq[s1[i]]++;
    }
  }
  for(int i=0; s2[i]!='\0'; i++){
    if(s2[i] !='\n'){
      freq[s2[i]]--;
    }
  }
  for(int i=0;i<256;i++){
    if(freq[i] != 0){
      printf("Not an Anagram");
    }
  }
  printf("Anagram");
  return 0;
}
```
👉 Two strings are called anagrams if:
<br>
1.They contain the same characters <br>
2. With the same frequency <br>
3. But possibly in a different order

```c
Input s1: listen
      s2: silent
Output: Anagram
```
