# Perform Left Rotate by K Positions on the Given Array

## Problem
Scan an array of size n and perform left rotation by k positions.

## Code (C)
```c
#include<stdio.h>

void display(int arr[],int n){
  for(int i=0;i<n;i++){
    printf("%d ",arr[i]);
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

  int k;
  scanf("%d",&k);

  for(int x=1;x<=k;x++){
    int temp=arr[0];
    for(int i=1;i<n;i++){
      arr[i-1]=arr[i];
    }
    arr[n-1]=temp;
    printf("Array after %dst rotation: ",x);
    display(arr,n);
  }
  return 0;
}
