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

Given a **non-empty** array of integers, every element appears _twice_ except for one. Find that single one.

Attempt this question [here][1]

**Example 1:**
{% highlight ruby %}
Input: [2,2,1]
Output: [1]
{% endhighlight %}

**Example 2:**
{% highlight ruby %}
Input: [4,9,5], nums2 = [9,4,9,8,4]
Output: [4,9]
{% endhighlight %}

{% highlight ruby %}
class Solution:
    def singleNumber(self, nums: List[int]) -> int:
        noDuplicates = []

        for i in nums:
            if i not in noDuplicates:
                noDuplicates.append(i)
            else:
                noDuplicates.remove(i)
        return noDuplicates.pop()
{% endhighlight %}

# Code Explanation:
This solution does not contain a hash map. I will re-attempt this question soon with a hash map solution. Basically what is happening in this solution is that we create a new array empty array that doesn't contain duplicates. We then traverse the nums list and check the elements. While we traverse it we add the elements to the noDuplicates list the first time they are encountered. If a number is passed to noDuplicates that already exists then we execute noDuplicates.remove(i) since that number does appear twice within the nums list.

[1]: https://leetcode.com/explore/interview/card/top-interview-questions-easy/92/array/549/
