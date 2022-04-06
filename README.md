# Data-structure-and-Algorithm
------------------------------------------------------------------------------------------------------------------
## Data-Structure and it's types
- Data structure is a storage that is used to store and organize data. It is a way of arranging data on a computer so that it can be accessed and updated efficiently.
- Depending on your requirement and project, it is important to choose the right data structure for your project. For example, if you want to store data sequentially in the memory, then you can go for the Array data structure.
- Basically, data structures are divided into two categories:
  - **Linear data structure** : In linear data structures, the elements are arranged in sequence one after the other. Since elements are arranged in particular order, they are easy to implement.
    - **Array** : In an array, elements in memory are arranged in continuous memory. All the elements of an array are of the same type.
    - **Stack** : In stack data structure, elements are stored in the LIFO principle. That is, the last element stored in a stack will be removed first.
    - **Queue** : Unlike stack, the queue data structure works iUnlike linear data structures, elements in non-linear data structures are not in any sequence. Instead they are arranged in a hierarchical manner where one element will be connected to one or more elements.n the FIFO principle where first element stored in the queue will be removed first.
    - **Linked List** : In linked list data structure, data elements are connected through a series of nodes. And, each node contains the data items and address to the next node.
  - **Non linear data structures** : Unlike linear data structures, elements in non-linear data structures are not in any sequence. Instead they are arranged in a hierarchical manner where one element will be connected to one or more elements. 
    -  **Graph** : In graph data structure, each node is called vertex and each vertex is connected to other vertices through edges.
    -  **Trees** : Similar to a graph, a tree is also a collection of vertices and edges. However, in tree data structure, there can only be one edge between two vertices.
--------------------------------------------------------
## Array
- Array is a container which can hold a fix number of items and these items should be of the same type.
- Element − Each item stored in an array is called an element.
- Index − Each location of an element in an array has a numerical index, which is used to identify the element.
### Traverse − print all the array elements one by one.
```
#include <stdio.h>
int main() 
{
   int Arr[] = {1,3,5,7,8};
   int length = sizeof(Arr)/sizeof(Arr[0]);
   int index = 0;  
   for(index = 0; index<length; index++) {
      printf("Arr[%d] = %d \n", index, Arr[index]);
   }
   return 0;
}
```
### Insertion − Adds an element at the given index.
```
#include <stdio.h>
int main()
{
	int arr[] = {1,2,3,4,5,6,7,8,9,10};
	int length = sizeof(arr)/sizeof(arr[0]);
    
	// print the original array
	for (int index = 0; index < length; index++){
		printf("%d ", arr[index]);}
	printf("\n");

	int x   = 50; // element to be inserted
	int pos = 5;  // position 

	// increase the size by 1
	length++;

	// shift elements forward
	for (int index = length-1; index >= pos; index--){
		arr[index] = arr[index - 1];}

	// insert x at pos
	arr[pos - 1] = x;

	// print the updated array
	for (int index = 0; index < length; index++){
		printf("%d ", arr[index]);}
	printf("\n");

	return 0;
}
```

### Deletion − Deletes an element at the given index.
```
#include <stdio.h>
int main() {
   int arr[] = {1,3,5,7,8};
   int length = sizeof(arr)/sizeof(arr[0]);
   int pos = 3;
   
   printf("The original array elements are :\n");
   for(int index = 0; index<length; index++) {
      printf("arr[%d] = %d \n", index, arr[index]);
   }
   
   //deletion    
   length--;
   for(int index = pos-1; index < length; index++){
         arr[index] = arr[index+1];
   }
	
   printf("The array elements after deletion :\n");
   for(int index = 0; index<length; index++) {
      printf("arr[%d] = %d \n", index, arr[index]);
   }
   return 0;
}
```


### Search − Searches an element using the given index or by the value.```
**Linear-Search**
```
#include <iostream>
using namespace std;

int search(int arr[], int n, int x)
{
	int i;
	for (i = 0; i < n; i++)
		if (arr[i] == x)
			return i;
	return -1;
}

// Driver code
int main(void)
{
	int arr[] = { 2, 3, 4, 10, 40 };
	int query = 10;
	int length = sizeof(arr) / sizeof(arr[0]);

	// Function call
	int result = search(arr, length, query);
	(result == -1)
		? cout << "Element is not present in array"
		: cout << "Element is present at index " << result;
	return 0;
}
```

