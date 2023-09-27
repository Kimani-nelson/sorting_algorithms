Sorting Algorithms and Big O Analysis

Introduction

Sorting is a fundamental operation in computer science and is used in a wide range of applications. Sorting algorithms are designed to arrange a list of elements in a specific order, such as ascending or descending. The efficiency of sorting algorithms is a critical consideration, especially when dealing with large datasets. This README provides an overview of common sorting algorithms and their Big O analysis, which describes their computational complexity.

Table of Contents

Common Sorting Algorithms

Bubble Sort
Selection Sort
Insertion Sort
Merge Sort
Quick Sort
Big O Analysis

Common Sorting Algorithms

Bubble Sort

Description: Bubble sort is a simple sorting algorithm that repeatedly steps through the list, compares adjacent elements, and swaps them if they are in the wrong order.
Time Complexity (Worst-case): O(n^2)
Time Complexity (Average-case): O(n^2)
Time Complexity (Best-case): O(n) (when the list is already sorted)

Selection Sort

Description: Selection sort divides the input list into two parts: a sorted sublist and an unsorted sublist. It repeatedly selects the smallest (or largest) element from the unsorted sublist and moves it to the sorted sublist.
Time Complexity (Worst-case): O(n^2)
Time Complexity (Average-case): O(n^2)
Time Complexity (Best-case): O(n^2) (regardless of the input data)

Insertion Sort

Description: Insertion sort builds a sorted list by repeatedly taking elements from the unsorted part and inserting them into their correct position in the sorted part.
Time Complexity (Worst-case): O(n^2)
Time Complexity (Average-case): O(n^2)
Time Complexity (Best-case): O(n) (when the list is nearly sorted)

Merge Sort

Description: Merge sort is a divide-and-conquer algorithm that recursively divides the input list into smaller sublists, sorts those sublists, and then merges them back together to obtain the final sorted list.
Time Complexity (Worst-case): O(n log n)
Time Complexity (Average-case): O(n log n)
Time Complexity (Best-case): O(n log n)

Quick Sort

Description: Quick sort is another divide-and-conquer algorithm that selects a 'pivot' element and partitions the list into two sublists: elements less than the pivot and elements greater than the pivot. It then recursively sorts these sublists.
Time Complexity (Worst-case): O(n^2) (rare, but can occur if the pivot selection is poor)
Time Complexity (Average-case): O(n log n)
Time Complexity (Best-case): O(n log n)

Big O Analysis

Big O notation is used to describe the upper bound on the time complexity of an algorithm. It provides a way to compare and analyze the efficiency of different sorting algorithms.

O(1): Constant time - The algorithm's runtime does not depend on the size of the input data.
O(log n): Logarithmic time - The runtime grows slowly as the input size increases.
O(n): Linear time - The runtime is directly proportional to the input size.
O(n log n): Linearithmic time - The runtime grows slightly faster than linear but is still efficient.
O(n^2): Quadratic time - The runtime grows quadratically with the input size.
O(n^3): Cubic time - The runtime grows cubically with the input size.
O(2^n): Exponential time - The runtime grows exponentially with the input size.

More Info

Data Structure and Functions

For this project you are given the following print_array, and print_list functions:
#include <stdlib.h>
#include <stdio.h>

/**
 * print_array - Prints an array of integers
 *
 * @array: The array to be printed
 * @size: Number of elements in @array
 */
void print_array(const int *array, size_t size)
{
    size_t i;

    i = 0;
    while (array && i < size)
    {
        if (i > 0)
            printf(", ");
        printf("%d", array[i]);
        ++i;
    }
    printf("\n");
}
#include <stdio.h>
#include "sort.h"

/**
 * print_list - Prints a list of integers
 *
 * @list: The list to be printed
 */
void print_list(const listint_t *list)
{
    int i;

    i = 0;
    while (list)
    {
        if (i > 0)
            printf(", ");
        printf("%d", list->n);
        ++i;
        list = list->next;
    }
    printf("\n");
}
Our files print_array.c and print_list.c (containing the print_array and print_list functions) will be compiled with your functions during the correction.
Please declare the prototype of the functions print_array and print_list in your sort.h header file
Please use the following data structure for doubly linked list:
/**
 * struct listint_s - Doubly linked list node
 *
 * @n: Integer stored in the node
 * @prev: Pointer to the previous element of the list
 * @next: Pointer to the next element of the list
 */
typedef struct listint_s
{
    const int n;
    struct listint_s *prev;
    struct listint_s *next;
} listint_t;

Please, note this format is used for Quiz and Task questions.

O(1)
O(n)
O(n!)
n square -> O(n^2)
log(n) -> O(log(n))
n * log(n) -> O(nlog(n))
n + k -> O(n+k)
…

Please use the “short” notation (don’t use constants). Example: O(nk) or O(wn) should be written O(n). If an answer is required within a file, all your answers files must have a newline at the end.

Tests

Here is a quick tip to help you test your sorting algorithms with big sets of random integers: Random.org
