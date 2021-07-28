---
layout: post
title: "C 04 - General tips"
date : 2021-07-28 05:19:00 +0200
categories: C
comments: false

---



General comments on how you can solve the 42Basecamp C04 exercise assignment.

<!--more-->

Quick reminders:

- In C04 you can only use  ```write```. Do **not** import ```stdio.h```.

- Solve small problems first. Then compose it, to make more complex ones. Do not try to write the final code at first.

- Think about the algorithm outside the computer. Use pen and paper to scratch around.

- Remember, you can't import functions from libraries. But you can create yours !

  ---

  Import ```stdlib.h``` and ```string.h``` so you can debug with the expected returns. Don't forget to remove the imports!

- Exercise 00:

  You have done this exercise at C01 exercise 06.

- Exercise 01:

  You have done this exercise at C01 exercise 05.

- Exercise 02:

  You have done this exercise at C00 exercise 07.

- Exercise 03:

  To convert `char`  to `int`, use casting. Example: ```x = (int) x; ```

  To convert `int` to `char`, decompose in single characters (``0~9``) and then add ``'0'``

  Take care about the restrictions of this particular function. Remember when debugging that, the output of the original ``atoi`` is different from ``ft_atoi``.

- Exercise 04:

  Break down in multiple functions and test each of them separately. Suggestion of functions to build:

  - ft_strlen() -> returns the size of a string
  - ft_base_verify() -> returns 0 if no errors found, -1 otherwise. Check all base constraints
  - ft_repetition() -> return 0 if there are no repetitions, -1 otherwise. Verify if there are characters that repeats
  - ft_putnbr() -> the function from exercise 02, but with modifications. You have to use the base!

- Exercise 05:

  It follows the same logic as the 04. It will take some time, it is not a simple exercise. If your time is not good, just go to the next list. But if you want to solve, break down into small functions, pay a lot of attention on the constraints. Most of your program will be constraint checking and a double while as the core algorithm.

  

  
