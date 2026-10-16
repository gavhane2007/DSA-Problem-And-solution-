# Mirror Image of Binary Tree in C++

## 1. Problem Statement

To implement a binary search tree (BST) in C++ and generate its mirror image by swapping the left and right child nodes of every node recursively.

**Modified Problem:** Perform the mirror operation twice to restore the original tree structure and display the original tree, its mirror image, and the restored tree using inorder traversal.

## 2. Approach

1. Create a binary search tree by inserting the given node values.
2. Display the original tree using inorder traversal.
3. Perform the first mirror operation by swapping the left and right children of every node recursively.
4. Display the mirror image using inorder traversal.
5. Perform the mirror operation a second time to restore the original tree structure.
6. Display the restored tree using inorder traversal.
7. Delete the tree to release dynamically allocated memory.

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
| Display original tree | O(n) |
| First mirror operation | O(n) |
| Display mirror image | O(n) |
| Second mirror operation | O(n) |
| Display restored tree | O(n) |
| Delete the tree | O(n) |
| Overall worst-case time complexity | O(n²) |

### Space Complexity

| Operation | Auxiliary Space |
|---|---|
| Recursive insertion | O(h) per insertion |
| Inorder traversal | O(h) |
| First mirror operation | O(h) |
| Second mirror operation | O(h) |
| Delete the tree | O(h) |
| Overall worst-case auxiliary space | O(n) |

**Note:**
- For a balanced BST, the height is O(log n).
- For a skewed BST, the height is O(n).
- Mirroring the tree twice takes O(n) time overall because each mirror operation takes O(n) time.
- The overall worst-case time complexity is O(n²) because of BST insertion.

## 4. Conclusion

The modified program creates a binary search tree and generates its mirror image by swapping the left and right child nodes recursively. It then performs the mirror operation a second time to restore the original tree structure. The original, mirrored, and restored trees are displayed using inorder traversal. This modification demonstrates recursion, binary tree manipulation, and time and space complexity analysis.
