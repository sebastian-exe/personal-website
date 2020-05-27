---
layout:     post
title:      Print Out All Possible Pairs
date:       2020-05-26 12:17:36
author:     Sebastian Moreno
summary:    This is the inaugural post of my interview coding questions.
categories: LeetCode
thumbnail: python
tags:
 - demo
 - action
 - carte
 - noire
---

There is a list of people containing strings representing the names of some people. Write a nested loop that prints out all possible pairs of these people that can make up a group of two. So for example, your loop should print out:

* Tim, Jeff
* Tim, Elon
* Tim, Bill
* Jeff, Elon
* Jeff, Bill
* Elon, Bill


{% highlight ruby %}
people = ["Tim", "Jeff", "Elon", "Bill"]

#write your solution below:
for i in range(len(people)):

  for j in range(i + 1, len(people)):

    print(people[i], people[j])
{% endhighlight %}

## Code Explanation:

The first for loop reaches the 0th index, in this case "Tim". Next the code enters the
second (j) for loop which starts at i + 1 index or in other words, one ahead of the i for loop,
in this case at "Jeff". The second for loop iterates through the entire list while the first loop
remains at the 0th index of "Tim". Once the second for loop has iterated and printed (third line of code)
all the possible combinations of names that Tim can produce the first for loop now moves onto the 1st index.
After this the process starts again with the second for loop and continues until all of the names have been
printed with all possible combinations.
