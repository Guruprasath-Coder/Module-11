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
```
def init (self, data): 
   self.data = data 
   self.next = None
class LinkedList:
   def init (self):
      self.head = None
   def push_front(self, newElement): 
      new_node = Node(newElement) 
      new_node.next = self.head 
      self.head = new_node
   def PrintList(self):
      temp = self.head 
      if(temp != None):
         print("The list contains:", end=" ") 
      while (temp != None): 
         print(temp.data, end=" ")
         temp = temp.next 
      print()
      else:
         print("The list is empty.")
MyList = LinkedList()
MyList.push_front(10) 
MyList.push_front(20) 
MyList.push_front(30) 
MyList.PrintList()
```
## Sample Output
![image](https://github.com/user-attachments/assets/99bb3fbc-1a1a-4fe5-aff7-144cd4ea8bc4)

## Result
Thus the program has been successfully executed

