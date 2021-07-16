---
layout: post
title: "C 00 - General tips"
date : 2021-07-15 21:22:00 +0200
categories: C
comments: false
---



General comments on how you can solve the 42Basecamp C00 exercise assignment.

<!--more-->

Quick reminders:

- In C00 you can use just ```write``` function. Do **not** import ```stdio.h```.

- The ```write``` function is a system call function that belongs to POSIX. Import ```<unistd.h>``` so you can use it.

- [Read the man page](https://man7.org/linux/man-pages/man2/write.2.html)

- Understand the function signature:   ```ssize_t write(int fd, const void *buf, size_t count);```

- Solve small problems first. Then compose it, to make more complex ones. Do not try to write the final code at first.

- Think about the algorithm outside the computer. Use pen and paper to scratch around.

- Remember, you cant import functions from libraries. But you can create yours !

  ---

- Exercise 00:
  
  This is one is simple, ***if***, you read the ```write``` man page. 

  Steps:
  
  - Build a function using the given signature
  - Use the ```write``` function.
  
- Exercise 01:

  It follow the same logic as exercise00, but now you have to print 26 characters (the whole alphabet). How you do this? Use ```while```.  You also need to learn how to declare and assign char variables. Here is how:

  ```c
  char 	any_name;
  any_name = 'a';
  ```

  Steps:

  - Declare a char variable;
  - Assign it to the first letter of alphabet.
  - Loop, until you reach `z`.
  - Use `write` function inside the while loop.

- Exercise 02:

  It is exactly the same as exercise 01, but backwards.

- Exercise 03:

  It is the same construction as the exercise 01 and 02. But using numbers 0-9. However, if your program is printing empty lines, read the ```write``` man page. Tip: do not use ```int```.

- Exercise 04:

  The first problem using ```if/ else```. A number `n` is positive if ```n >= 0```, else it is negative.

  Steps:

  - Open a ```if/ else``  statement
  - Use ```write``` to print `P` for positive and `N` for negative
  - Use double quotes ```""``` around `P` and `N`

  This was the last really simple problem on the assignment.

- Exercise 05:

  Now things get a little more complex. Solution structure suggestion:

  - Declare one char variable for the hundreds, dozens and units.
  - How far the hundreds can go? How far the dozens can go? How far the units can go?
  - Make a triple nested loop, one for the hundreds, one for the dozens and one for the units.
  - Every iteration should print a number on the terminal.
  - Compute the changes with  ```++``` operator. 

- Exercise 06:

  This exercise is similar than exercise 05. Break the exercise in pieces. Try to print first only :

  ```0, 1, 2, 3...10,11``` 

  Then add more complexity and try do print :

  ```00, 01, 02, 03...```

  Now to try to print the pairs.

  Tips:

  - Break down the exercise in pieces using helper functions.

- Exercise 07:
  
  The trick to solve this one is that you can transform a **```int```** in a  **```char```** with 
  
  ```new_char_variable = your_integer_goes_here + '0';```
  
  And also remember this: you can just do that if your integer is between ```0 - 9```. Which means that, for numbers with more than 2 digits you will have to break down the numbers into single digits. Keywords to do that:
  
  - Modulo operator ```%```
  - Division operator ```/```
  - Recursion process (it also can be an iterative process, if you prefer)
  
- Exercise 08:
  
  I have not done it yet, I will update it as soon as I finish.

