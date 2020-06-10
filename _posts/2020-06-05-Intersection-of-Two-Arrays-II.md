---
layout:     post
title:      Intersection of Two Arrays II
date:       2020-06-05 2:30:19
author:     Sebastian Moreno
summary:    Very Similar question to move zeros to end.
categories: LeetCode
thumbnail: python
tags:
 - demo
 - action
 - carte
 - noire
---

Given two arrays, write a function to compute their intersection.

Attempt this question [here][1]


<ins>Solution 1:</ins>
{% highlight ruby %}
class Solution:
    def intersect(self, nums1: List[int], nums2: List[int]) -> List[int]:
        result = []
        for i in nums1:
            if i in nums2:
                result.append(i)
                nums2.remove(i)

        return result
{% endhighlight %}

<ins>Solution 2:</ins>
{% highlight ruby %}

{% endhighlight %}
# Code Explanation:
So the best way to approach this is to create a sequence counter variable. In my case I called it seqIdx. The reason you want to do this is so that you can later validate that the second array is a subsequence of the first. After that I created a for loop that traverses the first array. While traversing, there are two nested if statements that test that the seqIdx variable isn't greater than the length of the sequence, and then that if the number that the first array is currently at matches a number within the second array. The purpose of the first if statement is so that we don't get an out of bounds error and then are unable to return a boolean. Lastly, the code tests if the seqIdx is the same length as the sequence and then returns true if they are and false if they aren't.

[1]: https://leetcode.com/explore/interview/card/top-interview-questions-easy/92/array/674/
