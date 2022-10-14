## Selection Sort:

- Takes the first index
- Iterates over the whole array to find the index of the smallest number 
- swaps the number\
**Time Complexity: O(N<sup>2</sup>)**\
**Auxiliary Space: O(1)**

Lets consider the following array as an example: arr[] = {64, 25, 12, 22, 11}

**First pass:**

For the first position in the sorted array, the whole array is traversed from index 0 to 4 sequentially. The first position where 64 is stored presently, after traversing whole array it is clear that 11 is the lowest value.
   64      25      12      22      11   
Thus, replace 64 with 11. After one iteration 11, which happens to be the least value in the array, tends to appear in the first position of the sorted list.
   11      25      12      22      64   
   
**Second Pass:**

For the second position, where 25 is present, again traverse the rest of the array in a sequential manner.
   11      25      12      22      64   
After traversing, we found that 12 is the second lowest value in the array and it should appear at the second place in the array, thus swap these values.
   11      12      25      22      64   
   
**Third Pass:**

Now, for third place, where 25 is present again traverse the rest of the array and find the third least value present in the array.
   11      12      25      22      64   
While traversing, 22 came out to be the third least value and it should appear at the third place in the array, thus swap 22 with element present at third position.
   11      12      22      25      64   
   
**Fourth pass:**

Similarly, for fourth position traverse the rest of the array and find the fourth least element in the array 
As 25 is the 4th lowest value hence, it will place at the fourth position.
   11      12      22      25      64
   
**Fifth Pass:**

At last the largest value present in the array automatically get placed at the last position in the array
The resulted array is the sorted array.
   11      12      22      25      64   

<hr/>

## Bubble Sort

- Takes first two elements then swaps the smaller one to the left and keeps repeating till the end of the array.
- keeps iterating until there is no element swapped\
**Time Complexity: O(N<sup>2</sup>)**\
**Auxiliary Space: O(1)**


Input: arr[] = {5, 1, 4, 2, 8}

First Pass: 

Bubble sort starts with very first two elements, comparing them to check which one is greater.( 5 1 4 2 8 ) –> ( 1 5 4 2 8 ), Here, algorithm compares the first two elements, and swaps since 5 > 1.\
( 1 5 4 2 8 ) –>  ( 1 4 5 2 8 ), Swap since 5 > 4\
( 1 4 5 2 8 ) –>  ( 1 4 2 5 8 ), Swap since 5 > 2\
( 1 4 2 5 8 ) –> ( 1 4 2 5 8 ), Now, since these elements are already in order (8 > 5), algorithm does not swap them.

Second Pass: 

Now, during second iteration it should look like this:( 1 4 2 5 8 ) –> ( 1 4 2 5 8 )\
( 1 4 2 5 8 ) –> ( 1 2 4 5 8 ), Swap since 4 > 2\
( 1 2 4 5 8 ) –> ( 1 2 4 5 8 )\
( 1 2 4 5 8 ) –>  ( 1 2 4 5 8 )

Third Pass: 

Now, the array is already sorted, but our algorithm does not know if it is completed.\
The algorithm needs one whole pass without any swap to know it is sorted.( 1 2 4 5 8 ) –> ( 1 2 4 5 8 )\ 
( 1 2 4 5 8 ) –> ( 1 2 4 5 8 )\
( 1 2 4 5 8 ) –> ( 1 2 4 5 8 )\
( 1 2 4 5 8 ) –> ( 1 2 4 5 8 )

