---
layout:     post
title:      Caesar Cipher Encryptor
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

Given a non-empty string of lowercase letters and a non-negative integer representing a key write a function that returns a new string obtained by shifting every letter in the inout string by k positions in the alphabet, where k is the key.

Note that letters should "wrap" around the alphabet; in other words, the letter `z` shifted by one returns the letter `a`.

If you are unfamiliar with the [asciitable][1] please check it out [here][1].

{% highlight ruby %}
def caesarCipherEncryptor(string, key):
    # Write your code here
	#time O(n) space = o(n)
	key = key % 26
	newString = ""
	for char in string:
		x = key + ord(char)

		if x > ord("z"):
			x =  (x - 26)

		newString += chr(x)

	return newString

{% endhighlight %}

# Code Explanation:
The easiest way that I found to complete this question is by making a method that passes in a string and a key. The first thing I do is mod the key by 26, which is the length of total letters in the alphabet. The reason I decided to do this was to help in wrapping the letters across the alphabet if the number for the key given was greater than 26. Next I created a new string that will hold the encrypted string and will be returned. After that I wrote a for loop which traverses each character in the string. a variable named X is set to the key + the ASCII value of the letter that is currently being indexed of the string. The reason we take the ASCII value is so that we can just loop to the front later if we have to pass `z`. The if statement under the assignment of the variable x actually takes care of that for us. For example, say the word is "wall" and the key is 15. The lower case letter `w` has an ASCII value of 120. 15 % 26 is just 15, so 120 + 15 = 135. 135 is greater than the ASCII value of `z` which is 122. This is when the if statement is executed and then subtracts 26 from the value of X to reposition it back within  the range of ASCII values of the alphabet. 135 - 26 = 110. The letter with the ASCII value of 110 is n. This is how the "wrapping" happens. Lastly, we then read in the character value of the ASCII number that X contains and then return the string back to the main.

[1]: [http://www.asciitable.com]
