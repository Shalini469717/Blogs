---
title: "Bubble, Selection, and Insertion Sort: Classic Sorting Algorithms Revisited"
seoTitle: "Sorting Algorithms"
seoDescription: "sorting algorithms bubble sort selection sort insertion sort"
datePublished: Mon Jun 12 2023 07:13:21 GMT+0000 (Coordinated Universal Time)
cuid: clisipfuf000v09mbcymuf1uy
slug: sorting-algorithms
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1686553394448/2d28f387-45c6-43cb-a4ae-1e48090e7e7b.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1686553730535/921ba8a4-b162-441c-9fab-83aac07ae92c.png
tags: algorithms, programming-blogs, programming, sorting, dsa

---

# Introduction

In this blog, I will be explaining various sorting techniques used to sort an array and explain them with the help of a visualizer. In case you are a beginner and are learning all these techniques, first let me tell you all the techniques I will explain in this blog: Bubble sort, Selection sort, and Insertion sort.

# Do I need to learn all these?

You might be thinking "Do I need to learn all these? Let me learn the most efficient one and get done with it".

All these have different approaches as bubble sort, selection sort, and insertion sort are based on incremental approaches whereas merge sort and quick sort are based on divide and conquer. Simply sorting only may not be always the requirement. The requirements can be different. You may need to modify/integrate a sorting algorithm in order to develop a completely different thing. The predefined sorting methods may not be efficient in all cases.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1686398178078/e0ba63be-f31f-4786-b9a9-fc237c1fe540.webp align="center")

I know people who are using Python just get done with `.sort()` and cpp people as far as I know use similar sort methods too. I use Python as well but in one of the contests I saw a question that asked about the number of swaps in bubble sort. I had to write the algo and solve it. So, unless the questions you solve just involve sorting and do not require you to modify the algorithm in place you can use the inbuilt methods.

In this blog, we will analyze their complexities and go from the algorithm having higher time complexity to lower time complexity. It might seem overwhelming and you might try to memorize the code, but trust me once you understand the working of the algorithm, you will be able to write the code yourself.

Feel free to skip to a specific technique in case you are familiar with the others.

# Bubble Sort

Let's get started with the good old bubble sort. First, just focus on understanding what it is, you will be able to write the code on your own.

If I have to say about bubble sort in one sentence - It is just comparing with the immediate neighbor element and swapping. You start from the beginning of the array and keep on comparing the elements and swapping. Let's understand it with an example array and we are sorting it in ascending order.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1686398157868/24eb24e4-1e90-4d27-9196-626e3fd0ddb1.webp align="center")

Let's start with the beginning of the array. Let's take two-pointers or rather markers say i and j. Since it is the beginning of the array, the starting pointer would be i and its value is 0. So i = 0. Now you need to take another pointer j which starts from the beginning and we use this pointer to compare the element with its neighboring element. Note that the swapping occurs if the element at the j index is greater than the element at index j+1. Else we keep on incrementing the value of j.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1686403740922/f196c110-5a1a-4b36-982e-3c6e253124c0.png align="center")

Now compare 6 and 5. Since 6 is greater than 5, swap 6 and 5 and increment j.

Now the value of j is 1. Similarly, follow the subsequent steps where we are still in index i = 0 but the value of j is being incremented while comparing.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1686468459051/29bb9e95-421e-4b1f-9991-c13b2049183b.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1686468709243/778657b2-3d7d-47a9-a0c9-880e3ef55438.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1686468544952/6d418874-70f1-41f4-8654-e1203957055c.png align="center")

Some important things to note here.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1686470705009/08ddbf9c-59da-494f-aaf0-019d4bebf0f1.png align="center")

1. You can observe that 8 is the last element in the array after doing the algo for i = 0. And what more? 8 is also the greatest element in the array. So, what did this algo do in this pass? It brought the greatest element to the end of the array. A similar thing happens in the subsequent passes for i = 1, 2...n-1.
    
2. In each pass, the greater elements keep accumulating in the end. So, by the end of the first pass i.e. when i = 0, the greatest element is at index n-1. By the end of the second pass i.e. when i = 1, the second greatest element is at index n-2. This means that the array is unsorted till n-2 elements as the last 2 elements are sorted.
    
3. So, you can move j values from 0 to n-i-1. Since the last i+1 elements are sorted, you just need to iterate over the unsorted part which is the n-i-1 elements.
    
4. This was done for index i = 0 and we need to do it until i = n-1 times.
    

