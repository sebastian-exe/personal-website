---
layout:     post
title:      Move Element To End
date:       2020-06-05 2:17:19
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

You're given an array of integers and an integer. Write a function that moves all instances of that integer in the array to the end of the array and returns the array. The function should perform this in place.


{% highlight ruby %}
def moveElementToEnd(array, toMove):
    if not array:
      return[]
    else:
      for i in range(len(array),-1,-1):
        i -= 1
        if array[i] == toMove:
          shift = array[i]
          array.pop(i)
          array.append(i)

      return array


{% endhighlight %}

# Code Explanation:
This is a pretty simple question. The first if statement just checks to see if the array is empty in which it would return an empty array back as well. The else statement traverses the array backwards!!! This is important to know that it is traversing the array backwards because we decrement the value of i after the for loop starts to do its thing. While it is traversing backwards if the number that an element in the array contains is equal to toMove we start to perform a shift popping and appending the number back to the end of the array. Doing this also keeps the other elements in place while shifting the others.
