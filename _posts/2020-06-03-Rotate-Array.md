---
layout:     post
title:      Rotate Array
date:       2020-06-03 5:38:19
author:     Sebastian Moreno
summary:    Shift all the elements of an array based on a key value
categories: LeetCode
thumbnail: python
tags:
 - demo
 - action
 - carte
 - noire
---

Given an array, rotate the array to the right by k steps, where k is non-negative.

<ins>Follow up:</ins>
* Try to come up as many solutions as you can, there are at least 3 different ways to solve this problem.
* Could you do it in-place with O(1) extra space?

Attempt this question [here][1]

<ins> Example 1: </ins>
{% highlight ruby %}
Input: nums = [1,2,3,4,5,6,7], k = 3
Output: [5,6,7,1,2,3,4]
Explanation:
rotate 1 steps to the right: [7,1,2,3,4,5,6]
rotate 2 steps to the right: [6,7,1,2,3,4,5]
rotate 3 steps to the right: [5,6,7,1,2,3,4]
{% endhighlight %}

<ins> Example 2: </ins>
{% highlight ruby %}
Input: nums = [-1,-100,3,99], k = 2
Output: [3,99,-1,-100]
Explanation:
rotate 1 steps to the right: [99,-1,-100,3]
rotate 2 steps to the right: [3,99,-1,-100]
{% endhighlight %}



<ins> Solution 1: </ins>
{% highlight ruby %}
class Solution:
    def rotate(self, nums: List[int], k: int) -> None:
        """
        Do not return anything, modify nums in-place instead.
        """
        rotate = [0] * len(nums)

        for i in range(len(nums)):
            rotate[(i+k) % len(nums)] = nums[i]


        for i in range(len(nums)):
            nums[i] = rotate[i]

{% endhighlight %}

<ins> Solution 2: </ins>
{% highlight ruby %}
class Solution:
    def rotate(self, nums: List[int], k: int) -> None:
        """
        Do not return anything, modify nums in-place instead.
        """
        rotate = nums.copy()

        for i in range(len(rotate)):
            nums[(i+k) % len(nums)] = rotate[i]
{% endhighlight %}


# Code Explanation:
I will explain the code to the second solution since it not only is 3 lines code but on average performs better than the first solution. Basically what is happening is that we copy the passed in nums array to another array called rotate. Then we loop through the rotate array. While we are looping through the rotate array we are calculating the new index of the values from the rotate array and overriding them in the nums array since the values must be changed in place. The new index is found by taking the i index from the for loop and adding that with the key k that is passed in from the main. We then mod it by the size of the array to take care of when the value of i + k happens to be bigger than the size of the array. After this has been done for every value in the rotate array the nums array will be completely shifted.

[1]: https://leetcode.com/explore/interview/card/top-interview-questions-easy/92/array/646/
