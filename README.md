# Notes-for-ONLINE-link
Class Notes for online class
Link List  - From the book  Chap 20   - These are just HIGHLIGHTS – look in the book for the actual code
The List interface extends the Collection interface and defines a collection for storing elements in a sequential order. To create a list, use one of its two concrete classes: ArrayList or LinkedList.

ArrayList and LinkedList are defined under the List interface. The List interface extends Collection to define an ordered collection with duplicates allowed.

LinkedList is a linked list implementation of the List interface. In addition to implementing the List interface, this class provides the methods for retrieving, inserting, and removing elements from both ends of the list, as shown in Figure 20.6. A LinkedList can be constructed using its no-arg constructor 

Since MyArrayList is implemented using an array, the methods get(int index) and set(int index, E e) for accessing and modifying an element through an index and the add(E e) method for adding an element at the end of the list are efficient. However, the methods add(int index, E e) and remove(int index) are inefficient because they require shifting a potentially large number of elements. You can use a linked structure to implement a list to improve efficiency for adding and removing an element at the beginning of a list.

In a linked list, each element is contained in an object, called the node. When a new element is added to the list, a node is created to contain it. Each node is linked to its next neighbor, as shown in Figure 24.7.
Figure 24.7 A linked list consists of any number of nodes chained together.
 













Figure 24.7 Full Alternative Text
A node can be created from a class defined as follows:

class Node<E> {
  E element;
  Node<E> next;

  public Node(E e) {
    element = e;
  }
}
We use the variable head to refer to the first node in the list and the variable tail to the last node. If the list is empty, both head and tail are null. Here is an example that creates a linked list to hold three nodes. Each node stores a string element.



The MyLinkedList class uses a linked structure to implement a dynamic list. 

It implements MyList. 

In addition, it provides the methods addFirst, addLast, removeFirst, removeLast, getFirst, and getLast, as shown in Figure 24.11.
Figure 24.11 MyLinkedList implements a list using a linked list of nodes.


Draw a diagram to show the linked list after each of the following statements is executed.
MyLinkedList<Double> list = new MyLinkedList<>();
list.add(1.5);
list.add(6.2);
list.add(3.4);
list.add(7.4);
list.remove(1.5);
list.remove(2);





Note
In a singly linked list, removeLast() takes O(n) time. In a doubly linked list, removeLast() can be implemented to take O(1) time. The LinkedList in the Java API is implemented using a doubly linked list. See CheckPoint 24.4.5.1.



