# Experiment 9(b): Binary Search Tree

## Aim
To write a Python program to build a Binary Search Tree (BST) using a built-in function.

---

## Algorithm

1. Start the program.
2. Import the `Node` class from the `binarytree` module.
3. Define a function `_build_bst_from_sorted_values()` to build a BST recursively from a sorted list.
4. Define a function `left_subtree()` to print the values in the left subtree of the BST.
5. Accept input from the user for the number of elements.
6. Read the elements into a list.
7. Sort the list.
8. Build the BST by calling `_build_bst_from_sorted_values()` with the sorted list.
9. Print the postorder traversal of the BST.
10. Print the left subtree values.
11. Check and print whether the built tree is a Binary Search Tree.
12. End the program.

---

## Program

```
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
<img width="737" height="205" alt="image" src="https://github.com/user-attachments/assets/fbb15adb-a011-4428-850e-b6744f66c896" />


## RESULT
Thus, the python code is written and executed successfully.
