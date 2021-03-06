---
layout:     post
title:      Reverse String
date:       2020-06-07 8:30:00
author:     Sebastian Moreno
summary:    Reverse String in place
categories: LeetCode
thumbnail: python
tags:
 - demo
 - action
 - carte
 - noire
---

Write a function that reverses a string. The input string is given as an array of characters char[].

Do not allocate extra space for another array, you must do this by modifying the input array in-place with O(1) extra memory.
You may assume all the characters consist of printable ascii characters.

Attempt this question [here][1]

**Example 1:**
{% highlight ruby %}
Input: ["h","e","l","l","o"]
Output: ["o","l","l","e","h"]
{% endhighlight %}


**Example 2:**
{% highlight ruby %}
Input: ["H","a","n","n","a","h"]
Output: ["h","a","n","n","a","H"]
{% endhighlight %}


{% highlight ruby %}
class Solution:
    def reverseString(self, s: List[str]) -> None:
        """
        Do not return anything, modify s in-place instead.
        """
        front = 0
        back = len(s) -1

        while front < back:
            temp = s[front]
            s[front] = s[back]
            s[back] = temp
            front += 1
            back -= 1


{% endhighlight %}

# Code Explanation:
A quick way to approach this question involves remembering how to do the swap in selection sort and how to use two pointers when traversing a string like we did in palindrome check. We have two pointer, one at the front of the word and one at the back of the word. After that we loop both pointers until they are next to each other. While we are looping the pointers we incorporate the same swap method that we used in selection sort manually swapping every letter while also incrementing the front pointer and decrementing the back pointer.

[1]: https://leetcode.com/explore/interview/card/top-interview-questions-easy/127/strings/879/