Use pen and paper to trace out the further steps and cross-check them with the help of the visualizer provided below. Here is a video for the same, you can understand it more clearly.

<iframe src="https://www.veed.io/embed/21c22712-ec8d-4595-b695-81cc6bbcfb79" width="744" height="504"></iframe>

You can try out these visualizers to visualize each step :

[Bubble Sort visualize | Algorithms | HackerEarth](https://www.hackerearth.com/practice/algorithms/sorting/bubble-sort/visualize/)

[Sorting (Bubble, Selection, Insertion, Merge, Quick, Counting, Radix) - VisuAlgo](https://visualgo.net/en/sorting)

## Code for Bubble sort

```c
void bubbleSort(int arr[], int n) {
  for (int i = 0; i < n-1; i++) {
    // loop to compare array elements
    for (int j = 0; j < n-i-1; j++) {
      // compare two adjacent elements
      // change > to < to sort in descending order
      if (arr[j] > arr[j + 1]) {
        // swapping elements
        int temp = arr[j];
        arr[j] = arr[j + 1];
        arr[j + 1] = temp;
      }
    }
  }
}
```

You can practice it here: [Bubble Sort | Practice | GeeksforGeeks](https://practice.geeksforgeeks.org/problems/bubble-sort/1)

## Time Complexity of Bubble sort

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1686398201474/4f1ee7fe-f679-4fc2-ba37-62635246c6bf.png align="center")

Since the outer for loop iterates for n times and the inner for loop iterates n times, each time the outer for loop is executed. Hence, the total iterations would be n². So, the time complexity of bubble sort is O(n²). Since it doesn't take up extra space, it is called an in-place sorting algorithm.

# Selection Sort

This one is rather simple and probably one of the techniques we would use even if we have no knowledge about Data Structures or coding. You divide the array into sorted and unsorted parts. You traverse the unsorted part of the array and find the minimum element and place it in the sorted part. That's it nothing more. Let's check this out with an example array.

This is much easier to understand if you already know how to find the minimum element in the array.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1686472496408/8c0d62e8-fbc2-49a0-aebd-1c0ebb3d105a.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1686472553042/c6b6f61b-8499-422b-b8f9-6729ea0fd21f.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1686472568068/6b6440fa-9cac-4a77-8065-3388fe589b90.png align="center")

Now repeat this for i=1,2, ... until n-1. The array will be sorted.

Things to note:

First i+1 elements will be sorted, so it is the sorted part of the array. You will find the minimum element from the unsorted array and swap it with the first element of the unsorted part of the array. This way the entire array will be sorted. Check out the video below to know what happens in the further passes.

<iframe src="https://www.veed.io/embed/4918631d-28cf-4f80-81d5-e9439e04b055" width="744" height="504"></iframe>

You can try out these visualizers to visualize each step :

[Selection Sort visualize | Algorithms | HackerEarth](https://www.hackerearth.com/practice/algorithms/sorting/selection-sort/visualize/)

[Sorting (Bubble, Selection, Insertion, Merge, Quick, Counting, Radix) - VisuAlgo](https://visualgo.net/en/sorting)

## Code for Selection Sort

```cpp
void selectionSort(int arr[], int n)
{
    int i, j, min_idx;
    // One by one move boundary of unsorted subarray
    for (i = 0; i < n-1; i++)
    {
        // Find the minimum element in unsorted array
        min_index = i;
        for (j = i+1; j < n; j++)
          if (arr[j] < arr[min_index])
            min_index = j;
 
        // Swap the found minimum element with the first element
           if(min_index != i)
            swap(arr[min_index], arr[i]);
    }
}
```

You can practice it here: [Selection Sort | Practice | GeeksforGeeks](https://practice.geeksforgeeks.org/problems/selection-sort/1)

## Time Complexity of Selection Sort

The time complexity of finding the minimum element in a sub-array takes O(n) time where n is the number of elements in the unsorted sub-array. As we will need to traverse the entire unsorted sub-array of size n for finding the minimum element so the time complexity of searching comes out to be O(n). Now, after the searching, we will be performing the swapping (if needed) but the swapping is a constant time operation i.e. it takes only O(1) time hence it will not affect the overall time complexity of the selection sort.

Now, for each of the n iterations, we perform the searching and swapping so the time complexity of the selection sort becomes O(n²).

Since we are swapping and not using any extra space, space complexity is O(1) and it is also an in-place sorting algorithm.

# Insertion Sort

This is also simple to understand because it is what you would be doing if you were given a bunch of cards with numbers and told to sort them out. In this sorting technique, you pick a number from the array sequentially and insert it into the right position.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1686398166397/c646336e-1e6e-4578-a7cf-ffb3644f80df.jpeg align="center")

Let's understand it with the help of an example.

Remember you just need to pick the element and insert it in the right position.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1686549203886/584eb198-f4a1-4977-8303-9dd452f0b65f.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1686549249819/8053ce67-2041-4639-bb72-a8a584b1689f.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1686549260415/e7303f15-4c15-4681-919d-882c5e9ea0e9.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1686549274105/598a42a1-759f-4830-a9a8-35fc04c3ee79.png align="center")

Things to note:

When we are inserting the element into the sorted part of the array say `key`, we need to compare the key with the existing elements in the array and move the elements greater than the key by one step to the right. Look at the video to get a better understanding.

<iframe src="https://www.veed.io/embed/68bc68f8-c928-4363-b80e-6f3011216c80" width="744" height="504"></iframe>

You can try out these visualizers to visualize each step :

[Insertion Sort visualize | Algorithms | HackerEarth](https://www.hackerearth.com/practice/algorithms/sorting/insertion-sort/visualize/)

[Sorting (Bubble, Selection, Insertion, Merge, Quick, Counting, Radix) - VisuAlgo](https://visualgo.net/en/sorting)

## Code for insertion sort

```c
void insertionSort(int arr[], int n)
{
    int i, key, j;
    for (i = 1; i < n; i++) {
        key = arr[i];
        j = i - 1;
 
        /* Move elements of arr[0..i-1], that are greater than key, 
        to one position ahead of their current position */
        while (j >= 0 && arr[j] > key) {
            arr[j + 1] = arr[j];
            j = j - 1;
        }
        arr[j + 1] = key;
    }
}
```

You can practice it here: [Insertion Sort | Practice | GeeksforGeeks](https://practice.geeksforgeeks.org/problems/insertion-sort/1)

## Time Complexity of Insertion Sort

The simplest worst-case input is an array sorted in reverse order. The set of all worst-case inputs consists of all arrays where each element is the smallest or second-smallest of the elements before it. In these cases, every iteration of the inner loop will scan and shift the entire sorted subsection of the array before inserting the next element. This gives insertion sort a quadratic running time i.e. O(n<sup>2</sup>).

# Summary

In Bubble sort, you compare the adjacent elements and keep on swapping if required while incrementing the j value to get the largest element at the end of the array.

In Selection sort, you take the minimum element from the unsorted part and swap it with the first element of the unsorted array.

In Insertion sort, you take the element and insert it in the correct position in the sorted array.

All these algorithms have O(n\*n) time complexity and O(1) space complexity and are called in-place sorting algorithms.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1686550924641/65300cad-5dca-4ad9-8c34-961123b36a65.webp align="center")

Due to the higher time complexity, these algorithms take a huge time for sorting larger datasets. I will be explaining sorting techniques that take much lesser time than these and why minimizing the time complexity is important in the upcoming blog.

# Let's Connect

Twitter: [**Shalini Muskula (@noname469717) / Twitter**](https://twitter.com/noname469717)  
Github: [**Shalini469717 (Shalini) (**](https://github.com/Shalini469717)[**github.com**](http://github.com)[**)**](https://github.com/Shalini469717)  
LinkedIn : [**Shalini Muskula | LinkedIn**](https://www.linkedin.com/in/shalini-muskula-52323922a/)

# References

[Why do We Need Sorting Algorithms? (](https://www.enjoyalgorithms.com/blog/why-should-we-learn-sorting-algorithms)[enjoyalgorithms.com](http://enjoyalgorithms.com)[)](https://www.enjoyalgorithms.com/blog/why-should-we-learn-sorting-algorithms)

[Insertion Sort - Data Structure and Algorithm Tutorials - GeeksforGeeks](https://www.geeksforgeeks.org/insertion-sort/)

[Insertion sort - Wikipedia](https://en.wikipedia.org/wiki/Insertion_sort)

[Sorting (Bubble, Selection, Insertion, Merge, Quick, Counting, Radix) - VisuAlgo](https://visualgo.net/en/sorting?slide=1)

Memes: [Sorting Meme Review » PREP INSTA](https://prepinsta.com/sorting-meme-review/)