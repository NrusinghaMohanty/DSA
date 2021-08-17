# Data Structure

* A data structure(DS) is a way of organizing data so that it can be used effectively.
* Why DS ?
  * They are essential ingredient in creating fast and powerful algorithms.
  * They help to manage and organize data.
  * They make code cleaner and easier to understand.

# Abstract Data Type(ADT)

* An abstract datatype is an abstraction of data structure which provides only the interfac to which a data structure must adhere to
* The interface doesnot give any specific details about how something should be implemented or on what programming language.
* An ADT is composd of,
  * A collection of data.
  * A set of operation on that data.
* Specifications of an ADT indicate what the ADT opeartion do,not how to implement them.
* **Implemention** 
  * Includes choosing a particular data structure.
  * A data structure is construct that can be defined in a programming language to store a collection of data.  
* Example :-

| Abstraction(ADT) | Implementation(Ds) |
| ---------------- | ------------------ |
| List | Dynamic array,linked list |
| Queue | Linked list based queue, array based queue, stack based queue |
| Map | Tree map hash map/ hash table |
| Vechicle | Golf cart,Bicycle, Smart car |

# Time complexity & Big-O Notation

## Time complexity

* Time complexity is the study of the efficiency of alogorithm. It tells us how much time it taken by an algorithm to process a given input.
* Example :- 

| No. of element | Time taken by shubham's algo | Time taken by Rohan's algo |
| -------------- | ---------------------------- | -------------------------- | 
| 10 elements | 90ms | 122ms |
| 70 elements | 110ms| 124ms |
| 110 elements | 180ms | 131ms |
| 1000 elements | 2s | 800ms |

Here we can see that first, shubham's algo worked well with smaller input; however as we increase the number of elements, Rohan's algo perform much better.

* **Calulating order in terms of input size:-**

In order to calulate the order(time complexity), the most impactful term cotaining "n" is taken into account (Here n refers to size of input). And rest of the smaller ae ignored.

Let us assume the following formula for the algorithm in terms input ize "n",

Algo 1 : k<sub>1</sub>n<sup>2</sup> + k<sub>2</sub>n + 36 = O(n<sup>2</sup>)
   
Algo 2 : k<sub>1</sub>n<sub>2</sub><sup>2</sup> + k<sub>3</sub>k<sub>2</sub> + 8 = O(n<sup>0</sup>) = O(1)

Here, we ignored other lower order terms(k<sub>2</sub>n ) in algo1 and carried the higer order term (k<sub>1</sub>n<sup>2</sup>) ,which was the square of the input ize. Hence the time complexity bcome n<sup>2</sup> . The second algo followed a constant time complexity

## Big - O 

Big – O notation is used to study the performance / complexity of an algorithm in theoretical terms. Big – O notation looks at the upper bound of an algorithms performance.

