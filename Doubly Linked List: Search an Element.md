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
```
class Node q:
def init (self, data): 
   self.data = data 
   self.next = None 
   self.prev = None
class DoublyLinkedList: 
   def init (self):
      self.head = None
   def insert_beginning(self,data): 
      new_node = Nodeq(data) 
      if(self.head == None):
         self.head = new_node 
         return
      self.head.prev = new_node 
      new_node.next = self.head 
      self.head = new_node

def insert_end(self, new_data): 
      new_node = Nodeq(new_data) 
      if self.head is None:
         new_node.prev = None 
         self.head = new_node 
         return
      last = self.head 
while last.next:
      last = last.next 
      last.next = new_node 
      new_node.prev = last
def search(self,data): 
      current = self.head 
while current:
      if current.data == data: 
         return True
      current = current.next
print("The given data doesnot exist:") 
      return False
Dllist = DoublyLinkedList() 
Dllist.insert_beginning(2) 
Dllist.insert_end(0) 
Dllist.insert_end(1) 
print(Dllist.search(0)) 
print(Dllist.search(3))
```
## Sample Output
![image](https://github.com/user-attachments/assets/c33c09b5-84d2-4382-a1e9-b8522a49b7eb)

## Result
Thus the program has been successfully execute
