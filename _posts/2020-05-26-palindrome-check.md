---
layout:     post
title:      Palindrome Check
date:       2020-05-26 11:24:19
summary:    Checks to see if a string is a palindrome
categories: jekyll
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

# Headings!

They're responsive, and well-proportioned (in `padding`, `line-height`, `margin`, and `font-size`).


[1]: https://leetcode.com/problems/valid-palindrome/
