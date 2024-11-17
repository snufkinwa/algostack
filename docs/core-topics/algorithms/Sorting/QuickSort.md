TODO

Best-Case: 0(n log (n))

Worst-Case: O(n<sup>2</sup>)

Using the midpoint as a pivot can help avoid worst-case in QuickSort but does not guarantee stability or correct sorting of duplicates unless explicitly handled.

TEMPLATE:

```python
from typing import List

def sortArrayInteral(nums: List[int], start: int, end: int) -> None:
    #Base case
    if end - start <= 1:
        return

    #Midpoint as pivot and move it to the end
    mid_idx = start + (end - start) // 2
    nums[mid_idx], nums[end - 1] = nums[end-1], nums[mid_idx]
    pivot = nums[end - 1]

    left, right = start, end - 1

    # Partitioning
    while left < right:
        while nums[left] < pivot and left < right:
            left += 1

        while nums[right] >= pivot and left < right:
            right -= 1
        nums[left], nums[right] = nums[right], nums[left]

    # Place pivot in its correct position
    nums[left], nums[end - 1] = nums[end - 1], nums[left]

    # Recursively sort left and right partitions
    sortArrayInterval(nums, start, left)
    sortArrayInterval(nums, left + 1, end)

class Solution:
    def sortArray(self, nums: List[int]) -> List[int]:
        # Use function to perform the Quick Sort
        sortArrayInterval(nums, 0, len(nums))
        return nums
```
