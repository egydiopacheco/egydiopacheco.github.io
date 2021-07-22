---
layout: post
title: "C 01 - General tips"
date : 2021-07-22 10:54:00 +0200
categories: C
comments: false
---



General comments on how you can solve the 42Basecamp C01 exercise assignment.

<!--more-->

Quick reminders:

- In C01 you can use just ```write``` function. Do **not** import ```stdio.h```.

- The ```write``` function is a system call function that belongs to POSIX. Import ```<unistd.h>``` so you can use it.

- [Read the man page](https://man7.org/linux/man-pages/man2/write.2.html)

- Understand the function signature:   ```ssize_t write(int fd, const void *buf, size_t count);```

- Visualize the quick sort algorithm [Here](https://www.youtube.com/watch?v=XE4VP_8Y0BU&t=1s)

- Pseudocode for quick sort [Here](https://www.cc.gatech.edu/classes/cs3158_98_fall/quicksort.html)

- Solve small problems first. Then compose it, to make more complex ones. Do not try to write the final code at first.

- Think about the algorithm outside the computer. Use pen and paper to scratch around.

- Remember, you can't import functions from libraries. But you can create yours !

  ---

- Exercise 00:

  You want to access the variable nbr, and change it. Read about the derreferentiator operator. It looks like a pointer but they are not the same. 

- Exercise 01:

  It is the same as the exercise 00, but repeated 9 times.

- Exercise 02:

  In c, arguments are passed by value, not by reference. In other words, you have to access the variables and change them. You may consider a temporary variable so you do not lost your original values.

- Exercise 03:

  Create two variables, one for storing the result of integer division (```/```) and other for storing the value of mod operation (```%```). After that use the derreferenciator operator to access the value inside the address passed as parameter, and change them accordingly: 

  - division receives the value of division operation;
  - mod receives the value of mod operation.

- Exercise 04:

  Do the same as exercise 03, but this the be careful to not lose your values. Create temporary variables to help you while you do the operations.

- Exercise 05:

  Build a while loop with a counter starting at 0. Loop over until the end of the string. You can use the '\0' as the condition for your while. Example:

  - while (....!= '\0')

    When printing using write, remember you don't need to use & for arrays, because they are already pointers, hence, contains an address inside of them.

- Exercise 06:

  You can solve this using a loop structure similar to exercise 05 with a counter, to get the size of the string. You can also use the difference between 2 pointers, to get the size of the string. That works because pointers support arithmetic operations. So you can do something like (this is just a scratch) :

  ```c
  char	*c; <- put some values here, like a string
  char	*d;
  
  d = c;
  
  d++;
  d++;
  
  print(d - c); <- returns 2;
  
  ```

  

- Exercise 07:

  If you have an array like: [1,2,3,4,5]. If you reverse it, the result will be: [5, 4, 3, 2, 1]. Realize that you just perfomed ```n / 2```  operations, where  ```n```  is the size of the array. If you perform   ```n```  operations, you will undo the changes you made it, so you will get back to the original array.

  After that, you will loop inside the array and change the first element with the last and so on, until you reach the middle. The main problem is to get the array indices right. Also, create a temporary variable so you do not lose values.

- Exercise 08:
  
  This exercise you should implement any sort algorithm. You can use bubble sort, quick sort, merge sort etc. Look for references on how to implement them.
  
  
