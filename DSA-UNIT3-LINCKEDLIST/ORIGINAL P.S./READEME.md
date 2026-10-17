# Food Order Management System Using Singly Linked List in C++

## 1. Problem Statement

To implement a Food Order Management System using a singly linked list in C++. Each node stores the Order ID, Customer Name, and Food Name. The system allows users to add new orders, display all pending orders, and complete orders by removing them from the list.

## 2. Approach

1. Define a node structure containing Order ID, Customer Name, Food Name, and a pointer to the next node.
2. Initialize the linked list as empty.
3. Insert new food orders into the linked list.
4. Display all pending orders by traversing the list from the first node to the last node.
5. Complete an order by removing it from the linked list.
6. Update the links after insertion or deletion.
7. Display the updated list after each operation.
8. Release dynamically allocated memory before terminating the program.

## 3. Complexity Analysis

Let:
- `n` = number of orders in the linked list.

### Time Complexity

| Operation | Complexity |
|---|---|
| Create a new node | O(1) |
| Insert at the beginning | O(1) |
| Insert at the end without a tail pointer | O(n) |
| Display all orders | O(n) |
| Delete the first order | O(1) |
| Search for an order | O(n) |
| Delete all orders | O(n) |

**Overall Time Complexity:** O(n) for a single traversal-based operation. Inserting all `n` orders individually at the end takes O(n²) time if no tail pointer is maintained.

### Space Complexity

| Operation | Auxiliary Space |
|---|---|
| Create a new node | O(1) |
| Insert an order | O(1) auxiliary space |
| Display all orders iteratively | O(1) auxiliary space |
| Delete the first order | O(1) |
| Store all `n` orders | O(n) total space |

**Overall Space Complexity:** O(n), because each order requires one node in the linked list.

## 4. Conclusion

The Food Order Management System successfully manages food orders using a singly linked list. It supports order insertion, display, and deletion. This project demonstrates dynamic memory allocation, linked-list traversal, insertion, deletion, and time and space complexity analysis.

