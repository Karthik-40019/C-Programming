# Calculate the Sum of Matrix

## Problem
Scan a 2D array of size r x c and print the sum of all its elements.

## Code (C)
```c
#include<stdio.h>
int main(){
  int r,c;
  scanf("%d %d",&r,&c);

  int mat[r][c];
  for(int i=0;i<r;i++){
    for(int j=0;j<c;j++){
      scanf("%d",&mat[i][j]);
    }
  }

  int sum=0;
  for(int i=0;i<r;i++){
    for(int j=0;j<c;j++){
      sum+=mat[i][j];
    }
  }
  printf("%d",sum);
  return 0;
}
