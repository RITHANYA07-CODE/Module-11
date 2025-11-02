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
# Doubly Linked List: Insert and Search

class Nodeq:
    def __init__(self, data):
        self.data = data
        self.prev = None
        self.next = None


class DoublyLinkedList:
    def __init__(self):
        self.head = None

    def insert_end(self, data):
        new_node = Nodeq(data)
        if self.head is None:
            self.head = new_node
        else:
            temp = self.head
            while temp.next:
                temp = temp.next
            temp.next = new_node
            new_node.prev = temp

    def display(self):
        temp = self.head
        print("The nodes in the doubly linked list are :")
        while temp:
            print(temp.data)
            temp = temp.next

    def search(self, key):
        print(f"The element {key} is being searched...")
        temp = self.head
        position = 1
        while temp:
            if temp.data == key:
                print("The node is present in the list at position :")
                print(position)
                return
            temp = temp.next
            position += 1
        print("The node isn't present in the list")


# --- Main Program ---
if __name__ == "__main__":
    dll = DoublyLinkedList()
    print("Elements are being added to the doubly linked list")

    # Insert elements as per expected output
    dll.insert_end(10)
    dll.insert_end(24)
    dll.insert_end(54)
    dll.insert_end(77)
    dll.insert_end(24)
    dll.insert_end(0)

    dll.display()

    # Search elements
    dll.search(77)
    dll.search(7)

```

## Sample Output
<img width="1051" height="441" alt="image" src="https://github.com/user-attachments/assets/4103ca9c-4d0e-44d9-a17b-1240d00359a8" />

## Result
Thus this Python program demonstrates the implementation of a **Doubly Linked List** where you can insert elements at both the beginning and the end of the list. Additionally, it allows you to search for a specific element in the list.
