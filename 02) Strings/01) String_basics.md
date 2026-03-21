# String Input and Printing Variations

## 1. Printing a string by iterating over each character.
```c
#include<stdio.h>
int main() {
  char arr[]={'H', 'E', 'L', 'L', 'O'};
  for(int i=0; i<5; i++){
    printf("%c", arr[i]);
  }
  return 0;
}
```
## 2. Printing a string stored as a string literal.
```c
#include<stdio.h>
int main() {
  char arr[] = "Hello";
  for(int i=0; i<5; i++){
    printf("%c", arr[i]);
  }
  return 0;
}
```
## 3. Traversing and printing a string until the null character.
```c
#include<stdio.h>
int main() {
  char arr[] = "Hello\0";
  
  int i = 0;
  while(arr[i] != '\0'){
    printf("%c", arr[i]);
    i++;
  }
  return 0;
}
```
Note: Even if we don’t explicitly add '\0', the compiler automatically appends it at the end of a string literal, so no error occurs.

## 4. Accessing individual characters of a string.
```c
#include<stdio.h>
int main() {
  char arr[] = "Hello\0";
  
  printf("%c\n", arr[0]);
  printf("%c\n", arr[1]);
  printf("%c\n", arr[2]);
  printf("%c\n", arr[3]);
  printf("%c\n", arr[4]);
  return 0;
}
```
## 5. Modifying the characters.
```c
#include<stdio.h>
int main() {
  char str[] = "Hello World\0";
  
  str[0] = 'M';
  str[7] = 'K';
  
  int i = 0;
  while(str[i] != '\0'){
    printf("%c", str[i]);
    i++;
  }
  return 0;
}

//Mello WKrld
```
Note: While printing we can use either str[i] or i[str] because, str[i] = *(str + i) and i[str] = *(i + str). Since addition is commutative it will give us the same output.

## 6. Printing a string using 4 different methods.
```c
#include<stdio.h>
int main() {
  char str[] = "Hello World\0";

  int i;
  
  //Method 1
  i=0;
  while(str[i] != '\0'){
    printf("%c", str[i]);
    i++;
  }
  printf("\n");
  
  //Method 2
  i=0;
  while(str[i] != '\0'){
    printf("%c", *(str+i));
    i++;
  }
  printf("\n");
  
  //Method 3
  i=0;
  while(str[i] != '\0'){
    printf("%c", i[str]);
    i++;
  }
  printf("\n");
  
  //Method 4
  i=0;
  while(str[i] != '\0'){
    printf("%c", *(i+str));
    i++;
  }
  return 0;
}

```
The above code will print "Hello World" 4 times in a new line.
<br>

Note: Strings initialized using string literals are automatically null-terminated ('\0'). However, when characters are initialized individually, the null terminator is not added automatically, so it must be included manually.

## 7. Use puts() function and print the string.
```c
#include<stdio.h>

int main() {
  char str[] = "Hello World\0";
  puts(str);
  return 0;
}
```
## 8. Use scanf() and then print the string.
```c
#include<stdio.h>

int main() {
  char str[20];
  scanf("%s", str); // scans only the fist word --> Limitation
  printf("%s", str);
  return 0;
}
```
```c
Input: Karthik practicing C
Output: Karthik
```
## 9. Then use gets() to scan full string.
```c
#include<stdio.h>

int main() {
  char str[20];
  gets(str); //reads full string
  puts(str);
  return 0;
}
```
```c
Input: Karthik practicing C
Output: Karthik practicing C
```
