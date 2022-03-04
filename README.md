# Bitonic-Sort
Python Program for Bitonic Sort
A sequence is called Bitonic if it is first increasing, then decreasing. In other words, an array arr[0..n-i] is Bitonic if there exists an index i where 0<=i<=n-1 such that 

x0 <= x1 …..<= xi  and  xi >= xi+1….. >= xn-1 
A sequence, sorted in increasing order is considered Bitonic with the decreasing part as empty. Similarly, decreasing order sequence is considered Bitonic with the increasing part as empty.
A rotation of Bitonic Sequence is also bitonic.
Bitonic Sorting

It mainly involves two steps.  

Forming a bitonic sequence (discussed above in detail). After this step we reach the fourth stage in below diagram, i.e., the array becomes {3, 4, 7, 8, 6, 5, 2, 1}
Creating one sorted sequence from bitonic sequence: After first step, first half is sorted in increasing order and second half in decreasing order. 
We compare first element of first half with first element of second half, then second element of first half with second element of second and so on. We exchange elements if an element of first half is smaller. 
After above compare and exchange steps, we get two bitonic sequences in array. See fifth stage in below diagram. In the fifth stage, we have {3, 4, 2, 1, 6, 5, 7, 8}. If we take a closer look at the elements, we can notice that there are two bitonic sequences of length n/2 such that all elements in first bitonic sequence {3, 4, 2, 1} are smaller than all elements of second bitonic sequence {6, 5, 7, 8}. 
We repeat the same process within two bitonic sequences and we get four bitonic sequences of length n/4 such that all elements of leftmost bitonic sequence are smaller and all elements of rightmost. See sixth stage in below diagram, arrays is {2, 1, 3, 4, 6, 5, 7, 8}. 
If we repeat this process one more time we get 8 bitonic sequences of size n/8 which is 1. Since all these bitonic sequence are sorted and every bitonic sequence has one element, we get the sorted array.
