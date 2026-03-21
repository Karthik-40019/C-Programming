# Perform Addition of 2 Matrices

## Problem
Scan two matrices and print their addition if dimensions are equal.

## Code (C)
```c
#include<stdio.h>
int main(){
  int r1,c1;
  scanf("%d %d",&r1,&c1);

  int mat1[r1][c1];
  for(int i=0;i<r1;i++){
    for(int j=0;j<c1;j++){
      scanf("%d",&mat1[i][j]);
    }
  }

  int r2,c2;
  scanf("%d %d",&r2,&c2);

  if(r1!=r2 || c1!=c2){
    printf("Addition not possible");
  }

  int mat2[r2][c2];
  for(int i=0;i<r2;i++){
    for(int j=0;j<c2;j++){
      scanf("%d",&mat2[i][j]);
    }
  }

  int sum=0;
  for(int i=0;i<r1;i++){
    for(int j=0;j<c1;j++){
      sum=mat1[i][j]+mat2[i][j];
      printf("%d ",sum);
    }
    printf("\n");
  }
}
