# Count Number of Even and Odd Elements in an Array

## Problem
Scan an array of size n and count the number of even and odd elements.

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
  int even,odd;
  even=odd=0;
  for(int i=0;i<n;i++){
    if(arr[i]%2==0){
      even++;
    }else{
      odd++;
    }
  }
  printf("No.of Even numbers: %d\n",even);
  printf("No.of Odd numbers: %d",odd);
  return 0;
}
