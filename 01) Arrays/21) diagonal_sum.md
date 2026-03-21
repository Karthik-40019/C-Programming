# Difference Between the Sum of Diagonals in a Matrix

## Problem
Scan a square matrix and print the difference between the sum of its primary and secondary diagonals.

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

  if(r!=c){
    printf("Not a Square Matrix");
  }

  int s1=0;
  int s2=0;
  for(int i=0;i<r;i++){
    for(int j=0;j<c;j++){
      if(i==j){
        s1+=mat[i][j];
      }
      if(i+j==r-1){
        s2+=mat[i][j];
      }
    }
  }
  printf("%d",s1-s2);
  return 0;
}
