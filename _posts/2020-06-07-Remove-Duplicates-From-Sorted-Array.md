---
layout:     post
title:      Remove Duplicates from Sorted Array
date:       2020-06-05 2:17:19
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
nums = [0 ,1,0,3,12]
#nums = [0,0,1]

def moveZeros(nums):

    for i in range(len(nums), -1, -1):
        i -= 1
        if nums[i] == 0:
            shiftZero = nums[i]
            nums.pop(i)
            nums.append(shiftZero)



moveZeros(nums)
print(nums)
{% endhighlight %}

# Code Explanation:
So the best way to approach this is to create a sequence counter variable. In my case I called it seqIdx. The reason you want to do this is so that you can later validate that the second array is a subsequence of the first. After that I created a for loop that traverses the first array. While traversing, there are two nested if statements that test that the seqIdx variable isn't greater than the length of the sequence, and then that if the number that the first array is currently at matches a number within the second array. The purpose of the first if statement is so that we don't get an out of bounds error and then are unable to return a boolean. Lastly, the code tests if the seqIdx is the same length as the sequence and then returns true if they are and false if they aren't.

[1]: https://leetcode.com/explore/interview/card/top-interview-questions-easy/92/array/567/
[2]: https://www.geeksforgeeks.org/backward-iteration-in-python/