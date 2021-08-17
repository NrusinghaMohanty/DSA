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

* Used :-
  * Used in amny list, queue and stack impplemenatations.
  * Great for creating circular list.
  * Can easily model real world objects such a trains.


## Singly linked list

Singly linked list only holds a reference to the next node. In the implementation you alays maintain a reference to the hear to the linked list and a reference to the tail node for quick additions/removals.

## Doubly linkd list

With a doubly linked list each nod holds a reference to the next and previous node. In the implementationyou always maintain a refernce to the head and tail of the doubly linked list to do quick additions/removals from the both ends of your list.


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

# Stack

* A stack is a one-ended linear data structure which models a real world by having two primary operaions, namely push and pop.

* Uses :-
  * Used by undo mechanisms in text editor.
  * Used in compiler syntax checking for matching brackets and braces.
  * Used behind the scenes to support recursion by keeping track of previous function calls.

**Complexity**

| | |
| - | - |
| Pushing | O(1) |
| Poping | O(1) |
| Peeking | O(1) |
| Size | O(1) |
| Searching | O(n) |

# Queues

* A queue is a linear data structure which models real world queues by having two primary operation namely enqueue and dequeue.

* There doesnot seem to be consistent terminology for inserting and removing elements from queues
  * Enqueue = Adding = Offering
  * Dequeue = Removing = Polling
* Used :- 
  * Any waiting line models is a queue. For a example a linup at a movie theatre.
  * Can be used to efficiently keep track of the X most recently added element.
  * Web server request management where you want first come firt serve 

**Complexity**

| | |
| - | - |
| Enqueue | O(1) |
| Dequeue | O(1) |
| Peeking | O(1) |
| Conatins | O(n) |
| Removal | O(n) |
| Is empty| O(1) |     

![](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png)

# Binary Search Tree

* Binary tree :- A tree whose element have at most two children is called a binary tree. Since each elemnt in a binary tree can have only two children, we typically name them them left and right child.


## Binary Search tree(BST)

* It is a type of binary tree
* Properties :-
  * All nodes/elements of the left subtree are lesser.
  * All nodes/elements of the right subtree are greter.
  * left and right subtree ae also BST.
  * There are no duplicate nodes

### Deletion

  * 0 children
  * 1 children
  * 2 children
    * In order predecessor
    * In order successor

* **0 children**

![](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png)

* **1 children**

![](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png)

* **2 children**

1. In order predecessor means the nodes replace with the largest element/node its left sub-tree.

![](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png)

2. In order successor means the nodes replace with the smallest element/node its lright sub-tree.

![](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png)

## Binary tree traversals

1. Inorder :- The flow will be Left-root-right
2. Preorder :- The flow will be root-Left-right
3. Postorder :- The flow will be Left-right-root


1. Inorder :- BDAGECHFII
2. Preorder :- ABDCEGFHI
3. Postorder :- DBGEHIFCA

# Hashing 

* Hashing is technique to place/map a large domain of key values into a specified location in the hash table, and the location is calulated from the key value itself using the hash table.

* **Hash table** :- This is an array of some constant size in which a key value will be placed in specified location.

* **Hash function** :- The function used to transform the keys of a record into its physical address is known as hash function.

* Need of hashing :-
  * To facilitate direct access of records infiles.
  * Involves less key comparison and searching can be performed in constant time/linear time complexity O(1).

* **Collision** :- It is defined as the situation. When two or more distinct records are mapped to the same physical address. This is the main problem of hashing technique when address generated by the mapping function maynot be unique.

* Principle criteria in deciding a hash function
  * The function "H" should be very easy and quick to compute.
  * The function "H" should uniformly distribute the keys i.e it should give two different indices for two different key values

* Hashing Techniques :-
  1. Direct hashing
  2. Subtraction hashing
  3. Mid-square method
  4. Modulo-division method (mostly used)
  5. Digit extraction method
  6. Folding
  7. Shifting
  8. Rotating
  9. Pseudo-random method   

### Modulo-division method

for the mapping key to address, the key is divided by a number(prime number which is closed to the available address) and the eminder generated is taken as relative address for record.

Formula :-

`H(k) = k mod(%) n`

Here , H(k) = Address,
       k = key,
       n = prime number

Example :-

Q. Suppose we have keys of 1098,1120 and 1230 and available address is 1000,  

| key(k) | Address H(k) |
| ---- | -------- |
| 1098 | 101 | 
| 1120 | 123 |
| 1230 | 233 |

Here n = 997 (because it is closest prime number to 1000) 

## Collision Resolution techniques

* Collision Resolution techniques is of two type,
  * Open hashing(closed addressing)
    * Chaining
  * Closed hashing(open addressing)
    * Linear probing
    * Quadratic probing
    * Double hashing

### Open hashing(closed addressing)

* chaining :-
  * This method used a hash table as an array of pointers, each points a linked list.
  * In this approach the colliding records are chained together by maninting a linked list of uch coliding records.

Example:-

Q. Use division method and closed addressing to store these values where h(k) = 2k+3 , n=10 and A = 3,2,9,6,11,13,7,12


### Closed hashing(open addressing)

The differenet techniques to find the free slot/address of the colliding key of record is called probing/open addressing.

**1. Linear probing**

Here, if a record with key "k" is mapped to an address preoccupied by some other record, then linear search starting from the address generated by hash function is done until a free location is found for storage.

**2. Quadratic probing**

Here, the address increment of colliding records is squared value of collision probs number(1<sup>2</sup>,2<sup>2</sup>,3<sup>2</sup>)

Formula :-

`Hash(k,p) = [h(k)+p<sup>2</sup>] mod n`

Here, H(k) = hash function used to find the relative address. 

p = probe number(0,1,2,3,.....,n-1)

**3. Double hashing**

Double hashing is the efficient method of collision resolution technique because it uses double hash function to calculate the address of any key.

Hash function should be such that the hash address generatd by two hash function

Formula :-

`Hash(k,p) = [h<sub>1</sub>(k)+v*p] % n`

Here, v = h<sub>2</sub>(k) % n

# AVL

* Height balanced binary tree
* Height difference between heights of left and right subtrees for every node is less than or equal to 1.
* Balanced factor = height of right subtree - height of left subtree
* Balanced factor can be -1,0 or 1 for a node to be balanced in a AVL tree.