![](https://res.cloudinary.com/djc1o48j7/image/upload/v1629216120/DSA/img_scr/IMG_20210817_184124_g0m08v.jpg)

| | |
| - | - |
| Constant time | O(1) | 
| Logarithmic time | O(log(n)) |
| Linear time | 0 (n)|
| linearthimtic time | O(n log(n)) |
| Quadric time | O(n<sup>2</sup>)
| Cubic time | O(n<sup>3</sup>) |
| Exponential time | O(b<sup>n</sup>) |
| Factorial time | O(n!)

# Static and Dynamic arrays

## Static array 

* A static array is a fixed length container containing "n" elements index from rang [0,n-1] .
* When and where to used :-
  * storing and accessing sequential data.
  * Temporarily storing objects.
  * Lookup tables and inverse lookup tables.
  * Can be used to rrun multiple values from a function.
  * Used in dynamic programming to cache answer to subproblems.

* **Complexity**

| | Static Array | Dynamic Array |
| - | ----------- | ------------- |
| Access | O(1) | O(1) |
| Search | O(n) | O(n) |
| Insertion | N/A | O(n) |
| Appending | N/A | O(1) |
| Deletion | N/A | O(n) |

## Dynamic array

* The dynamic array can grow and shrink in size.

```A = | 34 | 4 |

A.add(7) = | 34 | 4 | 7 |

A.add(28) = | 34 | 4 | 7 | 28 |

A.remove(4) = | 34 | 7 | 28 |
```
**How can we implement a dynamic array**

* one way to use a static array
  * Create  static array with an initial capacity.
  * Add elements to the underlying static array,keeping track of number of elements.
  * If adding another element will exceed the capacity, then create a new static array with twice the capacity and copy original elements into it.

# Singly and Doubly linked lists

* A linked list is a sequential list of nodes that hold data which point to other nodes also containing data.

![](https://res.cloudinary.com/djc1o48j7/image/upload/v1629213576/DSA/img_scr/IMG_20210817_184222_bqscfu.jpg)

* Used :-
  * Used in amny list, queue and stack impplemenatations.
  * Great for creating circular list.
  * Can easily model real world objects such a trains.

![](https://res.cloudinary.com/djc1o48j7/image/upload/v1629213531/DSA/img_scr/IMG_20210817_184317_iozx59.jpg)

## Singly linked list

Singly linked list only holds a reference to the next node. In the implementation you alays maintain a reference to the hear to the linked list and a reference to the tail node for quick additions/removals.

![](https://res.cloudinary.com/djc1o48j7/image/upload/v1629213515/DSA/img_scr/IMG_20210817_184629_qlisxz.jpg)

## Doubly linkd list

With a doubly linked list each nod holds a reference to the next and previous node. In the implementationyou always maintain a refernce to the head and tail of the doubly linked list to do quick additions/removals from the both ends of your list.

![](https://res.cloudinary.com/djc1o48j7/image/upload/v1629213531/DSA/img_scr/IMG_20210817_184618_jmhe2v.jpg)

| | Advantages | Disadvantages |
| - | --------- | ------------- |
| Singly linked list | Used less memory, simple implementation | Cannot easily access previous elements |
| Doubly linked list | Can be traversed backward | Takes 2x memory |

**Complexity**

| | Singly linked list | Doubly linked list |
| - | ----------------- | ------------------ |
| Search | O(n) | O(n) |
| Insert at head | O(1) | O(1) |
| Insert at tail | O(1) | O(1) |
| Remove at head | O(1) | O(1) |
| Remove at tail | O(n) | O(1) |
| Remove in middle | O(n) | O(n) |

# Union find

* Union find is a data structure that keeps track of elemnt which are split into one or more disjoint sets. It has two primary function, find(it find the group from where element belongs) and union(it merges two group together).

![](https://res.cloudinary.com/djc1o48j7/image/upload/v1629223162/DSA/img_scr/IMG_20210817_232155_egmwym.jpg)


* Uses:-
  * Kruskal's minimum spanning tree algorithm
  * Grid percolation
  * Network connectivity
  * Least common ancestor in trees
  * Image processing

**Complexity**

| | |
| - | - |
| contruction | O(n) | 
| Count components | O(1) | 

## Krushkal's Algorithm :

It helps to find out the minimal subset of edges using which we can traverse every vertex of a graph without forming a cycle. 

![](https://res.cloudinary.com/djc1o48j7/image/upload/v1629223164/DSA/img_scr/IMG_20210817_232229_irjemo.jpg)

# Fenwick Tree / Binary index tree

Fenwick tree is a data structure which is used for calculating the prefix sums and updating the elements in an array of numbers. It is also called binary indexed tree.

### Prefix sum calculation :
|Array     |2 |4 |5 |11 |
|:--------:|--|--|--|---|
|Prefix sum| 0| 6|11|22 |

Here the disadvantage is that if any one element of the array updates then we will have to recompute the sum again.

### Fenwick Tree range queries,point update and linear contruction :

![](https://res.cloudinary.com/djc1o48j7/image/upload/v1629220759/DSA/img_scr/IMG_20210817_224402_tnonci.jpg)

![](https://res.cloudinary.com/djc1o48j7/image/upload/v1629220763/DSA/img_scr/IMG_20210817_224433_kpikl5.jpg)