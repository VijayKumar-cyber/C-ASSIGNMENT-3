# C-ASSIGNMENT-3
# C Programming Exercises
## NAME:VIJAY KUMAR D
## REG NO:212224243002
## 1. Print all prime numbers between two limits

```c
#include <stdio.h>

int isPrime(int num) {
    if (num <= 1) return 0;
    for (int i = 2; i * i <= num; i++) {
        if (num % i == 0)
            return 0;
    }
    return 1;
}

int main() {
    int start, end;
    printf("Enter two limits: ");
    scanf("%d %d", &start, &end);

    printf("Prime numbers between %d and %d are:\n", start, end);
    for (int i = start; i <= end; i++) {
        if (isPrime(i))
            printf("%d ", i);
    }
    return 0;
}
```

**Output Example:**
```
Enter two limits: 10 30
Prime numbers between 10 and 30 are:
11 13 17 19 23 29
```

---

## 2. Count number of digits in a number

```c
#include <stdio.h>

int main() {
    int num, count = 0;

    printf("Enter a number: ");
    scanf("%d", &num);

    if (num == 0) {
        count = 1;
    } else {
        while (num != 0) {
            num /= 10;
            count++;
        }
    }

    printf("Number of digits: %d\n", count);
    return 0;
}
```

**Output Example:**
```
Enter a number: 12345
Number of digits: 5
```

---

## 3. Print alphabet 'S' in n x n matrix

```c
#include <stdio.h>

int main() {
    int n;
    printf("Enter size (n): ");
    scanf("%d", &n);

    for (int i = 0; i < n; i++) {
        for (int j = 0; j < n; j++) {
            if (i == 0 || i == n/2 || i == n-1 || 
                (i < n/2 && j == 0) || 
                (i > n/2 && j == n-1)) {
                printf("*");
            } else {
                printf(" ");
            }
        }
        printf("\n");
    }

    return 0;
}
```

**Output Example (n = 5):**
```
*****
*    
*****
    *
*****
```

---

## 4. Pyramid pattern

```
   *
  ***
 *****
*******
```

```c
#include <stdio.h>

int main() {
    int n = 4;

    for (int i = 1; i <= n; i++) {
        for (int j = i; j < n; j++) {
            printf(" ");
        }
        for (int k = 1; k <= (2 * i - 1); k++) {
            printf("*");
        }
        printf("\n");
    }

    return 0;
}
```

**Output:**
```
   *
  ***
 *****
*******
```

---

## 5. Find GCD of two numbers using loop

```c
#include <stdio.h>

int main() {
    int a, b, gcd;

    printf("Enter two numbers: ");
    scanf("%d %d", &a, &b);

    for (int i = 1; i <= a && i <= b; i++) {
        if (a % i == 0 && b % i == 0) {
            gcd = i;
        }
    }

    printf("GCD = %d\n", gcd);
    return 0;
}
```

**Output Example:**
```
Enter two numbers: 12 18
GCD = 6
```
