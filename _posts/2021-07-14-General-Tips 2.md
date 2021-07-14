---
layout: post
title: "Shell 01 - General tips"
date : 2021-07-14 20:42:00 +0200
categories: shell
comments: false
---



General comments on how you can solve the 42Basecamp shell00 exercise assignment.

<!--more-->

- Exercise 00:
  
  This is just a reminder.

- Exercise 01:
  
  In this exercise you learn how to deal with environment variables. You can access then in bash with this syntax: ```$VARIABLE_NAME``` . Useful commands:
  
  - tr

- Exercise 02:
  
  You have to search recursively, inside a directory, for files with ```.sh``` extension and print them, without the extension. Example: you find ```test.sh``` and them print ```test```. Useful commands:
  
  - find
  
  - exec

- Exercise 03:
  
  Follow the same logic as the exercise 02, but now you have to count the number of files, folders, subfolders, found. Useful comands:
  
  - find
  
  - wc

- Exercise 04:
  
  The context of regular expression are really useful on this one. Regex are tricky, so be careful. The tip is, run ```ifconfig -a``` inside your local machine terminal, and look for patterns on how MAC addresses show up. Useful commands:
  
  - grep
  - awk
  - sed

- Exercise 05:
  
  This is tricky. Try to take of all the special character and create ```MarVIn``` . Then add ``` '' ``` and check if you are able to create the file. Then add ```*``` and see if you can go. Go composing. Useful search:
  
  - Escape character: backslash: (```\```)

- Exercise 06:
  
  Type ls -l on your local machine, you will get an output (I suggested to do it on your local machine, because it will return more outputs without having to create files at the virtual environment. Basically, it is easier to test and debug). Now try to print only odd lines of this output. Do not insert blank/empty lines. Useful commands:
  
  - sed
  
  - awk

- Exercise 07:
  
  It is simple, but will demand time. You have to compose results of a command to other commands as arguments, using the pipeline operator ```|```. Think about a factory, every step will do a tiny thing, but in the you will have the whole product. Useful commands:
  
  - sed
  
  - awk
  
  - grep
  
  - tr
  
  - rev
  
  - sort

- Exercise 08:
  
  I have not done it yet, I will update it as soon as I finish.

