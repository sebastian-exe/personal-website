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

array = [8,5,2,9,5,6,3]

 #Space = O(1), Time = O(N^2)
def selectionSort(array):

    #first for loop, iterates through setting up the first value as the minVal
    for i in range(len(array)):
        minIndex = i
        #second for loop traverses the rest of the array making comparisons

        for j in range(i + 1, len(array)):
            #if there is a new value that is smaller than the currently known min value
            if array[minIndex] > array[j]:
                #make that new smallest value the minVal
                minIndex = j
        #swap
        temp = array[i]
        array[i] = array[minIndex]
        array[minIndex] = temp
    #once you're at the end of the first for loop, return the newly sorted array
    return array


print(selectionSort(array))


{% endhighlight %}

## Code Explanation:

Basically how selection sort works is that the first for loop starts at the 0th index. It then saves that index into the minIndex value. Next the code enters the second for loop. This " j " for loop starts at i + 1 index or in other words the first index. Within the second(j) for loop, there is a if statement. This if statement is entered if while traversing the rest of the unsorted array there is a new smaller value than that of the index of the first for loop, or in this case the element stored in the 0th index. If the if statement is entered then we must set the minIndex to be the index of that newly found smallest element. Before returning to the outer ("i") for loop, a swap must be performed placing the smallest value at the front of the array.

<ins>How the swap works:</ins> So think of it like this. Remember how the first for loop stops at the 0th index and then enters the second for loop? Well the element within that 0th index is stored within a temporary variable. Think of it as holding you phone in one hand and a book in the other and the temporary variable as a table. If you want to put the book in the opposite hand you must first put the phone on the table, swap hands, and then pick the phone back up. So here we are putting that value on the "table". Next we set the newly found smallest variable as the value at array[i]. What is actually happening here is that we are transferring the smallest value to the front of the list. The line of code that says array[minIndex] = temp is literary placing that bigger value into the spot where the smallest value used to be.  

[1]: https://www.geeksforgeeks.org/selection-sort/
