# Food Order Management System Using Doubly Linked List in C++

## 1. Problem Statement

To implement a Food Order Management System using a doubly linked list in C++. Each node stores the Order ID, Customer Name, and Food Name. The system allows users to add new orders, display pending orders, and complete orders by removing them from the list.

**Modified Problem:** Enhance the system by allowing orders to be displayed in both forward and reverse order. This demonstrates bidirectional traversal using a doubly linked list.

## 2. Approach

1. Define a node structure containing Order ID, Customer Name, Food Name, and pointers to the previous and next nodes.
2. Initialize the doubly linked list as empty.
3. Insert new food orders at the end of the list.
4. Display all orders from the first node to the last node.
5. Display all orders in reverse order, from the last node to the first node.
6. Complete an order by removing the first node from the list.
7. Update the previous and next pointers after insertion or deletion.
8. Display the updated order list after each operation.
9. Release dynamically allocated memory before terminating the program.

## 3. Complexity Analysis

Let:
- `n` = number of orders in the linked list.

### Time Complexity

| Operation | Complexity |
|---|---|
| Create a new node | O(1) |
| Insert an order at the end without a tail pointer | O(n) |
| Insert an order at the end with a tail pointer | O(1) |
| Display orders in forward order | O(n) |
| Display orders in reverse order | O(n) |
| Complete the first order | O(1) |
| Search for an order | O(n) |
| Delete all remaining orders | O(n) |

**Overall Time Complexity:** O(n) for a single traversal operation. Inserting all `n` orders individually at the end takes O(n²) time without a tail pointer, or O(n) total time with a tail pointer.

### Space Complexity

| Operation | Auxiliary Space |
|---|---|
| Create a new node | O(1) |
| Insert an order | O(1) auxiliary space |
| Forward traversal | O(1) auxiliary space when iterative |
| Reverse traversal | O(1) auxiliary space when iterative |
| Complete the first order | O(1) |
| Store all `n` orders | O(n) total space |

**Overall Space Complexity:** O(n), because each order requires one node containing data and two pointers.

## 4. Conclusion

The modified Food Order Management System manages food orders using a doubly linked list. It supports insertion, deletion, forward traversal, and reverse traversal. The modification demonstrates bidirectional traversal and the use of previous and next pointers in a doubly linked list.

