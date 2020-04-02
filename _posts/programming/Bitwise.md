---
title: Bitwise operations in coding
category: programming
excerpt: >-
    Using bitwise in practice.
---

# Bitwise in coding

Today I started a challenge in LeetCode, and it's first problem was: given a non empty array of integers, return the element that do not repeat itself. Also was asked to the program have linear runtime complexity.

Firstly I solved it with a lot of nested for and ifs, which lead me to pass the case but it does not rank me in a good position, based on performance.

But then I tought about the bitwise operators, which are fast methods of operations since it "operates at the processor level". For those who dont know about bitwise operators, I made a simple image to explain it in a very superficial level.


![](<blockquote class="imgur-embed-pub" lang="en" data-id="a/siGRcOA"><a href="//imgur.com/a/siGRcOA"></a></blockquote><script async src="//s.imgur.com/min/embed.js" charset="utf-8"></script>)


But basically, those operator works on the bit level, and do operations like those in the image. 


After that I rewrite my code using them. It solves the problem in very few lines of code and made the performance to rise a lot. In terms of Runtime Distribution, it was group on the very first group, and in terms of Memory Distribution it is placed on the 25% first.


(image)


Bitwise is something that I never thought about using in practical code. I always think about it as something abstract and low-level that I would never use. I'm glady wrong, and make me think about to leave a bit from the high level programming and start understand more how really computers work.
