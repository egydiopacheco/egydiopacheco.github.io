---
title: Memoization
category: programming
excerpt: >-
    Optimising Fibonacci function with Memoization.
---

# Memoization
Given the following code in C:

```c
#include<stdio.h>
#include<time.h>
#define EXIT_SUCESSFUL 0
int fib (int n) {
	if (n <= 1) return n;
	return fib(n-1) + fib(n-2);
}

int main () {
    clock_t start,end;
    double cpu_time_used;
	start = clock();
	int n = 45;
	printf("%d\n", fib(n));
    end = clock();
    cpu_time_used = ((double) (end - start)) / CLOCKS_PER_SEC;
	printf("Time spend in this to run this program: %d ms", cpu_time_used);
	return EXIT_SUCESSFUL;
}
```

The runtime of this recursive Fibonacci, is extremely inefficient. It take several seconds to give a result back, if so. The reason is shown in the following image:

![fib](https://i.imgur.com/cjfIt6x.jpg)

Basically, what is happening is that the program is calculating a result that was already calculated multiple times during it's execution. A simple solution to this problems is to save those calculations in a data structure, like an array. Once the calculations are saved, the program can consult those results very quickly, leading to an impressive optimization in the runtime.

```c
#include<stdio.h>
#include<time.h>
#define EXIT_SUCESSFUL 0

int fib_improved (int n) {
    int arr[n+2];
    arr[0] = 0;
    arr[1] = 1;
    
    for(int i = 2; i < n ; i++) {
        f[i] = f[i-1] + f[i-2];
    }
    return f[n];
}

int main () {
    clock_t start,end;
    double cpu_time_used;
    start = clock();
    int n = 45;
    printf("%d\n", fib_improved(n));
    end = clock();
    cpu_time_used = ((double) end - start) / CLOCKS_PER_SEC;
    printf("Time spend in this to run this program: %d ms", cpu_time_used);
    return EXIT_SUCESSFUL;
}
```

When comparing the runtime for n = 45, the first program takes about 11 seconds to finish and the second one is instantaneous.  Memoization clearly optimized the Fibonacci recursion.