**Binary-Search**
```
#include <bits/stdc++.h>
using namespace std;

int binarySearch(int arr[], int low, int high, int x)
{
	while (low <= high) {
		int mid = (low + high)/2;
		if (arr[mid] == x)   return mid;
		if (arr[mid] < x)    low = mid + 1;
		else                 high = mid - 1;
	}
	return -1;
}

int main(void)
{
	int arr[] = { 2, 3, 4, 10, 40 };
	int query = 10;
	int length = sizeof(arr) / sizeof(arr[0]);
	int result = binarySearch(arr, 0, length-1, query);
	(result == -1)
		? cout << "Element is not present in array"
		: cout << "Element is present at index " << result;
	return 0;
}
```
----------------------------------------------------------------------------------------------------------
## Linear Linked-List 
![image](https://user-images.githubusercontent.com/68856476/161975615-ae392b18-eb3f-4889-9327-c544224fdbc9.png))
- A linked list is a linear data structure that includes a series of connected nodes. Here, each node stores the data and the address of the next node.
```
#include <bits/stdc++.h>
using namespace std;

class Node {
public:
	int data;
	Node* next;
};

void traverse(Node* n)
{
    while (n != NULL) {
        cout << n->data << " ";
        n = n->next;
    }
}

int main()
{
	Node* head = NULL;
	Node* second = NULL;
	Node* third = NULL;

	// allocate 3 nodes in the heap
	head = new Node();
	second = new Node();
	third = new Node();

	head->data = 1; 
	head->next = second; 

	second->data = 2;
	second->next = third;


	third->data = 3; 
	third->next = NULL;
	
	traverse(head);
	
	return 0;
}
```
-----------------------------------------------------------------------------------------------------
## Circular-Linked-List
![image](https://user-images.githubusercontent.com/68856476/161979353-da9e75c1-f10d-477a-aefe-62b9fc1b06c0.png)
- Circular linked list is a linked list where all nodes are connected to form a circle. There is no NULL at the end.
- Any node can be a starting point. We can traverse the whole list by starting from any point. We just need to stop when the first visited node is visited again
-----------------------------------------------------------------------------------------------------
## Doubly-Linked-List
![image](https://user-images.githubusercontent.com/68856476/161984418-876f902f-542f-4115-a4ed-f6a2e00423e3.png)
- A Doubly Linked List (DLL) contains an extra pointer, typically called previous pointer, together with next pointer and data which are there in singly linked list.
- A DLL can be traversed in both forward and backward direction. 
- The delete operation in DLL is more efficient if pointer to the node to be deleted is given. 
- We can quickly insert a new node before a given node. 
```
/* Node of a doubly linked list */
class Node
{
    public:
    int data;
    Node* next; // Pointer to next node in DLL
    Node* prev; // Pointer to previous node in DLL
};
```
----------------------------------------------------------------------------------------------------------
## Headed-Linked-List
![image](https://user-images.githubusercontent.com/68856476/161985261-17c104b0-f401-444a-943a-666dfa99309e.png)
- A header node is a special node that is found at the beginning of the list. A list that contains this type of node, is called the header-linked list. This type of list is useful when information other than that found in each node is needed.
- For example, suppose there is an application in which the number of items in a list is often calculated. Usually, a list is always traversed to find the length of the list. However, if the current length is maintained in an additional header node that information can be easily obtained.
--------------------------------------------------------------------------------------------------------
## Stack
- A stack is an abstract data structure that contains a collection of elements. 
- Stack implements the LIFO mechanism i.e. the element that is pushed at the end is popped out first. 
- Some of the principle operations in the stack are −
  - **Push** - This adds a data value to the top of the stack.
  - **Pop** - This removes the data value on top of the stack
  - **Peek** - This returns the top data value of the stack
```
#include <iostream>
using namespace std;
int stack[100], n=100, top=-1;
void push(int val) {
   if(top>=n-1)
   cout<<"Stack Overflow"<<endl;
   else {
      top++;
      stack[top]=val;
   }
}
void pop() {
   if(top<=-1)
   cout<<"Stack Underflow"<<endl;
   else {
      cout<<"The popped element is "<< stack[top] <<endl;
      top--;
   }
}
void display() {
   if(top>=0) {
      cout<<"Stack elements are:";
      for(int i=top; i>=0; i--)
      cout<<stack[i]<<" ";
      cout<<endl;
   } else
   cout<<"Stack is empty";
}
int main() {
   int ch, val;
   cout<<"1) Push in stack"<<endl;
   cout<<"2) Pop from stack"<<endl;
   cout<<"3) Display stack"<<endl;
   cout<<"4) Exit"<<endl;
   do {
      cout<<"Enter choice: "<<endl;
      cin>>ch;
      switch(ch) {
         case 1: {
            cout<<"Enter value to be pushed:"<<endl;
            cin>>val;
            push(val);
            break;
         }
         case 2: {
            pop();
            break;
         }
         case 3: {
            display();
            break;
         }
         case 4: {
            cout<<"Exit"<<endl;
            break;
         }
         default: {
            cout<<"Invalid Choice"<<endl;
         }
      }
   }while(ch!=4);
   return 0;
}
```
---------------------------------------------------------------------------------------------------------------
## Queue
- A queue is an abstract data structure that contains a collection of elements. Queue implements the FIFO mechanism i.e. the element that is inserted first is also deleted first. In other words, the least recently added element is removed first in a queue
```
#include <iostream>
using namespace std;
int queue[100], n = 100, front = - 1, rear = - 1;
void Insert() {
   int val;
   if (rear == n - 1)
   cout<<"Queue Overflow"<<endl;
   else {
      if (front == - 1)
      front = 0;
      cout<<"Insert the element in queue : "<<endl;
      cin>>val;
      rear++;
      queue[rear] = val;
   }
}
void Delete() {
   if (front == - 1 || front > rear) {
      cout<<"Queue Underflow ";
      return ;
   } else {
      cout<<"Element deleted from queue is : "<< queue[front] <<endl;
      front++;;
   }
}
void Display() {
   if (front == - 1)
   cout<<"Queue is empty"<<endl;
   else {
      cout<<"Queue elements are : ";
      for (int i = front; i <= rear; i++)
      cout<<queue[i]<<" ";
         cout<<endl;
   }
}
int main() {
   int ch;
   cout<<"1) Insert element to queue"<<endl;
   cout<<"2) Delete element from queue"<<endl;
   cout<<"3) Display all the elements of queue"<<endl;
   cout<<"4) Exit"<<endl;
   do {
      cout<<"Enter your choice : "<<endl;
      cin>>ch;
      switch (ch) {
         case 1: Insert();
         break;
         case 2: Delete();
         break;
         case 3: Display();
         break;
         case 4: cout<<"Exit"<<endl;
         break;
         default: cout<<"Invalid choice"<<endl;
      }
   } while(ch!=4);
   return 0;
}
```
-------------------------------------------------------------------------------------------------------------------
