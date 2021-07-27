---
layout: post
title: "C 03 - General tips"
date : 2021-07-27 20:27:00 +0200
categories: C
comments: false

---



General comments on how you can solve the 42Basecamp C03 exercise assignment.

<!--more-->

Quick reminders:

- In C03 you cannot use any function . Do **not**  ```import ``` any library.

- Solve small problems first. Then compose it, to make more complex ones. Do not try to write the final code at first.

- Think about the algorithm outside the computer. Use pen and paper to scratch around.

- Remember, you can't import functions from libraries. But you can create yours !

  ---

  This assignment list, you will have to rewrite functions that already exists in libraries.

- Exercise 00:

  First of all: ```man strcmp```. Second, the output of this function is strange, so do not panic. You can import ```<string.h>``` just for debugging process. Do not forget to remove it!

  Another thing to be careful is: your return can be negative if you don't be cautious. Read about *casting*.

- Exercise 01:

  It is the same as exercise 00 but limited by a integer n. If you made 00 this one will be simple.

- Exercise 02:

  You have to write a function that concatenates two strings. Actually, there is an implementation on the man page.

  Do not forget to add the ``` \0``` at the end of concatenation.

- Exercise 03:

  As it happens with exercise 00/01, now you have to do the same you did on 02 but with an unsigned integer as a limit.

  Remember that your iterators need to be of type unsigned int, otherwise you will receive a warning at compile time, which invalidates your work.

- Exercise 04:

  Now you have to create a function that find a substring inside a string.

  If what you have to find is null, return the whole string.

  But the idea is to find a character that match with the string you have. Them you look the next one, until there is a complete match. Otherwise change the character position to next one and repeat the process.

  There is different implementations of this function on Apple open source , Google android functions, GNU and BSD libraries. If you are stuck you can look on what they did.

- Exercise 05:

  Be careful with the types. You receive an unsigned int and need to return an unsigned int. Do not create int iterators if you don't know what you're doing, otherwise you will have compile warning problems. This exercise you have to implement a function that concatenate a source string in a destiny string. Read on the man page what is the size parameter. This function is similar to ```strncat()``` that you already implemented. But there are differences. You can implement a function that calculates the length of a string, or you can use the followng snippet:

  ```c
  	while (n-- > 0 && *d) // n is size , *d is the destiny string
  		d++;
  	dest_len = d - dest; // then you do pointer arithmetic
  ```