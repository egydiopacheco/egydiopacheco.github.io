---

layout: notes

title: Shell 00 - General tips

date : 2021-07-13 09:50:00

categories: shell

---





General comments on how you can solve the 42Basecamp shell00 exercise assignment.



- Exercise 00:
  
   The first one is very straightforward, try to compose these commands:
  
  - echo "some message"
  
  - The pipe operator ( > )

- Exercise 01:
  
  This exercise is to learn about permissions and permission changes. You have to understand what is each component of the printed message by ```ls -l```.  After that you have to change the components of each test. Useful commands:
  
  - chmod
  
  - touch -d " custom date here " filename
  
  - echo

- Exercise 02:
  
  It is the same of exercise 1 but with addition of hard and symbolic links. Check this reference for exercise 01 and 02 [click here](https://salmenzouari.medium.com/what-is-soft-link-and-hard-link-in-linux-39e641e023bd#:~:text=A%20symbolic%20or%20soft%20link,to%20a%20non%2Dexistent%20file.). Useful commands:
  
  - ln 

- Exercise 03:
  
  A cool exercise. It is solvable by reading the extensive flag list of ```man ls```. Experiment on your computer root directory (/), which has a lot of files and folders.

- Exercise 04:
  
  In this one, you start to feel the shell scritpt power. It brings a like more complexity compared to the past ones. You should read the ```man git``` page. However, it is to extensive. Try to install an extension called ```tldr``` (*Too long to read*) and type ```tldr git``` on your terminal. Commands to look up:
  
  - git log

- Exercise 05:
  
  In my opinion, the hardest one in the list. The interpretation of the problem is crucial: **They want the list of files ignored by the .gitignore file, not what is inside the .gitignore file**. Commands to look up:
  
  - ```bash```
    find
    ```
  
  - ```bash
    git check-ignore
    ```

- Exercise 06:
  
  This one is super simple. Really. Just read the ```man patch``` and experiment with the files given in the zip archive on your computer. It is solvable by one command.

- Exercise 07:
  
  Well, the main tip I can give you is: Richard Stallman solved this problem for you in the ```man find ``` example section. Also look up for regex!

- Exercise 08:
  
  This is one tricky. You have to understand what is about magic, and the man page for it, is not very clear.
  
  But your solution file should follow the following design:
  
  ```shell```
  offset type test message
  ```
  
  Where offset is the limit of bytes your data will be tested. Type is, well the type, of you're dealing with. Test,  will be the values your file will be compared with. The message is what will be printed when the comparison succeeds.
