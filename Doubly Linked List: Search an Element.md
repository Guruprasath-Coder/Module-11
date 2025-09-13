# 📝 Doubly Linked List: Search an Element

This Python program demonstrates the implementation of a **Doubly Linked List** where you can insert elements at both the beginning and the end of the list. Additionally, it allows you to search for a specific element in the list.

---

## 🎯 Aim

To write a Python program that:
- Implements a **Doubly Linked List** with functions to insert elements at the beginning and the end of the list.
- Implements a search function to check if a given element exists in the list.

---

## 🧠 Algorithm

1. **Step 1:** Define a class `Nodeq` with:
   - `data` to store the node's value.
   - `next` to store the reference to the next node.
   - `prev` to store the reference to the previous node.

2. **Step 2:** Define a class `DoublyLinkedList` with:
   - `head` to point to the first node.

3. **Step 3:** In the `DoublyLinkedList` class, define methods:
   - `insert_beginning(data)` to insert a node at the beginning.
   - `insert_end(data)` to insert a node at the end.
   - `search(data)` to search for an element in the list.

4. **Step 4:** Create an instance of `DoublyLinkedList`.
   - Insert elements at the beginning and end.
   - Search for specific elements.

---

## 💻 Program
```python
# Node class
class Nodeq:
    def __init__(self, data):
        self.data = data      # store data
        self.next = None      # pointer to next node
        self.prev = None      # pointer to previous node


# Doubly Linked List class
class DoublyLinkedList:
    def __init__(self):
        self.head = None

    # Insert at beginning
    def insert_beginning(self, data):
        new_node = Nodeq(data)
        if self.head is None:
            self.head = new_node
        else:
            new_node.next = self.head
            self.head.prev = new_node
            self.head = new_node

    # Insert at end
    def insert_end(self, data):
        new_node = Nodeq(data)
        if self.head is None:
            self.head = new_node
            return
        temp = self.head
        while temp.next is not None:
            temp = temp.next
        temp.next = new_node
        new_node.prev = temp

    # Search for an element
    def search(self, data):
        temp = self.head
        position = 1
        while temp is not None:
            if temp.data == data:
                return f"Element {data} found at position {position}."
            temp = temp.next
            position += 1
        return f"Element {data} not found in the list."

    # Traverse the list
    def traverse(self):
        if self.head is None:
            print("The list is empty.")
        else:
            temp = self.head
            print("Doubly Linked List elements:", end=" ")
            while temp is not None:
                print(temp.data, end=" ")
                temp = temp.next
            print()


# ---- Main Program ----
dll = DoublyLinkedList()

# Insert elements at beginning and end
dll.insert_beginning(30)
dll.insert_beginning(20)
dll.insert_end(40)
dll.insert_end(50)

# Display the list
dll.traverse()

# Search elements
print(dll.search(20))   # Element present
print(dll.search(50))   # Element present
print(dll.search(100))  # Element not present


## Sample Output
Doubly Linked List elements: 20 30 40 50
Element 20 found at position 1.
Element 50 found at position 4.
Element 100 not found in the list.

## Result

The Python program successfully implemented a Doubly Linked List with:

Insertion at the beginning and end.

A search function to check if an element exists in the list.

Correct traversal and output display.
