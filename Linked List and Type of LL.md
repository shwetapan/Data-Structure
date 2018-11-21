#                                                                                                 <u>Linked List</u>



Linked List is another type of linear data structure in which you access the data element in linear order. Here, each element is represented by different object. Each object consist of two parts:  the data and its address. Every node stores the address of next node, so that you can directly traverse the next node, that is what called as link. Hence, the whole arrangement of nodes is called as linked list. 

##### Important things to consider for LL:

For LL, we need a head as a reference from whether the linked list starts.





![Linked List](https://drive.google.com/file/d/1jE9Hlb3D9xW6AuRCQQ6wZ4irg_sDf7Fi/view?usp=sharing)



A linked list uses dynamic allocation of memory. It is best suitable for object, whether it needs to deal with unknown number of objects. 

##### Advantages of Linked List

- Dynamic allocation of memory.

- Insertion and deletion is easy as compare to array.


##### Disadvantages of Linked List:

- It does not give the feasibility of direct addressing
- If you want to access the particular node of LL, you have to traverse the whole list. for example: it is easy to calculate the length of array in comparison to calculating the length of linked list.



## <u>Types of Linked List</u>

#### Singly Linked List

In singly LL, each node stores the data  and the address of next node only. Here, you can move only a certain direction. It is not possible to move in both direction in singly linked list.

##### structure of singly LL node:

It consist of data value and address of next pointer. It is represented as below:

struct node
{
​    int data;
​    struct node* next;
}




#### Doubly Linked List

In Doubly LL, each node stores the address of next node and previous node, so it is easy to traverse in both the direction in DLL. 

##### structure of Doubly LL node

It consist of data value and address of next node as next and previous node as prev. It is represented as below:

struct node
{
​    int data;
​    struct node* next;
​    struct node* prev;
}


##### Circular Linked List

 circular linked list is a linked list in which the last node pointing  again to the head of LL. Here, the structure of node is same as linked list only the difference is that the last node stores the address of head node.









