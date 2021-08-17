# Binary Search Tree

* Binary tree :- A tree whose element have at most two children is called a binary tree. Since each elemnt in a binary tree can have only two children, we typically name them them left and right child.

![](https://res.cloudinary.com/djc1o48j7/image/upload/v1629213591/DSA/img_scr/IMG_20210817_184933_yfnrfm.jpg)

## Binary Search tree(BST)

* It is a type of binary tree
* Properties :-
  * All nodes/elements of the left subtree are lesser.
  * All nodes/elements of the right subtree are greter.
  * left and right subtree ae also BST.
  * There are no duplicate nodes

![](https://res.cloudinary.com/djc1o48j7/image/upload/v1629213584/DSA/img_scr/IMG_20210817_185041_hhkgmn.jpg)  

### Deletion

  * 0 children
  * 1 children
  * 2 children
    * In order predecessor
    * In order successor

* **0 children**

![](https://res.cloudinary.com/djc1o48j7/image/upload/v1629213577/DSA/img_scr/IMG_20210817_185130_fjumoa.jpg)

* **1 children**

![](https://res.cloudinary.com/djc1o48j7/image/upload/v1629213614/DSA/img_scr/IMG_20210817_185159_gz7x9v.jpg)

* **2 children**

1. In order predecessor means the nodes replace with the largest element/node its left sub-tree.

![](https://res.cloudinary.com/djc1o48j7/image/upload/v1629213673/DSA/img_scr/IMG_20210817_185458_vyradv.jpg)

2. In order successor means the nodes replace with the smallest element/node its lright sub-tree.

![](https://res.cloudinary.com/djc1o48j7/image/upload/v1629213607/DSA/img_scr/IMG_20210817_185528_fxjbin.jpg)

## Binary tree traversals

1. Inorder :- The flow will be Left-root-right
2. Preorder :- The flow will be root-Left-right
3. Postorder :- The flow will be Left-right-root

![](https://res.cloudinary.com/djc1o48j7/image/upload/v1629213665/DSA/img_scr/IMG_20210817_185600_dhsrax.jpg)

In upper tree ,

1. Inorder :- BDAGECHFII
2. Preorder :- ABDCEGFHI
3. Postorder :- DBGEHIFCA

# Hashing 

* Hashing is technique to place/map a large domain of key values into a specified location in the hash table, and the location is calulated from the key value itself using the hash table.

* **Hash table** :- This is an array of some constant size in which a key value will be placed in specified location.

* **Hash function** :- The function used to transform the keys of a record into its physical address is known as hash function.

![](https://res.cloudinary.com/djc1o48j7/image/upload/v1629213677/DSA/img_scr/IMG_20210817_185716_v0pnof.jpg)

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

![](https://res.cloudinary.com/djc1o48j7/image/upload/v1629213645/DSA/img_scr/IMG_20210817_191030_zozx8e.jpg)

### Closed hashing(open addressing)

The differenet techniques to find the free slot/address of the colliding key of record is called probing/open addressing.

**1. Linear probing**

Here, if a record with key "k" is mapped to an address preoccupied by some other record, then linear search starting from the address generated by hash function is done until a free location is found for storage.

Q. Use division method and linear probing to store these values where h(k) = 2k+3 , n=10 and A = 3,2,9,6,11,13,7,12

![](https://res.cloudinary.com/djc1o48j7/image/upload/v1629213619/DSA/img_scr/IMG_20210817_191805_vdy8lv.jpg)

**2. Quadratic probing**

Here, the address increment of colliding records is squared value of collision probs number(1<sup>2</sup>,2<sup>2</sup>,3<sup>2</sup>)

Formula :-

`Hash(k,p) = [h(k)+p<sup>2</sup>] mod n`

Here, H(k) = hash function used to find the relative address. 

p = probe number(0,1,2,3,.....,n-1)

Q. Use division method and quadratic probing to store these values where h(k) = 2k+3 , n=10 and A = 3,2,9,6,11,13,7,12

![](https://res.cloudinary.com/djc1o48j7/image/upload/v1629213677/DSA/img_scr/IMG_20210817_192239_y7skna.jpg)

**3. Double hashing**

Double hashing is the efficient method of collision resolution technique because it uses double hash function to calculate the address of any key.

Hash function should be such that the hash address generatd by two hash function

Formula :-

`Hash(k,p) = [h<sub>1</sub>(k)+v*p] % n`

Here, v = h<sub>2</sub>(k) % n

Q. Use division method and double hashing to store these values A = 3,2,9,6,11,12

![](https://res.cloudinary.com/djc1o48j7/image/upload/v1629213708/DSA/img_scr/IMG_20210817_202616_ea5dl8.jpg)