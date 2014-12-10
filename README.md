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

7 - Create an implementation of a Queue using a circular array-based list
----
I have created an implementation of an array-based queue that uses a circular array. Here is the link to the code: https://github.com/carolinedanzi/03_Queue_Lab/blob/master/ArrayQueue.ipp

7 - Create an implementation of a List
----
I implemented the List interface using a Doubly-Linked List. Here is a link to the code: https://github.com/carolinedanzi/04_Linked_List_Lab/blob/master/LinkedList.h

7 - Create an implementation of a Binary Search Tree
----
I implemented a Binary Search Tree with recursive methods. Here is a link to the code: https://github.com/carolinedanzi/06_BST_Lab/blob/master/BST.h

7 - Create an implementation of a Hash Table
----
I implemented a Hash Table that uses open addressing with linear probling. Here is a link to the code: https://github.com/carolinedanzi/05_Hashing_Lab/blob/master/HashTable.h

7 - Create an implementation of a Heap
----
TODO: Provide a link to your completed 07_Heap_Lab

7 - Create an implementation of either Adjacency Lists or Adjacency Matrices
----
I have created an implementation of a graph using adjacency lists. Here is a link to the code: https://github.com/carolinedanzi/08_Graph_Lab/blob/master/Graph.cpp

7 - Implement graph algorithms
----
I have implemented a depth-first search graph traversal that prints out the nodes in the order they are looked at. The code is in the method "DFS": https://github.com/carolinedanzi/08_Graph_Lab/blob/master/Graph.cpp

21 - Determine space and time requirements of common data structure methods
-----
For each pair of data structures listed here, write a short essay comparing and contrasting them in terms of their running times for different operations. (7 points each)

* **Array-Based List vs. Linked List:** When using an array-based list as opposed to a linked list, there are different changes in runtime based on the inherent structures. An array-based list offers random access to any value in the array, so get(i) and set(i,x) at indices will run in constant time. However, arrays are not very dynamic, so adding and removing from the middle of the array requires shifting the elements to fill in the gap, which takes linear time.  On the other hand, linked lists can only offer sequential access, where you have to search through all the elements in order to find the one you are looking for.  Therefore, both get(i) and set(i, x) at indices take linear time.  Additionally, adding and removing when given an index will take linear time since we have to search through all the elements to get to the index where we wish to add or remove.  However, these running times change when using iterators, which act like bookmarks that point to where you are in the data structure.  To get an iterator for an index in an array list just takes constant time since it offers random access of elements, wherease getting an iterator for an index in a linked list takes linear time since we have to cycle through all the elements.  Adding and removing at an iterator in an array list still takes linear time because the elements will still need to be shifted.  In contrast, adding and removing at an iterator for linked lists will improve the running time to constant time.  Since the iterator is already pointing to where we want to add or remove, all that needs to be done is rearrange pointers, which takes constant time.  Get and set at an iterator will take constant time for both data structures, since the iterator will be pointing to the element we wish to get or change.  Lastly, adding and removing at the front of back of both data structures will take constant time.  For a circular array list, adding or removing the first or last element does not require shifting all the other elements.  For a doubly-linked list, adding or removing the first or last element does not require cycling through a lot of elements, since we can follow the pointers from the dummy node.  The same goes for getting an iterator for the first or last element - it will take constant time for both data structures.     

#####Running Times for Common Operations
|Operation                   | ArrayList | LinkedList|
|----------------------------|:---------:|:---------:|
|get an iterator for an index|    O(1)   |    O(n)   |
|add at index                |    O(n)   |    O(1)   |
|remove at index             |    O(n)   |    O(1)   |
|add at iterator             |    O(n)   |    O(1)   |
|remove at iterator          |    O(n)   |    O(1)   |
|get at index                |    O(1)   |    O(n)   |
|set at index                |    O(1)   |    O(n)   |
|get at iterator             |    O(1)   |    O(1)   |
|set at iterator             |    O(1)   |    O(1)   |
|get iterator at front/back  |    O(1)   |    O(1)   |
|add/remove at front/back    |    O(1)   |    O(1)   |

* **Binary Search Tree vs. Hash Table:**

#####Running Times for Common Operations
|Operation 		| Hash Table | Balanced BST |Unbalanced BST|
|-----------------------|:----------:|:------------:|:------------:|
|add(key, value)	|    O(1)    |    O(lg n)   |	  O(h)     |
|remove(key)		|    O(1)    |	  O(lg n)   |     O(h)     |
|get/set when given key |    O(1)    |    O(lg n)   |     O(h)     |
|find min/max		|    O(n)    |    O(lg n)   |     O(h)     |
|next/prev(key)		|    O(n)    |    O(lg n)   |     O(h)	   |

* **Adjacency List vs. Adjacency Matrix:**

#####Running Times for Common Operations
|Operation	 |Adjacency Matrix|Adjacency Lists|
|----------------|:--------------:|:-------------:|
|add an edge	 | 	O(1)	  |	O(d)	  |
|remove edge	 |	O(1)	  |  O(n) or O(d) |
|get cost of edge|	O(1)	  |	O(d)	  |
|get neighbors   |	O(n)	  |	O(1)	  |
|space used	 | 	O(n<sup>2</sup>)|O(n+m)	  |

