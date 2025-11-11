# Ex. No: 15A - Build a Binary Tree with Float Values

## AIM:
To write a Python program to build a binary tree with a root, left, and right node using floating-point values.

---

## ALGORITHM:

1. **Start the program.**
2. **Import** the `Node` class from the `binarytree` module.
3. **Create a root node** using the `Node` class and assign a floating-point value.
4. **Create left and right child nodes** for the root with float values.
5. **Convert the tree** to a list and print the list of nodes.
6. **End the program.**

---

## PYTHON PROGRAM

```python
from binarytree import Node

def _build_bst_from_sorted_values(sorted_values):
    if len(sorted_values)==0:
        return None
    mid_index=len(sorted_values)//2
    root=Node(sorted_values[mid_index])
    root.left=_build_bst_from_sorted_values(sorted_values[:mid_index])
    root.right=_build_bst_from_sorted_values(sorted_values[mid_index+1:])
    return (root)

def left_subtree(l):
    print("Left Subtree :")
    for i in l[1].values:
        print(i,"-->",end="")
    return

a=[]
size=int(input())
for i in range(0,size):
    val=int(input())
    a.append(val)
x=sorted(a)

l=_build_bst_from_sorted_values(x)
print("Postorder :",l.postorder)
left_subtree(l)
print("\nIs this a Binary Search Tree? ",l.is_bst)
```

## OUTPUT

<img width="916" height="286" alt="image" src="https://github.com/user-attachments/assets/778869dd-6174-4d0c-9950-59af6eaebcf7" />

## RESULT

Thus, the python code is written and executed successfully.
