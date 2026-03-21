# Reverse the Given Array

## Problem
Scan an array of size n and print the elements in reverse order.

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
  for(int i=n-1;i>=0;i--){
    printf("%d ",arr[i]);
  }
  return 0;
}
