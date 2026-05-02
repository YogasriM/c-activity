# c-activity
## Yogasri M
## 212224220124

## 1. Write a c program to print all prime numbers between two limits.
```
#include <stdio.h>

int main() {
    int start, end, i, j, isPrime;

    printf("Enter the starting limit: ");
    scanf("%d", &start);

    printf("Enter the ending limit: ");
    scanf("%d", &end);

    printf("Prime numbers between %d and %d are:\n", start, end);

    for(i = start; i <= end; i++) {
        if(i <= 1)
            continue;  

        isPrime = 1;  

        for(j = 2; j <= i / 2; j++) {
            if(i % j == 0) {
                isPrime = 0; 
                break;
            }
        }

        if(isPrime == 1)
            printf("%d ", i);
    }

    return 0;
}
```
## output
<img width="798" height="339" alt="image" src="https://github.com/user-attachments/assets/f81b7531-f97d-4195-a488-2a9414ad02f1" />

## 2. Write a c program to count the number of digits in a number.
```
#include <stdio.h>

int main() {
    int num, count = 0;

    printf("Enter a number: ");
    scanf("%d", &num);

  
    if(num == 0) {
        count = 1;
    } else {
      
        if(num < 0)
            num = -num;

        while(num > 0) {
            num = num / 10;  
            count++;
        }
    }

    printf("Number of digits = %d", count);

    return 0;
}
```
## output
<img width="838" height="362" alt="image" src="https://github.com/user-attachments/assets/73c41593-48f1-4833-bf59-b7aa4b904b22" />

## 3. Write a c program to print the alphabet S in n x n matrix.
```
#include <stdio.h>

int main() {
    int n, i, j;

    printf("Enter the value of n: ");
    scanf("%d", &n);

    for(i = 0; i < n; i++) {
        for(j = 0; j < n; j++) {

           
            if(i == 0 || i == n/2 || i == n-1 || 
               (j == 0 && i < n/2) || 
               (j == n-1 && i > n/2)) {
                printf("* ");
            } else {
                printf("  ");
            }
        }
        printf("\n");
    }

    return 0;
}
```
## output
<img width="611" height="394" alt="image" src="https://github.com/user-attachments/assets/4d0fbf3b-cf3a-4f83-bfb4-2c7aaad82aa4" />

## 4. Write a c program to print the pyramid pattern.

```
#include <stdio.h>

int main() {
    int n, i, j;

    printf("Enter number of rows: ");
    scanf("%d", &n);

    for(i = 1; i <= n; i++) {

      
        for(j = 1; j <= n - i; j++) {
            printf(" ");
        }

        for(j = 1; j <= (2 * i - 1); j++) {
            printf("*");
        }

        printf("\n");
    }

    return 0;
}
```
## output
<img width="802" height="363" alt="image" src="https://github.com/user-attachments/assets/10797b49-fdf2-4e92-9a57-effd6179f7a5" />

## 5. Write a c program to find GCD of two numbers using loop.
```
#include <stdio.h>

int main() {
    int a, b, i, gcd;

    printf("Enter two numbers: ");
    scanf("%d %d", &a, &b);

   
    if(a < 0) a = -a;
    if(b < 0) b = -b;

  
    for(i = 1; i <= a && i <= b; i++) {
        if(a % i == 0 && b % i == 0) {
            gcd = i;
        }
    }

    printf("GCD = %d", gcd);

    return 0;
}
```
## output
<img width="736" height="308" alt="image" src="https://github.com/user-attachments/assets/c80bb513-3d36-4adf-bb1c-94aaa7c2993e" />
