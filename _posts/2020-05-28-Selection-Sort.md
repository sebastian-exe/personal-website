---
layout:     post
title:      Selection Sort
date:       2020-05-28 12:31:19
summary:    See what the different elements looks like.
categories: LeetCode
thumbnail: python
tags:
 - demo
 - action
 - carte
 - noire
---

Write a function that takes in an array of integers and returns a sorted version of that array. Use the Selection Sort algorithm to sort the array.

## What is Selection Sort?
**Note** If you are not familiar with [selection sort][1] please read more about it [here][1] before attempting the problem.
The basic gist of the selection sorting algorithm is that it takes an unsorted array, traverses it, and then places the smallest current element at
that at the beginning of the array. This is done repeatedly until the array is entirely sorted.

## Here is an example:
Say we have a given array such as arr = [1 , 4 , 2 , 3 , 5 , 0]. First selection sort would traverse the array keeping in mind the smallest element. Once the smallest
element has been encountered it places that element to the very front of the array.

1. <ins>The First pass would look like this:</ins>
* [0 , 1 , 4 , 2 , 3 , 5]

2. <ins>The second pass would look like this:</ins>
* **Note** Since 1 is already the following smallest element, nothing is changed during this pass.
* [0, 1 , 4 , 2 , 3 , 5]

3. <ins>The third pass would look like this:</ins>
* [0 , 1 , 2 , 4 , 3 , 5]

4. <ins>The fourth pass would look like this:</ins>
* [0 , 1 , 2 , 3 , 4 , 5]
* **Note** that this is the final pass since at this point in time all of the elements are in the proper order.

Now that we understand conceptually what is happening with selection sort, lets attempt to understand the code.
{% highlight ruby %}

  def selectionSort(array):

    #we must traverse through all elements in the array
    for i in range(len(array)):

      #find the minimum element in remaining unsorted array
      int minIndex = i;

      for j in range(i+1, len(array)):
        #if we find a new element that is smaller than our currently recorded element
        if[minIndex] > array[j]:
        #make that element the new smallest index
          minIndex = array[j]

        #perform a swap
        array[i], array[minIndex] = array[index], array[i]

{% endhighlight %}



[1]: https://www.geeksforgeeks.org/selection-sort/
[2]: https://noahfrederick.com/log/lion-terminal-theme-peppermint/
[3]: https://github.com/jacobtomlinson/carte-noire
[4]: http://pixyll.com/
