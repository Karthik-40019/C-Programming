# Check if Array is Sorted or Not

## Problem
Scan an array of size n and check whether it is sorted or not.

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
  int sorted=1;
  for(int i=1;i<n;i++){
    if(arr[i]>arr[i-1]){
      continue;
    }else{
      printf("Array is not sorted");
      sorted=0;
    }
  }
  if(sorted){
    printf("Array is sorted");
  }
  return 0;
}
