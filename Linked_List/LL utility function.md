when we have any data structure, we have to think about utility function as how we are going to use the given data structure.

Utility Functions for Linked List:

* Traverse a Linked List.
* operations performed on DS as search an element,  delete or insert an element etc.



### Traverse a Linked List:

void traverse(struct node *head)
{
​    struct node *temp;
​    temp=head;
​    while(temp!=null)
​    {
​        pf(temp->data)
​        temp=temp->next;
​    }
​    
}



### **Utility Functions:**

##### 1) How many extra pointers we need, to delete a single node from the linked list.

![Linked List](https://drive.google.com/file/d/1z6Pq_EdiJ3bNVxS3F6gTASOYeNUBqdnZ/view?usp=sharing)

In the above example, if we want to delete node 3, then take a temporary pointer lets say temp when you traverse LL, then check whether temp -> next ->==3 if this condition is true then temp->next=temp->next->next. 



##### 2) Given only a pointer/reference to a node to be deleted in a singly linked list, how do you delete it?



sol: there are two solutions for this problem:

A **simple solution** is to traverse the linked list until you find the node you want to delete. But this solution requires pointer to the head node which contradicts the problem statement.

**Fast solution** is to copy the data from the next node to the node to be deleted and delete the next node. Something like following.

```
struct Node *temp  = node_ptr->next;
    node_ptr->data  = temp->data;
    node_ptr->next  = temp->next;
    free(temp);
```

![Linked List](https://drive.google.com/file/d/1z6Pq_EdiJ3bNVxS3F6gTASOYeNUBqdnZ/view?usp=sharing)



##### 3) Given a singly LL, find the middle element in single traversal.

There are two approach to solve this problem:

`a) Approach 1:

Traverse the whole linked list and count the no. of nodes. Now traverse the list again till count/2 and return the node at count/2.

psudo code:

`` Traverse the LL`

`calculate the size, do (n/2)`

`Traverse again till n/2`



b) Approach 2:

**slow and fast pointer:** take two pointers, move one at one position at a time and the other one at the two position at the time. When the fast pointer reaches end slow pointer will reach middle of the linked list. Here, we have to take care of dangling pointer also.

![Linked List](https://drive.google.com/file/d/1qrZT6OfWdvtJaoZZdKQZdYY_np-IgPGU/view?usp=sharing)

c) Approach 3:

Initialize mid element as head and initialize a counter as 0. Traverse the list from head, while traversing increment the counter and change mid to mid->next whenever the counter is odd. So the mid will move only half of the total length of the list.



##### 4) Given a linked list, find the kth element from the last.

let's say we have n number of nodes in a linked list.

Approach 1)

1) Calculate the length of Linked List. let's say it is len.
2) traverse the (len – n + 1)th node from the beginning of the LL.

Approach 2:

* Maintain two pointers – let's say p and q. 

*  Initialize both reference pointer to the head. 

* Move q pointer till k. 

* Now maintain gap of k. 

* Move both the pointers till q reaches end and then return p.

*  p will point to the kth element from last.

  In 2nd approach we are traversing only single time.



##### 5) Write a function to get the intersection point of two Linked Lists.

**Method (Using difference of node counts)**
1) Get count of the nodes in the first list, let count be c1.
2) Get count of the nodes in the second list, let count be c2.
3) Get the difference of counts d = abs(c1 – c2)
4) Now traverse the bigger list from the first node till d nodes so that from here onwards both the lists have equal no of nodes.
5) Then we can traverse both the lists in parallel till we come across a common node. (Note that getting a common node is done by comparing the address of the nodes)