5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----
Define/describe each of the following terms, as they apply to memory management in C++

* **The call stack** - The call stack keeps track of function calls and local variables while a program is running.  The elements are pushed and popped off the back of the Stack in the order they were added, so the stack is a LIFO (last-in-first-out) queue.  Variables stored here are statically allocated, meaning they are allocated at compile time.  The call stack also keeps track of which function called which function, which can be helpful for debugging.  
* **The heap** - The heap is the part of RAM (random access memory) where dynamically allocated variables are stored.  This is an important part of memory management – pointers often point here, and a programmer can run into trouble if they have a memory leak and the heap fills up.  
* **Address** - An address is the exact location in memory where an object is stored.  It is an integer represented in hexadecimal.  In C++, programmers have direct access to memory addresses, and can store them in variables called pointers, or access them using &, the address-of operator.  Direct access to memory is one of the reasons why C++ is such a fast language.  
* **Pointer** - A pointer stores a memory address, usually of another variable. By pointing to an address in memory, pointers can pass that variable location to a function. The function can then access and modify the data at that memory address.

Answer the following questions about memory management and dynamic variables

* **What is a memory leak, and why is it bad?**
A memory leak occurs when there is an object that is no longer in use or reachable (there is no pointer to it) but it still exists in memory.  This is bad because as the program continues to run, the amount of space in memory will decrease as more objects are created and stored, but never destroyed.  Eventually you will run out of memory.
* **What is a dangling pointer (or dangling reference), and why is it dangerous?**
A dangling pointer points to a space in memory that once contained an object useful to the program but no longer does.  This is dangerous because you do not know what the pointer is pointing to.  This can cause problems in a program that can be very difficult to debug.  With a dangling pointer it is possible to overwrite another variable because the pointer is not pointing to where you think it should. Letting a pointer point to a spot in memory that is not in use is dangerous. Also, someone else could put something bad in the spot in memory where the dangling pointer is pointing to, which could cause problems.
* **What is a destructor, and why are they necessary (in C++) to prevent memory leaks? Why *aren't* they necessary in Java?**
The destructor deallocates the memory used in the class to prevent memory leaks. It makes sure that there are no dangling pointers, which point to a space in memory that no longer holds an object, or a memory leak where the space in memory still holds an object but is no longer reachable. Java does not need the destructor because it has a "garbage collector" that looks at the heap and deletes objects that are not in use. Therefore, the deallocation of memory is automatic, so the programmer need not explicitly destruct the class. C++ does not have an automatic memory deallocator, which is why the programmer must create their own destructor to clean up after themselves.  Source used: http://www.oracle.com/webfolder/technetwork/tutorials/obe/java/gc01/index.html

5 - Create collection classes using templates in C++
----
TODO: Answer the following questions about templates in C++

* What is the main benefit of using templates when creating collection classes?
* In normal C++ code the .h file contains the declarations, and the .cpp file contains implementations. Explain why this isn't the case with template-based collection classes.

20 - Using time and space analysis, justify the selection of a data structure for a given application
----
TODO: Answer the following questions about choosing data structures. (5 points each)

* If I needed a data structure to store a set of strings, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why. (Remember that a set doesn't have any order, and doesn't store duplicates. We can add items, remove items, and check to see if an item is already in the set.)
* **If I needed a data structure to store a grocery list, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.**
If you were to use a Queue with FIFO (first-in-first-out) queueing discipline, this would be best if you wrote the items in the order you wanted to locate them in the store.  Then you could go down the list, crossing out (removing) the items at the top (front) of the list, and adding to the back as needed.  However, I doubt many people can write their grocery lists in the correct order the first time without needing to add items in the middle.  To me, a List data structure would be best for a grocery list.  You can add and remove from the middle, which would be helpful when putting items in an order, such as by location within the grocery store.  If you forgot to add an item in the “cold” section of the list, for example, you would just need to use the add(i,x) operation.  Then when you are in the grocery store, you can just use get(i) to look at the next item on the list.  Furthermore, I think a LinkedList would be best, as opposed to an ArrayList.  ArrayLists add and remove in linear time but get and set in constant time.  However, add and remove would be heavily used for making a grocery list, so it would be better if these methods were faster.  Therefore, a LinkedList would be more helpful since its add and remove functions can run in constant time.  Also, although get and set run in linear time, get(0) would run in constant time since it is just looking at the first element – it would not need to cycle through all the list entries.  This would be sufficient for an organized grocery list; checking the next item on the list would be fast and easy.  
* If I needed a data structure to store student records so that I could look students up by Banner number, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
* Imagine that I'm implementing a network router. It needs to keep a queue of packets waiting to be sent out over the network, but this queue need a special ability: Different companies are going to pay me different amounts of money, and the packets from the highest paying company should be sent out first. That is, if company X paid 20 and company Y paid 10, then X's packets always get sent before Y's packets. Y only gets to send packets if X doesn't have any waiting. Which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
