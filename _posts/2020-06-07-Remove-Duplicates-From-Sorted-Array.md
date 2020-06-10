---
layout:     post
title:      Remove Duplicates from Sorted Array
date:       2020-06-07 2:17:19
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

Given a sorted array _nums_, remove the duplicates in-place such that each element appear only once and return the new length.

Do not allocate extra space for another array, you must do this by modifying the input array in-place with O(1) extra memory.

Attempt this question [here][1]

<ins>Example 1:</ins>
{% highlight ruby %}
Given nums = [1,1,2]

Your function should return length = 2, with the first two elements of nums being 1 and 2 respectively.

It doesn't matter what you leave beyond the returned length.


{% endhighlight %}

<ins>Example 2:</ins>
{% highlight ruby %}
Given nums = [0,0,1,1,1,2,2,3,3,4]

Your function should return length = 5, with the first five elements of nums being modified to 0, 1, 2, 3, and 4 respectively.

It doesn't matter what values are set beyond the returned length.

{% endhighlight %}


<ins>Solution:</ins>
{% highlight ruby %}
class Solution:
    def removeDuplicates(self, nums: List[int]) -> int:

        i = 0
        for j in range(len(nums)):
            if nums[i] != nums[j]:
                i += 1
                nums[i] = nums[j]

        return i + 1
{% endhighlight %}

# Code Explanation:
Basically what is going on is that we are using i = 0 as a counter. We then traverse the array using a for loop with another variable, in this case j. If the first number is not equal to the second number, we increment the counter i, and we set nums[i] to nums[j] to update the position of the position of the counter to be after the duplicate. Then the process starts all over again.

[1]: https://leetcode.com/explore/interview/card/top-interview-questions-easy/92/array/727/
