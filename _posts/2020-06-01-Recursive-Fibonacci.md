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
The best way to approach any recursive problem is by first attacking the base cases. In this scenario they are the first two values of the fibonacci sequence. This is taken care of when we place if statements to return specific values when n is 2 and when n is 1. To generate the rest of the sequence, we must implement a recursive call. The recursive call is placed after the base statements and is an implementation of the equation that generates the fibonacci sequence. 

[1]: https://www.programiz.com/python-programming/examples/fibonacci-recursion
[2]: https://www.geeksforgeeks.org/program-for-nth-fibonacci-number/
