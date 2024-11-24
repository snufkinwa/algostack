Template for dfs

Use DFS to use less memory for wide graphs/ Find nodes far away from root like looking in a maze.

```python
function dfs(node, state):

    if node is null:
        ...
        return


    left = dfs(node.left, state)
    right = dfs(node.right, state)
        ...
    return ...
```

Given a binary tree, find its max-depth

```python
class Node:

    def __init__(self, val, left=None, right=None):

        self.val = val

        self.left = left

        self.right = right


def tree_max_depth(root: Node) -> int:

    def dfs(root):

        # null node adds no depth

        if not root:

            return 0

        # num nodes in longest path of current subtree = max num nodes of its two subtrees + 1 current node

        return max(dfs(root.left), dfs(root.right)) + 1


    return dfs(root) - 1 if root else 0

```

---

```python

```
