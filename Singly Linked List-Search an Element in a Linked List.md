# # 🔍 Singly Linked List-To Search an Element in a Linked List

This project contains a simple implementation of a **singly linked list** in Python, allowing insertion and searching of elements.

---

## 🎯 Aim

To write a Python program to search for a given element in a singly linked list using object-oriented programming principles.

---

## 🧠 Algorithm

1. **Define a Node class** with `data` and `next` attributes.
2. **Define a LinkedList class** with:
   - A `head` pointer initialized to `None`.
   - A `push()` method to add elements at the beginning.
   - A `search()` method to check whether a given value exists.
3. Create a `LinkedList` instance.
4. Insert the elements **10, 30, 11, 21, 14** using `push()` (which results in reverse order).
5. Read an integer input from the user.
6. Use `search()` to check if the element exists in the list.
7. Output **"Yes"** if found, else **"No"**.

---

## 💻 Program
```python
# Node class
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None


# Singly Linked List class
class LinkedList:
    def __init__(self):
        self.head = None

    # Insert at beginning
    def push(self, new_data):
        new_node = Node(new_data)
        new_node.next = self.head
        self.head = new_node

    # Search for an element
    def search(self, key):
        current = self.head
        while current:
            if current.data == key:
                return True
            current = current.next
        return False

    # Display list elements
    def display(self):
        current = self.head
        print("Linked List elements:", end=" ")
        while current:
            print(current.data, end=" ")
            current = current.next
        print()


# ---- Main Program ----
ll = LinkedList()

# Insert given elements using push() (reverse order in list)
for val in [10, 30, 11, 21, 14]:
    ll.push(val)

ll.display()

# Search for user input
key = int(input("Enter element to search: "))
if ll.search(key):
    print("Yes")
else:
    print("No")

## Sample Output
Linked List elements: 14 21 11 30 10
Enter element to search: 21
Yes

Linked List elements: 14 21 11 30 10
Enter element to search: 99
No

## Result
The Python program successfully implemented a Singly Linked List where:

Elements were inserted using push() (added at the beginning).

The search() method correctly determined whether the input element was present in the list.
