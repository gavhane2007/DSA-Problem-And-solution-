# Mirror Image of Binary Tree in C++

## 1. Problem Statement

To implement a binary search tree (BST) in C++ and generate its mirror image by swapping the left and right child nodes of every node recursively. Display the original tree and its mirror image using inorder traversal.

## 2. Approach

1. Create a binary search tree by inserting the given node values.
2. Display the original tree using inorder traversal.
3. Generate the mirror image by swapping the left and right children of every node recursively.
4. Display the mirrored tree using inorder traversal.
5. Delete the tree to release dynamically allocated memory.

## 3. Complexity Analysis

Let:
- `n` = number of nodes in the tree.
- `h` = height of the tree.

### Time Complexity

| Operation | Complexity |
|---|---|
| Create a node | O(1) |
| Insert one node | O(h) |
| Insert all nodes (average case) | O(n log n) |
| Insert all nodes (worst case) | O(n²) |
| Inorder traversal | O(n) |
| Mirror operation | O(n) |
| Delete the tree | O(n) |
| Overall worst-case time complexity | O(n²) |

### Space Complexity

| Operation | Auxiliary Space |
|---|---|
| Recursive insertion | O(h) per insertion |
| Inorder traversal | O(h) |
| Mirror operation | O(h) |
| Delete the tree | O(h) |
| Overall worst-case auxiliary space | O(n) |

**Note:**
- For a balanced BST, the height is O(log n).
- For a skewed BST, the height is O(n).
- The mirror operation takes O(n) time because every node is visited once.

## 4. Conclusion

The program successfully creates a binary search tree and generates its mirror image by swapping the left and right child nodes recursively. The project demonstrates binary search trees, recursion, inorder traversal, and time and space complexity analysis.

