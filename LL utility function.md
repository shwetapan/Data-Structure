when we have any data structure, we have to think about utility function as how we are going to use the given data structure.

Utility Functions for Linked List:

* Traverse a Linked List.
* operations performed on DS as search an element,  delete or insert an element etc.
* 

1) How many extra pointers we need, to delete a single node from the singly linked list.

we need 1 extra pointer to delete a node from singly LL.

![Linked List](https://drive.google.com/file/d/1z6Pq_EdiJ3bNVxS3F6gTASOYeNUBqdnZ/view?usp=sharing)

In the above example, if we want to delete node 3, then take a temporary pointer lets say temp when you traverse LL, then check whether temp -> next ->==3 if this condition is true then temp->next=temp->next->next. that means you are placing the next address to 5(check in image) which means 3 will automatically be deleted.

2) Given only a pointer/reference to a node to be deleted in a singly linked list, how do you delete it?

copy  p->data=p->next->data and in next step p will be advanced to p->p->next



![Linked List](https://drive.google.com/file/d/1z6Pq_EdiJ3bNVxS3F6gTASOYeNUBqdnZ/view?usp=sharing)





Traverse a Linked List:

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

