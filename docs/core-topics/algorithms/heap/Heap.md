Python comes with built-n `heapq`

Heaps are special tree based data structures. Referring to a binary heap that is like a binary tree structure. However the treee isn't always binary, as long a node follow 2 heap properties it is a valid heap.

Two types of heaps min heap and max heap. The heap is an odd data structure - it's required to be a complete tree but unlike binary search tree, it's not sorted across a level.

Best case O(log(N))

```python
import heapq
>>> h = []
>>> heapq.heappush(h, (5, 'write code'))
>>> heapq.heappush(h, (7, 'release product'))
>>> heapq.heappush(h, (1, 'write spec'))
>>> heapq.heappush(h, (3, 'create tests'))
>>> heapq.heappop(h)
(1, 'write spec')
>>> h[0]
>>> (3, 'create tests')

```
