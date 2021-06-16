 
 WHAT IS A LINKED LIST?
 =====================
 A **linked list** is a linear collection of data elements whose order is not given by their physical placement in memory. Instead, each element points to the next. It is a data structure consisting of a collection of nodes which together represent a sequence.

 -Each element(node) holds two pieces of information or properties.  The data value iteself and a pointer that references the next element in the list.  This is considered a *"Singly linked list"*. <br> 
 A *"Doubly linked list"* contains an additional pointer referencing the previous element.

A singly linked list whose nodes contain two fields: an integer value and a link to the next node

A doubly linked list whose nodes contain three fields: an integer value, the link forward to the next node, and the link backward to the previous node

![Image of Singly/Doubly Linked List](https://miro.medium.com/max/615/1*iMYmkYDCSrXXdwpbqm-ekA.jpeg)
<br><br><br>

<h2>Linked List:</h2>
 -Can be any element, can be unique elements OR duplicate elements.

-Can be distinguished from an array because elements in an array can be accessed at any time.  A link list must start at the "head" or first element, and work its way through addional elements to access the requested element.  (Slower)

-A drawback of linked lists is that search operations are slow in linked lists. Unlike arrays, random access of data elements is not allowed. Nodes are accessed sequentially starting from the first node.
It uses more memory than arrays because of the storage of the pointers.

-Advantage is.. because elements can be stored anywhere in memory and dont require being stored in a contiguous block of memory(array).  Elements can be added and removed much faster and easier.  Always takes the same amount of time no matter the size of the list.

![Image of Array vs Linked List](https://i1.faceprep.in/Companies-1/difference-between-arrays-and-linked-list.png)
<br><br>
**<h2>A great example of a linked list, is a music player where a user is able to jump to a "next" or "previous" track on a particular playlist or list of songs.</h2>**
<br><br><br>

HOW DOES A NODE STORE DATA?
==========================
What is a node?
-In computer science a node is a basic unit of a data structure, such as a a tree data structure. Nodes contain data and also may link to other nodes usually by a pointer. Another example of this is a binary tree data structure or a linked list.


![Image of Node Tree](https://i.stack.imgur.com/5kJXf.gif)

---------------------------------------------------------------
#####################################################
#####################################################
<br><br>
In JavaScript, a linked list looks like this:

```
const list = {
    head: {
        value: 6
        next: {
            value: 10                                             
            next: {
                value: 12
                next: {
                    value: 3
                    next: null	
                    }
                }
            }
        }
    }
};
```



<h2>Implementing a List Node in JavaScript:</h2>
As stated earlier, a list node contains two items: the data and the pointer to the next node. We can implement a list node in JavaScript as follows:

```
class ListNode {
    constructor(data) {
        this.data = data
        this.next = null                
    }
}
```

<br><br>
<h2>Implementing a Linked List in JavaScript:</h2>
The code below shows the implementation of a linked list class with a constructor. Notice that if the head node is not passed, the head is initialised to null.

```
class LinkedList {
    constructor(head = null) {
        this.head = head
    }
}
```
<br>
<br>

<h2>Putting it all together:</h2>
Let's create a linked list with the class we just created. First, we create two list nodes, node1 and node2 and a pointer from node 1 to node 2.

```
let node1 = new ListNode(2)
let node2 = new ListNode(5)
node1.next = node2
```
Next, we'll create a Linked list with the node1:

```
let list = new LinkedList(node1)
```

Let's try to access the nodes in the list we just created:

```
console.log(list.head.next.data) //returns 5
```

[Helpful YouTube video](https://www.youtube.com/watch?v=ChWWEncl76Y)

