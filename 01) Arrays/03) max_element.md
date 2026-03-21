# Find Maximum Element in an Array

## Problem
Scan an array of size n and print the maximum element.

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
  int max=arr[0];
  for(int i=1;i<n;i++){
    if(max<arr[i]){
      max=arr[i];
    }
  }
  printf("Max Element is: %d",max);
  return 0;
}
