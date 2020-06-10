---
layout:     post
title:      Three Number Sum
date:       2020-06-08 8:30:00
author:     Sebastian Moreno
summary:    Medium Ranked Question
categories: LeetCode
thumbnail: python
tags:
 - demo
 - action
 - carte
 - noire
---

Write a function that takes in a non-empty array of distinct integers and an integer representing a target sum. The function should find all triplets in the array that sum  up to the target sum and return a two dimensional array of all these triplets. The numbers in each triplet should be ordered in ascending order, and the triplets themselves should be ordered in ascending order with respect to the numbers they hold.

If no three numbers sum up to the target sum, the function should return an empty array.


{% highlight ruby %}
def threeNumberSum(array, targetSum):
    # Write your code here.
	array.sort()

	threeNumSums = []

	for i in range(len(array)-2):
		left = i + 1
		right = len(array) -1
		while left < right:
			if (array[i] + array[left] + array[right]) == targetSum:
				#store them in an array
				threeNumSums.append([array[i], array[left], array[right]])
				left += 1
				right -= 1

			elif (array[i] + array[left] + array[right]) < targetSum:
				#increment the left pointer
				left += 1
			elif (array[i] + array[left] + array[right]) > targetSum:
				#decrement the right pointer
				right -= 1

	return threeNumSums
    pass


{% endhighlight %}

# Code Explanation:
Alright lets keep this short.  SO whats happening is that the best way to see if we have a triplet that matches the target sum is to first sort the array. That way we can establish three pointer. An i, left pointer that starts at i + 1 and a right pointer that starts at the very last element. The pointer are named in the direction that they are going to move in. We then trigger the while loop and this engages until the pointers meet up at the same element in the array meaning that all possible types of combination have been attempted with the current i element. If the three pointers sum up to less than the target sum we know to move the left pointer. If the three pointers sum up to move than the target sum we know to move the right pointer to decrease the value of the summation of the three pointers. And if the three pointers add up the the target sum, we append them in a 2D array and then move both the left and right pointers in their respective directions to see if that i pointer still has any other potential matches in the array. 
