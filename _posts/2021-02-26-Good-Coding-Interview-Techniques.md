---
layout:     post
title:      Good Coding Interview Techniques 
date:       2021-02-26 10:30:00
author:     Sebastian Moreno
summary:    Tips to ace that coding Interview
categories: LeetCode
thumbnail: python
tags:
 - demo
 - action
 - carte
 - noire
---

## <ins>**Introduction**</ins>
When starting a coding interview it is important to remain calm. The night before I recommend getting plenty of rest so that you are able to be fresh and have a sharp mind during the interview. I will now list some tips that I recommend everyone should follow to be able to ensure the optimal amount of success in an interview scenario and ultimately securing an offer.

* Start studying 4 - 6 weeks before an interview. 
* Remember to apply early as this industry is very competitive
* Pick a language that you are cofortable with and stick with it, I suggest python3
* Study 1 to 2 questions a day to prevent burn out. 
* Ensure that you are comfortable with Big-O notation and space complexities. 
* Don't get discourage! There are tons of great places to work. 

## <ins>**How to approach an Internview**</ins>
* The first 5 - 10 minutes: 
One of the most important and overlooked things in an interview situation is that you first talk out your thought process with the interviewer. Do not begin writting code until you have clearly stated what you're thinking and why you think your currently psuedocode solution will work. At this time it is not necessary to state hypothetical run time complexities. Also, it is extremely important that you start to ask questions about the test cases. Many times the interviewers will not provide all the base cases for you and expect the interviewee to ask questions and uncover the edge test cases.
* The next 11 - 45 minutes:
Start to write your solution. Remember to use good variable names here and write clean and readable code. Always continue to speak why you code to the interviewer so that you are clearly communicating your ideas to them. If you get stuck and do not know how to solve the question at this point it is important not to freak out. Ask the interviewer questions that might help uncover any tips or help you think through the questions differently.
* The last 15 minutes (45 - 60 minutes):
Talk through your solution with the interviewer. Here it is now expected that you state the run time and space complexity for your solution. The interviewer might begin to ask questions as to why you solved the question in a specific manner and can potentially ask you if there are any other available solutions for that problem. At the end of the interview the interviewer will most likely ask you if you have any questions for them. At this point I always suggest asking why they chose to be at *insert company name*. It is always insightful to hear from other students.

# Code Explanation:
Alright lets keep this short.  SO whats happening is that the best way to see if we have a triplet that matches the target sum is to first sort the array. That way we can establish three pointer. An i, left pointer that starts at i + 1 and a right pointer that starts at the very last element. The pointer are named in the direction that they are going to move in. We then trigger the while loop and this engages until the pointers meet up at the same element in the array meaning that all possible types of combination have been attempted with the current i element. If the three pointers sum up to less than the target sum we know to move the left pointer. If the three pointers sum up to move than the target sum we know to move the right pointer to decrease the value of the summation of the three pointers. And if the three pointers add up the the target sum, we append them in a 2D array and then move both the left and right pointers in their respective directions to see if that i pointer still has any other potential matches in the array. Note! Something that is important to realize is that the for loop loops until len(array)-2. The reason it loops until -2 is because you need to loop the i and still make sure that you're leaving room for the left and right pointers in the for loop while looping. If you don't do this you may get an out of bounds error.
