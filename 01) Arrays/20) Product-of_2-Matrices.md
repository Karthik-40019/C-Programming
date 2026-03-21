# Perform Product of 2 Matrices

## Problem
Scan two matrices and print their product if multiplication is possible.

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

  if(c1!=r2){
    printf("Multiplication is not possible");
  }

  int mat2[r2][c2];
  for(int i=0;i<r2;i++){
    for(int j=0;j<c2;j++){
      scanf("%d",&mat2[i][j]);
    }
  }

  for(int i=0;i<r1;i++){
    for(int j=0;j<c2;j++){
      int sum=0;

      for(int k=0;k<c1;k++){
        sum+=mat1[i][k]*mat2[k][j];
      }
      printf("%d ",sum);
    }
    printf("\n");
  }
  return 0;
}
