# Find the First Occurrence and Last Occurrence of the Given Element in the Array

## Problem
Scan an array of size n and find the first and last occurrence of a given element.

## Code (C)
```c
#include<stdio.h>
int main(){
  int n;
  scanf("%d",&n);

  int arr[n];
  for(int i=0;i<n;i++){
    scanf("%d",&arr[i]);
  }

  int k;
  scanf("%d",&k);

  int n1=0;
  int n2=n-1;

  int found=0;
  while(n1<n){
    if(arr[n1]!=k){
      n1++;
    }else{
      printf("First occurrence at %d index\n",n1);
      found=1;
      break;
    }
  }

  while(n2>=0){
    if(arr[n2]!=k){
      n2--;
    }else{
      printf(" Last occurrence at %d index",n2);
      found=1;
      break;
    }
  }

  if(!found){
    printf("Key Not Found");
  }
  return 0;
}
