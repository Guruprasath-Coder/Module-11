# 📚 Doubly Linked List: Insert Elements at the End of a Doubly Linked List

This Python program demonstrates the creation and manipulation of a **Doubly Linked List** where elements can be inserted at the **end** of the list. The program also provides a method to traverse the list and display the elements.

---

## 🎯 Aim

To write a Python program that:
- Implements a **Doubly Linked List**.
- Allows insertion of elements at the end of the list.
- Provides functionality to traverse the list and display its elements.

---

## 🧠 Algorithm

1. **Step 1:** Define a class `Node` to represent each node in the doubly linked list with attributes:
   - `item` for storing the data of the node.
   - `nref` for storing the reference to the next node.
   - `pref` for storing the reference to the previous node.

2. **Step 2:** Define a class `DoublyLinkedList` with:
   - `start_node` to point to the first node of the list.

3. **Step 3:** Define methods in the `DoublyLinkedList` class:
   - `insert_in_emptylist(data)` to insert an element when the list is empty.
   - `insert_at_end(data)` to insert elements at the end of the list.
   - `traverse_list()` to traverse the list and print the elements.

4. **Step 4:** Create an instance of `DoublyLinkedList` and use the `insert_at_end()` method to insert elements into the list.

5. **Step 5:** Use the `traverse_list()` method to print the elements of the list.

---

## 💻 Program
```python
# Node class
class Node:
    def __init__(self, item):
        self.item = item      # data stored in the node
        self.nref = None      # reference to next node
        self.pref = None      # reference to previous node


# Doubly Linked List class
class DoublyLinkedList:
    def __init__(self):
        self.start_node = None

    # Insert in empty list
    def insert_in_emptylist(self, data):
        if self.start_node is None:
            new_node = Node(data)
            self.start_node = new_node
        else:
            print("The list is not empty!")

    # Insert at end
    def insert_at_end(self, data):
        if self.start_node is None:
            self.insert_in_emptylist(data)
            return
        n = self.start_node
        while n.nref is not None:
            n = n.nref
        new_node = Node(data)
        n.nref = new_node
        new_node.pref = n

    # Traverse the list
    def traverse_list(self):
        if self.start_node is None:
            print("The list is empty!")
            return
        else:
            n = self.start_node
            print("Doubly Linked List elements:", end=" ")
            while n is not None:
                print(n.item, end=" ")
                n = n.nref
            print()


# ---- Main Program ----
dll = DoublyLinkedList()

print("Inserting elements at the end of Doubly Linked List:")
dll.insert_at_end(10)
dll.insert_at_end(20)
dll.insert_at_end(30)
dll.insert_at_end(40)

# Traverse and display
dll.traverse_list()


## Sample Output
Inserting elements at the end of Doubly Linked List:
Doubly Linked List elements: 10 20 30 40

## Result

The Python program successfully implemented a Doubly Linked List where:

Elements were inserted at the end of the list.

The list was traversed and displayed correctly
