# Remove Duplicates from Given Array

## Problem
Scan an array of size n and print elements after removing duplicates.

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
  int visited[100]={0};
  for(int i=0;i<n;i++){
    if(visited[arr[i]]==0){
      printf("%d ",arr[i]);
      visited[arr[i]]=1;
    }
  }
  return 0;
}
