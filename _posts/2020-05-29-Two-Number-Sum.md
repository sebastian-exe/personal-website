---
layout:     post
title:      Two Number Sum
date:       2020-05-29 5:38:19
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

Write a function that takes in a non-empty array of distinct integers and an integer representing a target sum. If any two numbers in the input array sum up to the target sum, the function should return them in array, in any order. If no two numbers sum up to the target sum, the function should return an empty array.

**Note** that the target sum has to be obtained by summing two different integers in the array; you can't add a single integer to itself in order to obtain the target sum

Attempt this question [here][1]!

{% highlight ruby %}

array = [3,5,-4,8,11,1,-1,6]
targetSum = 10

#Space = O(1) Time = O(N)
def TwoNumSum(array, targetSum):

    #first for loop, iterates through setting up the first value as valOne
    for i in range(len(array)):
        valOne = array[i]

        #second for loop iterates through setting up the second value as valTwo
        for j in range(i + 1, len(array)):
            valTwo = array[j]

            #add both valOne and valTwo and set them to a third variable
            valThree = valOne + valTwo

            #if both of the values add up to the targetSum, return them
            if valThree == targetSum:
                return[valOne, valTwo]

      #if no pairs are found, return an empty array
      return[]

{% endhighlight %}

# Code Explanation:
Basically what is happening is that the first for loop iterates through and sets a value to valOne. Then the second for loop does the same and sets the value of an element one index ahead of the first for loop equal to valTwo. After that I decided to sum both of these values and set them equal to a third value just for clarity. Next enters an if statement checking to see if the targetSum is equal to the summation of valOne and valTwo. If this is true, the if statement is executed and we return an array containing the values of valOne and valTwo. If this is not true, both for loops continue to execute and add matching pairs until either a pair does equal the targetSum or they reach the end of the array and no matches have been made. If no matches have been made the function return an empty array.

[1]: https://leetcode.com/problems/two-sum/
