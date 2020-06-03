---
layout:     post
title:      Rotate Array
date:       2020-06-03 5:38:19
author:     Sebastian Moreno
summary:    See what the different elements looks like.
categories: LeetCode
thumbnail: python
tags:
 - demo
 - action
 - carte
 - noire
---

Given two non-empty arrays of integers, write a function that determines whether the second array is a subsequence of the first one.

A subsequence of an array is a set of numbers that aren't necessarily adjacent in the array but that are in the same order as they appear in the array. For instance the numbers `[1, 4, 6]` form a subsequence of the array `[1, 2, 3, 4, 5, 6]` and so do the numbers `[2, 4]`. Note that a single number in an array and the array itself are both valid subsequences of the array.

Attempt a similar question [here][1]


{% highlight ruby %}

array = [5,1,22,25,6,-1,8,10]
sequence = [1,6,-1,10]


def isValidSubsequence(array, sequence):
  #Write your code There
  seqIdx = 0

  for num in array:
    #restrict so that the seqIdx doesn't go out of bounds
    if seqIdx < len(sequence):
    #check if the array element matches the sequence element
      if num == sequence[seqIdx]:
          #increment sequence index
          seqIdx = seqIdx + 1

   if seqIdx == len(sequence):
      return True
  else:
      return False
{% endhighlight %}

# Code Explanation:
So the best way to approach this is to create a sequence counter variable. In my case I called it seqIdx. The reason you want to do this is so that you can later validate that the second array is a subsequence of the first. After that I created a for loop that traverses the first array. While traversing, there are two nested if statements that test that the seqIdx variable isn't greater than the length of the sequence, and then that if the number that the first array is currently at matches a number within the second array. The purpose of the first if statement is so that we don't get an out of bounds error and then are unable to return a boolean. Lastly, the code tests if the seqIdx is the same length as the sequence and then returns true if they are and false if they aren't.

[1]: https://leetcode.com/problems/is-subsequence/
