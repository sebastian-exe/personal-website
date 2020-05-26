---
layout:     post
title:      Print Out All Possible Pairs
date:       2020-05-26 12:17:36
summary:    This is the inaugural post of my interview coding questions.
categories: jekyll
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

for i in range(len(people)):

  for j in range(i + 1, len(people)):

    print(people[i], people[j])
{% endhighlight %}
