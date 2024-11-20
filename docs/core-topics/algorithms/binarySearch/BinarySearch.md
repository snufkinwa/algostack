Vanilla Binary Search

```python
from typing import List

def binary_search(arr: List[int], target: int) -> int:
    left, right = 0, len(arr) - 1

    while left <= right:
        mid = (left + right) // 2
        if arr[mid] == target:
            return mid
        if arr[mid] < target:
            left = mid + 1
        else:
            right = mid - 1
    return -1

```

```python
from typing import List

def find_boundary(arr: List[bool]) -> int:
    left, right= 0, len(arr) - 1
    boundary_idx  = -1

    while left <= right:
        mid = (left + right) // 2
        if arr[mid]:
            boundary_idx = mid
            right = mid - 1
        else:
            left = mid + 1
    return boundary_idx
```

```python
from typing import List

def find_boundary(arr: List[bool]) -> int:
    left, right= 0, len(arr) - 1
    boundary_idx  = -1

    while left <= right:
        mid = (left + right) // 2
        if arr[mid]:
            boundary_idx = mid
            right = mid - 1
        else:
            left = mid + 1
    return boundary_idx
```

```python
def searchRange(self, nums, target):

    left, right = 0, len(nums)-1

    first_pos, last_pos = -1, -1



    # find first pos

    while left <= right:

      mid = (left + right) // 2

      if nums[mid] == target:

          first_pos = mid

          right = mid - 1

      elif nums[mid] > target:

          right = mid - 1

      else:

          left = mid + 1



    #find last pos

    left, right = 0, len(nums)-1

    while left <= right:

      mid = (left + right) // 2

      if nums[mid] == target:

          last_pos = mid

          left = mid+1

      elif nums[mid] > target:

          right = mid - 1

      else:

          left = mid + 1

    return (first_pos, last_pos)
```

```python
class Solution:
    def search(self, nums: List[int], target: int) -> int:
      l, r = 0, len(nums) - 1
      while l <= r:
        m = (l + r) // 2

        q = nums[m]
        if q == target: return m
        if nums[l] <= q:
            if target > q or target < nums[l]:
                l = m + 1
            else:
                r = m - 1
        else:
            if target < q or target > nums[r]:
                r = m - 1
            else:
                l= m + 1

      return -1

```
