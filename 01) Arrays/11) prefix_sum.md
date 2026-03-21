# Calculate and Print the Prefix Sum Array of Given Array

## Problem
Scan an array of size n and print its prefix sum array.

## Code (C)
```c
#include<stdio.h>

void display(int prefix[],int n){
  for(int i=0;i<n;i++){
    printf("%d ",prefix[i]);
  }
  printf("\n");
}

int main(){
  int n;
  scanf("%d",&n);

  int arr[n];
  for(int i=0;i<n;i++){
    scanf("%d",&arr[i]);
  }

  int prefix[n];
  prefix[0]=arr[0];

  for(int i=1;i<n;i++){
    prefix[i]=arr[i]+prefix[i-1];
  }
  display(prefix,n);
  return 0;
}
