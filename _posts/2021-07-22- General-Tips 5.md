---
layout: post
title: "C 02 - General tips"
date : 2021-07-22 05:27:00 +0200
categories: C
comments: false

---



General comments on how you can solve the 42Basecamp C02 exercise assignment.

<!--more-->

Quick reminders:

- In C02 you can only use just ```write``` function at exercises 11 and 12. Do **not** import ```stdio.h```.

- Solve small problems first. Then compose it, to make more complex ones. Do not try to write the final code at first.

- Think about the algorithm outside the computer. Use pen and paper to scratch around.

- Remember, you can't import functions from libraries. But you can create yours !

  ---

  This exercise assignment is about reading the man pages. Really. Exercises 1 to 8 are all similar, 9 and 10 are a bit difficult but totally doable. 11 and 12 are challenges.

  11 and 12 are not listed here. If I have time until the end of the bootcamp I comeback to edit this one.

- Exercise 00:

  I will not say anything about this one. Just surprise yourself with : ``man strcpy``

- Exercise 01:

  Same as exercise 00, just with a tiny detail at the end. This detail is also explained on ``man strcpy``

- Exercise 02:

  Now, open your ASCII table! You will use it on exercises 2~8. The solution is just a while with an if condition using ASCII code. 

  Do not forget the ```str[j] != 0``` on the if condition.

  The null character is represented by ```\0```.

- Exercise 03:

  Now you just have to change the if condition, to verify if it is numeric. ASCII table again!

- Exercise 04:

  All the characters in the string must be lowercase. Yes, ASCII..

- Exercise 05:

  Same from exercise 04, but with uppercase. I think you already got the idea what is happening...

- Exercise 06:

  The ASCII code you want is: ```(~ < 32) and (= 127)```.

- Exercise 07:

  The difference between `a` and `A` in ASCII table is `32`. So the operation the you want to do is `x - 32`.

- Exercise 08:

  Same as exercise 07, but now you do `x + 32`.

- Exercise 09:

  This exercise is not difficult. But is boring, you have to be careful and it will take some of your time. You want to compose the if conditions with all the constraints the problem states.

- Exercise 10:

  It is not that clear of the exercise wants and the output is kinda obscure. Steps:

  Read the man page several times.

  Create a function that calculates the length of a string.

  You want to return an unsigned integer. Be careful to not create int type iterators.

  Read the man page again. Do not forget the null terminator.

  Size is size or size minus something?

  If you are stuck, read the apple source code for this function.

  Do tests while you progress with the function.