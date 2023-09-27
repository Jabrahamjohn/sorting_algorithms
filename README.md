<h1 class="gap">0x1B. C - Sorting algorithms &amp; Big O</h1>

<p><img src="https://s3.amazonaws.com/intranet-projects-files/holbertonschool-low_level_programming/248/willy-wonka.png"><br>
<br></p>

## Learning Objectives:bulb:
What you should learn from this project:

* At least four different sorting algorithms
* What is the Big O notation, and how to evaluate the time complexity of an algorithm
* How to select the best sorting algorithm for a given input
* What is a stable sorting algorithm

# RESOURCES
### Read or Watch
<ul>
<li><a href="/rltoken/-j5MKLBlzZAC2RfJ5DTBIg" title="Sorting algorithm" target="_blank">Sorting algorithm</a> </li>
<li><a href="/rltoken/WRvrE2BaNVQFssHiUATTrw" title="Big O notation" target="_blank">Big O notation</a> </li>
<li><a href="/rltoken/ol0P7NbYVb5R31iOv4Q40A" title="Sorting algorithms animations" target="_blank">Sorting algorithms animations</a> </li>
<li><a href="/rltoken/_I0aEvhfJ66Xyob6dd9Utw" title="15 sorting algorithms in 6 minutes" target="_blank">15 sorting algorithms in 6 minutes</a> (<em><b>WARNING</b>: The following video can trigger seizure/epilepsy. It is not required for the project, as it is only a funny visualization of different sorting algorithms</em>)</li>
<li><a href="/rltoken/Ea93HeEYuNkOL7sGb6zzGg" title="CS50 Algorithms explanation in detail by David Malan" target="_blank">CS50 Algorithms explanation in detail by David Malan</a></li>
<li><a href="/rltoken/21X_eaj5RGcLIL9mZv2sqw" title="All about sorting algorithms" target="_blank">All about sorting algorithms</a></li>
</ul>

### [0. Bubble sort](./0-bubble_sort.c)
* Write a function that sorts an array of integers in ascending order using the Bubble sort algorithm


### [1. Insertion sort](./1-insertion_sort_list.c)
* Write a function that sorts a doubly linked list of integers in ascending order using the Insertion sort algorithm


### [2. Selection sort](./2-selection_sort.c)
* Write a function that sorts an array of integers in ascending order using the Selection sort algorithm


### [3. Quick sort](./3-quick_sort.c)
* Write a function that sorts an array of integers in ascending order using the Quick sort algorithm


### [4. Shell sort - Knuth Sequence](./100-shell_sort.c)
* Write a function that sorts an array of integers in ascending order using the Shell sort algorithm, using the Knuth sequence


### [5. Cocktail shaker sort](./101-cocktail_sort_list.c)
* Write a function that sorts a doubly linked list of integers in ascending order using the Cocktail shaker sort algorithm


### [6. Counting sort](./102-counting_sort.c)
* Write a function that sorts an array of integers in ascending order using the Counting sort algorithm


### [7. Merge sort](./103-merge_sort.c)
* Write a function that sorts an array of integers in ascending order using the Merge sort algorithm


### [8. Heap sort ](./104-heap_sort.c)
* Write a function that sorts an array of integers in ascending order using the Heap sort algorithm


### [9. Radix sort](./105-radix_sort.c)
* Write a function that sorts an array of integers in ascending order using the Radix sort algorithm


### [10. Bitonic sort](./106-bitonic_sort.c)
* Write a function that sorts an array of integers in ascending order using the Bitonic sort algorithm


### [11. Quick Sort - Hoare Partition scheme](./107-quick_sort_hoare.c)
* Write a function that sorts an array of integers in ascending order using the Quick sort algorithm


### [12. Dealer](./1000-sort_deck.c)
* Write a function that sorts a deck of cards.

---

## MORE INFO
### Data structures and functions
<ul>
<li>For this project you are given the following <code>print_array</code>, and <code>print_list</code> functions:</li>
</ul>
<pre><code>#include &lt;stdlib.h&gt;
#include &lt;stdio.h&gt;

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
    while (array &amp;&amp; i &lt; size)
    {
        if (i &gt; 0)
            printf(", ");
        printf("%d", array[i]);
        ++i;
    }
    printf("\n");
}
</code></pre>
<pre><code>#include &lt;stdio.h&gt;
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
        if (i &gt; 0)
            printf(", ");
        printf("%d", list-&gt;n);
        ++i;
        list = list-&gt;next;
    }
    printf("\n");
}
</code></pre>
<ul>
<li>Our files <code>print_array.c</code> and <code>print_list.c</code> (containing the <code>print_array</code> and <code>print_list</code> functions) will be compiled with your functions during the correction.</li>
<li>Please declare the prototype of the functions <code>print_array</code> and <code>print_list</code> in your <code>sort.h</code> header file</li>
<li>Please use the following data structure for doubly linked list:</li>
</ul>
<pre><code>/**
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
</code></pre>
<p>Please, note this format is used for Quiz and Task questions.</p>
<ul>
<li><code>O(1)</code></li>
<li><code>O(n)</code></li>
<li><code>O(n!)</code></li>
<li>n square -&gt; <code>O(n^2)</code></li>
<li>log(n) -&gt; <code>O(log(n))</code></li>
<li>n * log(n) -&gt; <code>O(nlog(n))</code></li>
<li>n + k -&gt; <code>O(n+k)</code></li>
<li>…</li>
</ul>
<p>Please use the “short” notation (don’t use constants). Example: <code>O(nk)</code> or <code>O(wn)</code> should be written <code>O(n)</code>.
If an answer is required within a file, all your answers files must have a newline at the end.</p>
<h3>Tests</h3>
<p>Here is a quick tip to help you test your sorting algorithms with big sets of random integers: <a href="/rltoken/YR-VWQbICB59wZs1eAaI3w" title="Random.org" target="_blank">Random.org</a></p>

## Author:
**Abraham john**
 - [GitHub](https://github.com/Jabrahamjohn)
 - [Twitter](https://twitter.com/Jabrahamjohns)


   COLLABORATION:
   [Cellphone](+254758238617)
