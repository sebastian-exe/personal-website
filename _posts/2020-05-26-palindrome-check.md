---
layout:     post
title:      Palindrome Check
date:       2020-05-26 11:24:19
author:     Sebastian Moreno
summary:    Checks to see if a string is a palindrome
categories: LeetCode
thumbnail: java
tags:
 - demo
 - action
 - carte
 - noire
---


Given a string __str__, the task is to find whether the string str is a palindrome or not in java without using library methods. Consider only alphanumeric characters and ignore cases.

Attempt this question [here][1]!



{% highlight ruby %}
class Solution {
    public boolean isPalindrome(String str) {
        int front = 0;
        int back = str.length() -1;

        while(front < back){
            if(str.charAt(front) ! = str.charAt(back)){
                return false;
            }
            front++;
            back--;
        }
        return true;
    }
}
{% endhighlight %}

# Code Explanation:
The question is asking for us to validate and return a boolean for whether or not a strings is a palindrome. The proper way to approach this is to place two "pointers" one at the beginning of the string and one at the end of the string. I do this in the code above with front and back int variables. The next step is to continue looping while these two pointers have not crossed. Within the while loop there is an if statement with the parameters comparing the string characters at certain indexes of front and back. If at any point during iteration the front or back index characters are not the same value then we know that the string is not a palindrome. If the if statement is not executed, we move each pointer, the front up one index and the back down one index to make a new comparison along the string. If the while loop terminates and the if statement is never executed the function returns true because at that point we have checked every letter in the string.


[1]: https://leetcode.com/problems/valid-palindrome/
