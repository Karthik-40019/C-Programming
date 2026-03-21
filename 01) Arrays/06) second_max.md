# Print the Second Largest Element in the Array

## Problem
Scan an array of size n and print the second largest element.

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
  int smax=-1;

  for(int i=1;i<n;i++){
    if(arr[i]>max){
      smax=max;
      max=arr[i];
    }
    else if(arr[i]>smax && arr[i]!=max){
      smax=arr[i];
    }
  }
  printf("%d ",smax);
  return 0;
}
