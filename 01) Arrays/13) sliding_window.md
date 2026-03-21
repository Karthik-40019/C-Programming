# Compute the Maximum Subarray Sum of Size K Using Sliding Window

## Problem
Scan an array of size n and compute the maximum sum of subarray of size k using sliding window.

## Code (C)
```c
#include<stdio.h>

int max(int a,int b){
  return (a>b) ? a : b;
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

  int sum=0;
  for(int i=0;i<k;i++){
    sum+=arr[i];
  }

  int Max=sum;
  for(int i=k;i<n;i++){
    sum=sum+(arr[i]-arr[i-k]);
    Max=max(Max,sum);
  }

  printf("Maximum sum of size %d = %d",k,Max);
  return 0;
}
