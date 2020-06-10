---
layout:     post
title:      Move Zeros
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

Given an array nums, write a function to move all 0's to the end of it while maintaining the relative order of the non-zero elements.

Attempt this question [here][1]

{% highlight ruby %}
Input: [0,1,0,3,12]
Output: [1,3,12,0,0]

{% endhighlight %}

<ins>Solution:</ins>
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
This question is very similar to move element to end. The main difference between these two questions is that we are performing the shifting of pop and appending just to elements that have the value of zero and not a specified value as in move elements to end

[1]: https://leetcode.com/explore/interview/card/top-interview-questions-easy/92/array/567/
