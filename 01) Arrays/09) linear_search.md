# Implement Linear Search

## Problem
Scan an array of size n and search for a given key using linear search.

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
  int key;
  scanf("%d",&key);

  int found=1;
  for(int i=1;i<n;i++){
    if(arr[i]==key){
      printf("Key found at index %d",i);
      found=0;
      break;
    }
  }
  if(found){
    printf("Key not found");
  }
  return 0;
}
