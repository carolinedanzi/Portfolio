Portfolio
=========
Document completion of the course's learning outcomes.

Instructions
====
The goal of this is to make it very easy for me (or an employer, or a teaching assistant) to see whether or not you have mastered the material of the class. The hope is that I would be able to grade your work without downloading and compiling your code. For labs, I can grade them by inspecting the code. For projects you must provide a video demonstrations of your programs. Some questions require essay responses.

Important
=========
If you prefer, you may turn this in to me via email, instead of hosting it on GitHub. Please talk to me about it during office hours or before or after class.

Body of portfolio
====

7 - Create an implementation of a Queue
----
I have created an impletenation of an array-based queue that uses a circular array. Here is the link to the code: https://github.com/carolinedanzi/03_Queue_Lab/blob/master/ArrayQueue.ipp

7 - Create an implementation of a List
----
I implemented the List interface using a Doubly-Linked List. Here is a link to the code: https://github.com/carolinedanzi/04_Linked_List_Lab/blob/master/LinkedList.h

7 - Create an implementation of a Binary Search Tree
----
TODO: Provide a link to your completed 06_BST_Lab OR ClosestStarbucks project (only if you used a search tree)

7 - Create an implementation of a Hash Table
----
I created a HashTable that uses open addressing and linear probing. Here is the code: https://github.com/carolinedanzi/05_Hashing_Lab/blob/master/HashTable.h

7 - Create an implementation of a Heap
----
TODO: Provide a link to your completed 07_Heap_Lab OR Vise project (only if you implemented a heap for it)

7 - Create an implementation of either Adjacency Lists or Adjacency Matrices
----
TODO: Provide a link to your completed 08_Graph_Lab OR Vise project (only if you implemented a graph for it)

7 - Implement graph algorithms
----
TODO: Provide a link to your completed Vise project (only if you used graph traversal), or add a graph traversal to 08_Graph_Lab and provide a link

21 - Determine space and time requirements of common data structure methods
-----
TODO: For each pair of data structures listed here, write a short essay comparing and contrasting them in terms of their running times for different operations. (7 points each)

* When using an array-based list as opposed to a linked list, there are different changes in runtime based on the inherent structures. An array-based list can offer easy access to any value in the array, so get(i) and set(i,x) can run in constant time. However, arrays are not very dynamic, so adding and removing from the middle of the array requires shifting the elements to fill in the gap, which takes linear time.  On the other hand, linked lists are more dynamic, so add(i,x) and remove(i) can take constant time if iterators are used.  However, accessing a specific value in the list takes linear time because you have to cycle through all of the list elements.  Therefore, get(i) and set(i,x) take linear time for linked lists. 

#####Running Times for Common Operations
|Operation | ArrayList | LinkedList|
|----------|:---------:|:---------:|
|add(i,x)  |    O(n)   |    O(1)   |
|remove(i) |    O(n)   |    O(1)   |
|get(i)    |    O(1)   |    O(n)   |
|set(i,x)  |    O(1)   |    O(n)   |

* Binary Search Tree vs. Hash Table
* Adjacency List vs. Adjacency Matrix

5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----
TODO: Define/describe each of the following terms, as they apply to memory management in C++

* The call stack (not to be confused with the stack data structure!)
* The heap (not to be confused with the heap data structure!)
* Address
* **Pointer** - A pointer stores a memory address, usually of another variable. By pointing to an address in memory, pointers can pass that variable location to a function. The function can then access and modify the data at that memory address.

TODO: Answer the following questions about memory management and dynamic variables

* **What is a memory leak, and why is it bad?**
A memory leak occurs when there is an object that is no longer in use or reachable (there is no pointer to it) but it still exists in memory.  This is bad because as the program continues to run, the amount of space in memory will decrease as more objects are created and stored, but never destroyed.  Eventually you will run out of memory.
* **What is a dangling pointer (or dangling reference), and why is it dangerous?**
A dangling pointer points to a space in memory that once contained an object useful to the program but no longer does.  This is dangerous because you do not know what the pointer is pointing to.  Also, someone else could put something bad in the spot in memory where the dangling pointer is pointing to, which could cause problems.
* **What is a destructor, and why are they necessary (in C++) to prevent memory leaks? Why *aren't* they necessary in Java?**
The destructor deallocates the memory used in the class to prevent memory leaks. It makes sure that there are no dangling pointers, which point to a space in memory that no longer holds an object, or a memory leak where the space in memory still holds an object but is no longer reachable. Java does not need the destructor because it has a "garbage collector" that looks at the heap and deletes objects that are not in use. Therefore, the deallocation of memory is automatic, so the programmer need not explicitly destruct the class. C++ does not have an automatic memory deallocator, which is why the programmer must create their own destructor to clean up after themselves.  Source used: http://www.oracle.com/webfolder/technetwork/tutorials/obe/java/gc01/index.html

5 - Create collection classes using templates in C++
----
TODO: Answer the following questions about templates in C++


20 - Using time and space analysis, justify the selection of a data structure for a given application
----
TODO: Answer the following questions about choosing data structures. (5 points each)

* If I needed a data structure to store a set of strings, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why. (Remember that a set doesn't have any order, and doesn't store duplicates. We can add items, remove items, and check to see if an item is already in the set.)
* If I needed a data structure to store a grocery list, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
* If I needed a data structure to store student records so that I could look students up by Banner number, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
* Imagine that I'm implementing a network router. It needs to keep a queue of packets waiting to be sent out over the network, but this queue need a special ability: Different companies are going to pay me different amounts of money, and the packets from the highest paying company should be sent out first. That is, if company X paid 20 and company Y paid 10, then X's packets always get sent before Y's packets. Y only gets to send packets if X doesn't have any waiting. Which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
