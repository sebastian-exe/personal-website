---
layout:     post
title:      Product Sum (incomplete)
date:       2020-06-02 5:38:19
author:     Sebastian Moreno
summary:    Special Array question
categories: LeetCode
thumbnail: python
tags:
 - demo
 - action
 - carte
 - noire
---

Write a function that takes in a "special" array and returns its product sum. A "special" array is a non-empty array that contains either integers or other "special" arrays. The product sum of a "special" array is the sum of its elements,  where "special" arrays inside it are summed themselves and then multiplied by their level of depth

<ins>For Example</ins> the product sum of `[x,y]` is `x + y`; the product sum of `[x, [y,z]]` is `x + 2y + 2z`.


{% highlight ruby %}

# Tip: You can use the type(element) function to check whether an item
# is a list or an integer.
def productSum(array, bm = 1):
    # Write your code here.
	prodSum = 0

	for i in array:
		print(i)			
		if type(i) is list:
			print("successfully entered list")
			prodSum += productSum(i, bm + 1)

		elif type(i) is int:
			prodSum += i
			print("prodSum: ", prodSum)

	print("prodSum: ", prodSum)
	return prodSum * bm


{% endhighlight %}

# Code Explanation:
First you want to initialize a variable to contain the sum. After this you want to loop through the array checking the type of element in the array with the built in type function in python. If the type of the element matches to list this means that we've entered a bracket. Think of entering a bracket as entering a new array where you must add the numbers within that array, take care of the multiplication factor, and then return that and add that new number to the prodSum before entering the bracket. The way we take care of this is through recursion.

<ins>For Example: </ins> lets take this example array of [5, 2 [7, -1]]. According to the attributes of the special array the result of this would be 19. Heres how the code handles this. As the code is looping through the array and we see that the type of 5 is an integer the code will enter the elif statement. Here we will add 5 to the prodSum which is currently 0 incrementing the value to of prodSum to 5. After that we move onto the next character in the array. The next character is 2. Again, within the for loop we enter the elif statement adding 2 to the existing value of prodSum, making prodSum have a total of 7 now. Next a bracket is encountered while looping through the array. Here instead of entering the elif statement we enter the if statement because a bracket is of type list and not of type integer. Within the if statement you will see that the value of prodSum is set to be added to the result of a recursive call of the productSum method. Remember, that the characteristics of the special array is that when a bracket is encountered you must multiply the result of adding the numbers within the bracket by the number of level deep the bracket is. In this case, the bracket in front of the 7 is 2 levels deep (notice the first bracket in front of the 5. ) To take care of this factor we add one to the variable called bm which is short for base multiplier. Now we must enter the recursive call. The function is passes a 7 which adds that to the now reinitialized variable of prodsum to 0 (only during this recursive call, once we exit we will add it back to the existing value of prodsum). The same happens for the -1. The value of prodsum at the end of this is 6. If you see, the return statement multiplies the value of prodSum by the base multiplier value, thus returning a value of 12 from the recursive call and ending the recursive call. The value of 12 is then added to the existing value of prodSum before the recursive call was made which was 7. Now prodSum is equal to 19. The for loop reaches the end of the array and returns 12 multiplied by the base multiplier of one (since all other brackets have been exited). 
