---
title: Sorting Algorithms and types
layout: post
tags: [Coding]
date: 2020-05-07
image: images/algorithms.jpg

---

In general, Sorting is the process of arranging objects in an orderly fashion. The order could be based on any property of the object.

In Computer Domain, sorting refers to process of arranging objects in a list in ascending or descending order. 

##### Why is sorting required?
Sorting is one of the very basic algorithms in computer science. A great amount of research work has already been performed by academia in this field to search for the most optimized versionn of a sorting algorithm. But Why is sorting required??  
Sorting enables quick search of elements in the list, gives a way of comparing data in least time etc. There are often times while searching for a product online we want to bbuy the cheapest option available. In this case we can sort elements in ascending order and get the product with smallest value/price.

##### Types of sorting algorithms
Many Sorting algorithms have been experimented and documented till date. Each of them having their own advantage and disadvantages depending on the use case scenarios. Some of them are simple and easy to implement, while some are faster than others in specific cases, while some handles the memory constraint better etc.

* Selection Sort
* Insertion Sort
* Bubble Sort
* Merge Sort
* Heap Sort
* Quick Sort etc.

###### Selection Sort
```
time Complexity: O(n^2)  
space Complexity: O(n)
```

As the name suggests, select the smallest element in unsorted list and place in sorted list. The unsorted list is the availble list. The requirment of another sorted list can be achieved by dividing the original list in two halves by an index. Such that one part beahves as sorted list and another is unsorted one. Pick smallest element from unsorted list and add it to sorted list.  
Here is sample code in python for insertion sort.	

```
for i in range(len(A)): 
      
    # Find the minimum element in remaining  
    # unsorted array 
    min_idx = i 
    for j in range(i+1, len(A)): 
        if A[min_idx] > A[j]: 
            min_idx = j 
              
    # Swap the found minimum element with  
    # the first element         
    A[i], A[min_idx] = A[min_idx], A[i] 
```

###### Insertion Sort
```
time Complexity: O(n^2)  
space Complexity: O(n)
```
Insertion also follows similar principle as Selection Sort. Both of them are quite similar. 
```
# Traverse through 1 to len(arr) 
    for i in range(1, len(arr)): 
  
        key = arr[i] 
  
        # Move elements of arr[0..i-1], that are 
        # greater than key, to one position ahead 
        # of their current position 
        j = i-1
        while j >= 0 and key < arr[j] : 
                arr[j + 1] = arr[j] 
                j -= 1
        arr[j + 1] = key 
```

###### Bubble Sort
```
time Complexity: O(n^2)  
space Complexity: O(n)
```
Bubble sort works on elements in pair and sorts them accordingly.
```
n = len(arr) 
   
    # Traverse through all array elements 
    for i in range(n): 
        swapped = False
  
        # Last i elements are already 
        #  in place 
        for j in range(0, n-i-1): 
   
            # traverse the array from 0 to 
            # n-i-1. Swap if the element  
            # found is greater than the 
            # next element 
            if arr[j] > arr[j+1] : 
                arr[j], arr[j+1] = arr[j+1], arr[j] 
                swapped = True
  
        # IF no two elements were swapped 
        # by inner loop, then break 
        if swapped == False: 
            break
``` 