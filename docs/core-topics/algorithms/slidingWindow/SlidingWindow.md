Sliding window is a variant of two pointers problems. Keep track of the overall result of window, when we slide the window insert/remove an item.

```python

def subarray_sum_fixed(nums: List[int], k: int) -> int:

    window_sum = 0

    for i in range(k):

        window_sum += nums[i]

    largest = window_sum

    for right in range(k, len(nums)):

        left = right - k

        window_sum -= nums[left]

        window_sum += nums[right]

        largest = max(largest, window_sum)

    return largest

```

Dynamically done sliding window

```python

def subarray_sum_shortest(nums: List[int], target: int) -> int:

    window_sum = 0
    length = len(nums)
    left = 0

    for right in range(len(nums)):
        window_sum += nums[right]
        while window_sum >= target:
            length = min(length, right - left + 1)
            window_sum -= nums[left]
            left += 1
    return length
```
