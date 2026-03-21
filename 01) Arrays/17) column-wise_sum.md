# Calculate and Print Column-wise Sum

## Problem
Scan a 2D array of size r x c and print the sum of each column.

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
  for(int j=0;j<c;j++){
    for(int i=0;i<r;i++){
      sum+=mat[i][j];
    }
    printf("Sum of Column %d: %d\n",j,sum);
    sum=0;
  }
  return 0;
}
