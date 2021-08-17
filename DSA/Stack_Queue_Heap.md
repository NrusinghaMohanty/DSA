# Stack

* A stack is a one-ended linear data structure which models a real world by having two primary operaions, namely push and pop.

![](https://res.cloudinary.com/djc1o48j7/image/upload/v1629213561/DSA/img_scr/IMG_20210817_184715_vcgdez.jpg)

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

![](https://res.cloudinary.com/djc1o48j7/image/upload/v1629213557/DSA/img_scr/IMG_20210817_184842_twcari.jpg)

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

* Queue basically of 3 type,
  1. Circular Queue
  2. Priority Queue
  3. Dequeue (Double Ended Queue)

## Heap

* **Complete binary tree** - A complete binary tree is a binary tree in which,
  * All the nodes have two children except leaft nodes
  * Last level is filled from the left i.e, the nodes are added from left side at the last level

![](https://res.cloudinary.com/djc1o48j7/image/upload/v1629220761/DSA/img_scr/IMG_20210817_224508_ozn6ep.jpg)  

* **Leaf node** - Node that is present at the last level of an binary tree

![](https://res.cloudinary.com/djc1o48j7/image/upload/v1629220757/DSA/img_scr/IMG_20210817_224532_cefitr.jpg)

* **Heap** - Heap is a tree based data structure in which all the nodes are in a specific order/sequence.
* Uses,
  * It is used to implement priority queue
  * It is used for accessing largest element or smallest element quickly.

* Type of heap,
  1. Max heap
  2. Min heap

* **Max heap** - In max heap,the child nodes are alway smaller than the parent node. The largest among all node is the root node.

* **Min heap** - In min heap, the parent node is smaller than its children. The root node is smallest of all node.

* **Adding a element to a heap** :-

![](https://res.cloudinary.com/djc1o48j7/image/upload/v1629213677/DSA/img_scr/IMG_20210817_201040_uyaloj.jpg)

* **Removing a element from a heap** :-

![](https://res.cloudinary.com/djc1o48j7/image/upload/v1629213724/DSA/img_scr/IMG_20210817_201821_ovceaw.jpg)

* **Process for removing** - when you want to emove a node
  1. Replace the node to be deleted with the last element
  2. Delete the node
  3. Arrange the heap in correct order