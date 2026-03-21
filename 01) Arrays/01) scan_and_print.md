# Scan and Print the Same Array

## Problem
Scan an array of size n and print all its elements.

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
  for(int i=0;i<n;i++){
    printf("%d ",arr[i]);
  }
  return 0;
}
