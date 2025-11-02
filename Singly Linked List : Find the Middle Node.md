# 📚 Singly Linked List : Search an element

This Python program demonstrates the implementation of a **Doubly Linked List**, allowing insertion of elements at both the **beginning** and **end** of the list. It also includes a **search function** to check whether a specific element exists in the list.

## 🎯 Aim

To write a Python program that:

* Implements a **Doubly Linked List** with the ability to insert elements at the beginning and end.
* Implements a **search operation** to check whether a given element exists in the list.
  
## 🧠 Algorithm

1. **Step 1:**
   Define a class `Nodeq` to represent each node, containing:

   * `data` → stores the value.
   * `next` → reference to the next node.
   * `prev` → reference to the previous node.

2. **Step 2:**
   Define a class `DoublyLinkedList` that contains:

   * A pointer `head` that refers to the first node of the list.

3. **Step 3:**
   Implement methods inside `DoublyLinkedList`:

   * `insert_beginning(data)` — Inserts a node at the beginning of the list.
   * `insert_end(data)` — Inserts a node at the end of the list.
   * `search(data)` — Searches for a node with the given value and returns whether it exists.

4. **Step 4:**
   Create an instance of `DoublyLinkedList`, perform insertions at both ends, and use the search function to check for specific values.

---

## 💻 Program
```
class Nodeq: 
    def __init__(self, data): 
        self.data = data 
        self.next = None
        self.prev = None

class DoublyLinkedList: 

    def __init__(self): 
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
        temp = self.head
        while temp:
            if temp.data==data:
                break
            temp = temp.next
        if temp==None:
            print("The given data doesnot exist:")
            return False
        return True

Dllist = DoublyLinkedList() 
Dllist.insert_beginning(2)
Dllist.insert_end(0)
Dllist.insert_end(1)
print(Dllist.search(0)) 
print(Dllist.search(3))  
```

## Sample Input & Output
<img width="679" height="201" alt="image" src="https://github.com/user-attachments/assets/06f5648f-c1cb-4fb6-b675-f2a49ed2b24d" />

## Result
The program successfully:

* Implements a **Doubly Linked List**.
* Allows insertion at both the **beginning** and **end**.
* Enables **searching** for a specific element and displays whether it exists in the list.

