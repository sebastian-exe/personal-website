---
layout:     post
title:      Single Number
date:       2020-06-02 8:31:19
author:     Sebastian Moreno
summary:    Array question under LeetCode easy.
categories: LeetCode
thumbnail: python
tags:
 - demo
 - action
 - carte
 - noire
---

Given an array of integers, find if the array contains any duplicates.
Your function should return true if any value appears at least twice in the array, and it should return false if every element is distinct.

Attempt this question [here][1]

<ins> First Attempt Is Below</ins>
* this attempt passed 17 of 18 test cases on LeetCode but eventually threw a time limit exceeded error.
{% highlight ruby %}
class Solution:
    def containsDuplicate(self, nums: List[int]) -> bool:

        for i in range(len(nums)):
            for j in range(i+1, len(nums)):
                #print("i: ", nums[i], "j: ", nums[j])
                if nums[i] == nums[j]:
                    return True
        return False

{% endhighlight %}

<ins> Second Successful Attempt </ins>
{% highlight ruby %}
class Solution:
    def containsDuplicate(self, nums: List[int]) -> bool:
        nums.sort()

        for i in range(len(nums)-1):
            if nums[i] == nums[i +1]:
                return True
        return False
{% endhighlight %}

# Code Explanation:
There are multiple solutions to this type of problem. My first attempt takes an iterative approach to the question and uses a nested for loop to search the indexes. I like to call this approach a "two pointer solution" since I have the j variable in front of the i variable while the comparisons are being made.

The second attempt is more of something that you want to do during an interview scenario. This approach is also more efficient that the first solution. Basically the first step is to sort the numbers array. This allows us to have just one for loop that can index the now sorted array. Notice that the for loop goes to range(len(num))  - 1, this protects you from an out of bounds error within the if statement when it starts to make comparisons. Next comes the if statement. The if statement will be

[1]: https://leetcode.com/explore/interview/card/top-interview-questions-easy/92/array/578/
