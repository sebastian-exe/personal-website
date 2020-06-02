---
layout:     post
title:      Recursive Fibonacci
date:       2020-06-01 3:45:30
author:     Sebastian Moreno
summary:    Generate the Fibonacci Numbers Recursively
categories: LeetCode
thumbnail: python
tags:
 - demo
 - action
 - carte
 - noire
---

The Fibonacci sequence is defined as follows: the first number of the sequence is `0`, the second number is `1`, and the nth number is the sum of the (n-1)th and (n-2)th numbers. Write a function that takes in an integer `n` and returns the nth fibonacci number.

**Note** The fibonacci sequence is often defined with its first two numbers as `F0 = 0` and `F1 =  1`. For the purpose of this question, the first fibonacci number is `F0`; therefore, `getNthFib(1)` is equal to `F0`, `getNthFib(2)` is equal to `F1`

Attempt this question [here][1]!
If you want to read more about recursion and how it works with the fibonacci sequence you can read more about it [here][2]
{% highlight ruby %}
def  getNthFib(n):
  #write your code here.
  #O(2^N) time, O(N) Space

  if n == 2:
    return 1
  if n == 1
    return 0

  return getNthFib(n-1) + getNthFib(n-2)
{% endhighlight %}

# Code Explanation:
Basically what is happening is that the first for loop iterates through and sets a value to valOne. Then the second for loop does the same and sets the value of an element one index ahead of the first for loop equal to valTwo. After that I decided to sum both of these values and set them equal to a third value just for clarity. Next enters an if statement checking to see if the targetSum is equal to the summation of valOne and valTwo. If this is true, the if statement is executed and we return an array containing the values of valOne and valTwo. If this is not true, both for loops continue to execute and add matching pairs until either a pair does equal the targetSum or they reach the end of the array and no matches have been made. If no matches have been made the function return an empty array.

[1]: https://www.programiz.com/python-programming/examples/fibonacci-recursion
[2]: https://www.geeksforgeeks.org/program-for-nth-fibonacci-number/
