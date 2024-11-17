Best-case : O( n log (n))

Worst-case: O(n<sup>2</sup>)

Stable.

```python
from typing import List

def sort_list(unsorted_list: List[int]) -> List[int]:

    n = len(unsorted_list)

    # Base case: A list of size 1 or 0 is already sorted
    if n <= 1:
        return unsorted_list

    # Split the list into left and right halves
    midpoint = n // 2
    left_list = sort_list(unsorted_list[:midpoint])
    right_list = sort_list(unsorted_list[midpoint:])
    result_list = []

    left_pointer, right_pointer = 0, 0

    # Merge the sorted left and right lists with two pointers
    while left_pointer < len(left_list) or right_pointer < len(right_list):
        if left_pointer == len(left_list):
            # If left list is empty, append element from right
            result_list.append(right_list[right_pointer])
            right_pointer += 1

        elif right_pointer == len(right_list):
            # If right list is empty, append element from left
            result_list.append(left_list[left_pointer])
            left_pointer += 1

        elif left_list[left_pointer] <= right_list[right_pointer]:
            # Append smaller element from left
            result_list.append(left_list[left_pointer])
            left_pointer += 1

        else:
            # Append smaller element from right
            result_list.append(right_list[right_pointer])
            right_pointer += 1

    return result_list
```
