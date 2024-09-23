---
title : "Sorting algorithms"
date :  "`r Sys.Date()`" 
weight : 3 
chapter : false
pre : " <b> 3. </b> "
---
Sorting algorithms are used to rearrange a given list of elements according to a comparison operator on the elements. There are many different sorting algorithms, each has its own advantages and limitations. We will discover these following three sorting algorithms: ***selection, bubble, and merge sort***

#### Selection sort

Selection sort algorithm works by finding the minimum element in the unsorted portion of the array and swapping it with the first unsorted element. Repeat until the array is fully sorted.

We can represent an array as follows:

![flowchart](https://raw.githubusercontent.com/baobaoupcloud/cs-w3/main/static/images/3.sortingalgorithms/sorting1.png)

The algorithm for selection sort in pseudocode is:

```bash
For i from 0 to n–1
    Find smallest number between numbers[i] and numbers[n-1]
    Swap smallest number with numbers[i]
```

It has the time complexity of O(n²), Ω(n²). This algorithm is simple to understand and implement. It is inefficient for large datasets, especially when the data is nearly sorted.

#### Bubble sort

This sorting algorithm works by repeatedly swapping elements to “bubble” larger elements to the end.

The pseudocode for bubble sort is:

```bash
Repeat n-1 times
    For i from 0 to n–2
        If numbers[i] and numbers[i+1] out of order
            Swap them
    If no swaps
        Quit
```

Analyzing bubble sort, the time complexity is O(<math xmlns="http://www.w3.org/1998/Math/MathML">
<msup>
<mi>n</mi>
<mn>2</mn>
</msup>
</math>), for the worst case and Ω(n) for the best case. Bubble sort is a simple approach. It is efficient for small datasets or nearly sorted data. But it is comparatively a slow algorithm, not suitable for large arrays.

#### Merge sort

Merge sort is a sorting algorithm that follows the divide-and-conquer approach. It works by recursively dividing the input array into smaller subarrays and sorting those subarrays then merging them back together to obtain the sorted array.

The pseudocode for merge sort is:

```bash
If only one number
    Quit
Else
    Sort left half of number
    Sort right half of number
    Merge sorted halves
```

For example the following list of numbers:

`6 3 4 1`

First, merge sort asks, “is this one number?” The answer is “no,” so the algorithm continues.

Second, merge sort will now split the numbers down the middle (or as close as it can get) and sort the left half of numbers.

`6 3 | 4 1`

Third, merge sort would look at these numbers on the left and ask, “is this one number?” Since the answer is no, it would then split the numbers on the left down the middle.

`6 | 3`

Fourth, merge sort will again ask , “is this one number?” The answer is yes this time! Therefore, it will quit this task and return to the last task it was running at this point:

`6 3 | 4 1`

Fifth, merge sort will sort the numbers on the left.

`3 6 | 4 1`

Now, we return to where we left off in the pseudocode now that the left side has been sorted. A similar process of steps 3-5 will occur with the right-hand numbers. This will result in:

`3 6 | 1 4`

Both halves are now sorted. Finally, the algorithm will merge both sides. It will look at the first number on the left and the first number on the right. It will put the smaller number first, then the second smallest. The algorithm will repeat this for all numbers, resulting in:

`1 3 4 6`

Merge sort is complete, and the program quits.

Merge sort is a very efficient sort algorithm with a worst case of O(n log n). The best case is still Ω(n log n) because the algorithm still must visit each place in the list.

In summary, ***Merge sort*** is generally the best choice for large datasets due to its efficiency but it requires extra space to store the merged subarrays. ***Selection and Bubble Sort*** are simpler to implement but are not suitable for large inputs.

And that’s the end of week 3.
