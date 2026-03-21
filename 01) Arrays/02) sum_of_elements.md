# Sum of All Elements in an Array

## Problem
Scan an array of size n and print the sum of all its elements.

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
  int sum=0;
  for(int i=0;i<n;i++){
    sum+=arr[i];
  }
  printf("Sum of Elements: %d",sum);
  return 0;
}
