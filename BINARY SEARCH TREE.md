
# Ex. No: 15B - Build a Binary Search Tree Using Built-in Function

## AIM:
To write a Python program to build a binary search tree using a built-in function.

---

## ALGORITHM:

1. **Start the program.**
2. Define `_build_bst_from_sorted_values(sorted_values)` to recursively build a binary search tree (BST) from a sorted list.
3. Define `left_subtree(l)` to print the left subtree of the BST.
4. Take user input for the number of elements and store the values in a list `a`.
5. Sort the list and pass it to `_build_bst_from_sorted_values()` to construct the BST.
6. Print the postorder traversal of the BST.
7. Call `left_subtree(l)` to print the left subtree.
8. Check whether the tree is a binary search tree using the `is_bst` property.
9. **End the program.**

---

## PROGRAM:

```python
from binarytree import Node
def bst(x):
    
    if len(x)==0:
        return None
    mid=len(x)//2
    root=Node(x[mid])
    root.left=bst(x[:mid])
    root.right=bst(x[mid+ 1 :])
    return (root)
    
x=[8,5,14,1,7,10,20]
root=bst(sorted(x))
print("BST before insertion:")
for i in root.values:
    print(i,'-->',end='')
x.append(int(input()))
root=bst(sorted(x))
print("\nBST after insertion:")
for i in root.values:
    print(i,'-->',end='')
```

## OUTPUT

<img width="737" height="205" alt="image" src="https://github.com/user-attachments/assets/c72e7e84-b5ee-4a7f-acf3-3328f09857ed" />

## RESULT

Thus, the python code is written and executed successfully.
