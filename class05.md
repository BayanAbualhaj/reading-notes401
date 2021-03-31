# ReadingNotes 

## Implementation: Linked Lists


![57](https://github.com/BayanAbualhaj/reading-notes401/blob/master/img/linked.png?raw=true)

* A Linked List is a sequence of Nodes that are connected/linked to each other.

* There are two types of Linked List 
    - Singly:Singly refers to the number of references the node has.
    - Doubly:Doubly refers to there being two (double) references within the node

* Nodes are the individual items/links that live in a linked list.Each node contains a property called Next.
    - The Head is a reference type of type Node to the first node in a linked list.
    - The Current reference is a reference type of type Node that is currently being looked at.

* **Traversal:**
    - The best way to approach a traversal is through the use of a while() loop.
    - This allows us to continually check that the Next node in the list is not null.
    - The Current will tell us where exactly in the linked list we are and will allow us to move/traverse forward until we hit the end.

* **Big O:**
    - The Big O of time for Includes would be O(n)This is because, at its worse case, the node we are looking for will be the very last node in the linked list.
    - **n** represents the number of nodes in the linked list.
    - The Big O of space for Includes would be O(1). This is because there is no additional space being used than what is already given to us with the linked list input.

    * An O(1) function takes constant time, which is to say that it doesn’t matter how many elements we have, or how huge our input is: it’ll always take the same amount of time and memory to run our algorithm.
    
    - An O(n) function is linear, which means that as our input grows , the space and time that we need to run that algorithm grows linearly.

    - O(n²) function, which clearly takes exponentially more time and memory the more elements that you have.


* Adding a Node:


![57](https://miro.medium.com/max/567/1*2xkFCMB1TWrmzs_e6rg_9g.png)

    1 - Set Current equal to Head. This will guarantee us that we are starting from the very beginning.

    2 - We can then instantiate the new node that we are adding.

    - The values passed in as arguments into the Add() method will define what the value of the Node will be.

    - newNode.Next by default is set to null. We want to set newNode.Next property to the same location that the Head node is pointing towards.

    - Because Head is just a reference type, we will be assigning it to the same allocation in memory as the node it is pointing too. In this case, it’s Node1.

    - At this point in the program we now “technically” have newNode at the beginning of the linked list, but we are not done yet.

    - We now have to re-assign where Head is pointing too. Since Node1 is no longer the first node in the list, we want to re-assign Head to point at newNode.

    - While we are at it, let’s just re-assign current as well to make sure should any further operation start at the new true start of the linked list.

_______________________________

## Linear data structures:

* linear data structures, which means that there is a sequence and an order to how they are constructed and traversed.

* non-linear data structures, items don’t have to be arranged in order, which means that we could traverse the data structure non-sequentially.

* Linked lists don’t need to take up a single block of memory; instead, the memory that they use can be scattered throughout.

____________________________________

* A static data structure needs all of its resources to be allocated when the structure is created;this means that even if the structure was to grow or shrink in size and elements were to be added or removed, it still always needs a given size and amount of memory.

* a dynamic data structure can shrink and grow in memory.It doesn’t need a set amount of memory to be allocated in order to exist, and its size and shape can change, and the amount of memory it needs can change as well.

