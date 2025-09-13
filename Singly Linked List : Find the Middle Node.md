# 📚 Singly Linked List : Find the Middle Node of a Singly Linked List Using Recursion

This Python program demonstrates how to find the middle node of a singly linked list using recursion. The program calculates the middle element by utilizing two pointers, with one pointer moving one step at a time (slow) and the other moving two steps at a time (fast). When the fast pointer reaches the end of the list, the slow pointer will be at the middle node.

## 🎯 Aim

To write a Python program that:
- Creates a singly linked list.
- Uses recursion to find the middle node of the list.
- In case of an even number of nodes, it returns the second middle element.

## 🧠 Algorithm

1. **Node Class**: 
   - Define a `Node` class to represent each node in the singly linked list. Each node has two attributes: `data` and `next`.
   
2. **LinkedList Class**:
   - Define a `LinkedList` class that manages the linked list with methods to:
     - `append(data)`: Add a new node to the end of the list.
     - `get_middle_recursive(slow, fast)`: A recursive helper function to find the middle node using two pointers (slow and fast).
     - `find_middle()`: A method to call the recursive function and return the middle node's data.

3. **Input**:
   - First, the program reads an integer `n`, representing the number of elements in the linked list.
   - Then, it reads `n` space-separated integers to form the linked list.

4. **Recursive Middle Finding**:
   - The `get_middle_recursive` method uses two pointers to traverse the list:
     - The `slow` pointer moves one step at a time.
     - The `fast` pointer moves two steps at a time.
   - When the `fast` pointer reaches the end, the `slow` pointer will be at the middle node.

5. **Output**:
   - The program prints the middle element. If the list has an even number of nodes, it returns the second middle element.

---

## 💻 Program
```python
# Node class for singly linked list
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None


# LinkedList class
class LinkedList:
    def __init__(self):
        self.head = None

    # Append node at the end
    def append(self, data):
        new_node = Node(data)
        if not self.head:
            self.head = new_node
            return
        temp = self.head
        while temp.next:
            temp = temp.next
        temp.next = new_node

    # Recursive function to find middle
    def get_middle_recursive(self, slow, fast):
        # Base case: if fast reaches end or fast.next is None
        if fast is None or fast.next is None:
            return slow
        # Recursive call: slow moves 1 step, fast moves 2 steps
        return self.get_middle_recursive(slow.next, fast.next.next)

    # Function to find middle node
    def find_middle(self):
        if not self.head:
            return None
        middle_node = self.get_middle_recursive(self.head, self.head)
        return middle_node.data


# ---- Main Program ----
if __name__ == "__main__":
    ll = LinkedList()

    # Input number of elements
    n = int(input("Enter number of elements: "))
    values = list(map(int, input("Enter elements: ").split()))

    for val in values:
        ll.append(val)

    # Find and print middle
    middle = ll.find_middle()
    print("Middle element:", middle)


## Sample Input & Output
Enter number of elements: 5
Enter elements: 10 20 30 40 50

Middle element: 30

## Result

The Python program successfully implemented a Singly Linked List and found the middle node using recursion.

For odd number of nodes, it returns the exact middle.

For even number of nodes, it returns the second middle element.

