# Big O Notation

<img src="./BigO.png" width="400">

Big O notation is like a special way of talking about **how long an algorithm takes to run** as we add more and more things for it to handle.

It’s kind of like math, but we don’t worry about every tiny detail; instead, we look at how the steps grow as we add more to do.

Let’s break down what this means:

- **How quickly time grows**: This is called "complexity." Imagine it takes you 5 seconds to clean up 10 toys, but what if you had 100 toys? Or 1,000? The more toys you have, the longer it takes! Complexity tells us how much longer as we add more.

- **Same kind of task**: If you have two games to play, like one where you’re counting toys and one where you’re stacking blocks, you can’t compare how fast they are because they’re too different. Big O works only when comparing similar jobs — so we can see what’s faster when doing the same kind of work.

- **More and more pieces**: Imagine we have a huge pile of Legos and we want to build a tall tower. If we have just a few Legos, it’s quick. But if we have the entire bucket, it takes a lot longer! Big O shows us what happens as the amount of work gets really big.

<span style="background-color: #FF5C00">_O_(1)</span> or "constant time" means that no matter how many toys we have — 1, 10, or even 100 — it always takes the same amount of time to complete the task. So, whether there's just one toy or a whole pile, it only needs one step to finish.

Imagine turning on a light switch: whether there’s one person in the room or 100, it still only takes one quick flip!

<p align = "center">
<img src = "https://media1.tenor.com/m/pb775b3jCzsAAAAC/starvstheforcesofevil-starbutterfly.gif"> </p>

```python
def pick_up_toy(toys):
    # Always pick up the first toy in the pile
    print(toys[0])
    # No matter how many toys there are,
    # we're only taking one step to complete!
```

<span style="background-color: #FF5C00">_O_(_n_)</span> or "linear time" where _n_ is the number of toys in the list. If we have 10 toys, we'll do 10 steps; if we have 100 toys, we'll do 100 steps. So the time grows in a straigt line as we add more toys.

<p align = "center">
<img src = "https://www.educative.io/api/page/5870871921033216/image/download/6490343026458624" width = "400"></p>

```python
def pick_up_each_toy(toys):
    # Go through each toy one by one
    for toy in toys:
        print(toy)
    # We do one step per toy, so the time grows with the number of toys (n)!
```

Now we're pairing up toys to see every possible combination. For each toy, we want to see how it pairs with every other toy in the pile.

```python
def print_all_possible_ordered_pairs(toys):
    for first_toy in toys:
        for second_toy in toys:
            print(first_toy, second_toy)
```

Here, we're nesting loops- one loop goes through each toy and inside that, another loop goes through each toy again.

If we have **n** toys, the first loop runs **n** times for each of those, the second loop also runs **n** times. This means we're making **n** \* **n** or **n²** pairs in total!

So, this function is <span style="background-color: #FF5C00">_O_(n²)</span> or "quadratic time"- the time it takes grows like a big square as we add more toys.

- With 10 toys 🦖🪀, we print 100 pairs.
- With 1,000 toys 🧸🧩, we print 1,000,000 pairs!

It grows quickly because each new toy creates a full set of new combinations with all the toys that came before it.

## Concepts

### Dropping Constants: Ignore Extra Plays

When we’re counting steps, we don’t worry about extra plays. Even if we do something twice, we still just count it once!

If you look at each toy twice, we still call it <span style="background-color: #FF5C00">_O_(_n_)</span>, or "one look per toy."

```python
 def look_at_toys_twice(toys):
     for toy in toys:
         print(toy)  # First look
     for toy in toys:
         print(toy)  # Second look
```

_Even though we look twice, we just count it as once!_

### Dropping Less Important Steps: Focus on Big Actions

When we’re counting steps, we only care about the big steps that take a lot of time as we add more toys. The small, quick steps don’t matter as much, so we ignore them.

Imagine you’re looking at each toy in a pile, and then you make every possible pair of toys. Looking at each toy is quick, but making all the pairs takes a lot longer. So, we only focus on the time it takes to make pairs.

```python
def print_all_numbers_then_all_pair_sums(toys):
    print("These are the toys:")
    for toy in toys:
        print(toy)  # Quick step, O(n)

    print("And these are all possible pairs:")
    for toy1 in toys:
        for toy2 in toys:
            print(toy1, toy2)  # This part takes longer, O(n²)
```

_Making pairs takes much longer than just looking, so we only count the big step!_

### Best, Worst, and Average Cases: Different Ways to Count

Sometimes finding a toy is easy, and sometimes it’s hard. Big O usually talks about the hardest or "worst case" way.

If you’re looking for your favorite toy, it might be right on top (<span style="background-color: #FF5C00">_O_(1)</span>), or it might be hidden all the way at the bottom (<span style="background-color: #FF5C00">_O_(_n_)</span> ).

```python
    def find_favorite(toys, favorite):
        for toy in toys:
            if toy == favorite:
                return True
        return False
```

_If it’s on top, we find it fast! If it’s last, it takes a while._

### Space Complexity: How Much Room We Need for Our Toys

Sometimes, when we play with toys, we need to think about how many boxes we need to hold everything. This is called "space complexity" — how much space we need as we add more toys.

- <span style="background-color: #FF5C00">_O_(1)</span> means we only need one box, no matter how many toys we have! We don’t need more space, even if we add more toys.

```python
    def single_box(toys):
        box = "one box for sorting"
        print(box)
```

_With <span style="background-color: #FF5C00">O(1)</span>, you don’t need more room if you get more toys!_

- <span style="background-color: #FF5C00">_O_(n)</span> we need one box for each toy. If you have 10 toys, you need 10 boxes. If you get 100 toys, you need 100 boxes. Here, space grows with the number of toys.

### Why Space Complexity Is Useful

Space complexity helps us decide how much room we need to finish a task. If we need a lot of space, we might run out of room! So we have to think carefully: do we want to save time, or do we want to save space?

For example, if we want to find the biggest toy, we only need one space to keep track of the "biggest toy so far." We don’t need space for every toy:

```python
def get_largest_toy(toys):
    biggest_toy = "no toy yet"  # We only need one spot
    for toy in toys:
        if toy > biggest_toy:
            biggest_toy = toy
    return biggest_toy
```

_This is <span style="background-color: #FF5C00">O(1)</span> space because we only need one spot, no matter how many toys we have!_

### Knowing When to Optimize: Don’t Make It Too Complicated!

Sometimes, making things go faster or use less room is nice, but it can make things confusing. It’s okay if it’s not perfect if it’s still easy to use.

If sorting toys takes a long time, try making fewer steps, but don’t make it too hard to understand.

```python
    def simple_sort(toys):
        sorted_toys = sorted(toys)  # Sorting made easy
        return sorted_toys
```

_Sometimes it’s more important to keep it simple!_

## How Constraints Help Us Solve Coding Problems on HackerRank

When we solve coding problems on HackerRank, we get special rules called **constraints**. These rules help us figure out the best way to solve the problem:

1. **How Big the Problem Is:** If there’s only a small amount of work, we can solve it any way we want! But if there’s a huge amount, we need a faster way, or it’ll take forever.

2. **How Hard the Problem Is:** Some parts are easy, while others are tricky. The rules tell us how hard each part is so we can plan better.

3. **Choosing the Best Approach:** By checking the rules, we can find the fastest and easiest way to finish without getting stuck.

Before starting, look at the rules! They help us solve coding problems quickly and smartly on HackerRank.

### Example of the **constraints** in [_Problem Solving_](https://www.hackerrank.com/challenges/problem-solving/problem)

| **Constraint**  | **Meaning in the Problem Context**                                                                                                                                                                   |
| --------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `1 ≤ T ≤ 100`   | We can have up to 100 test cases, meaning we may need to solve this problem up to 100 different times, each with its own set of `N`, `K`, and `vi` values.                                           |
| `1 ≤ N ≤ 300`   | `N` is the number of problems to solve in each test case. With up to 300 problems, we need an efficient solution that can handle this many problems without slowing down.                            |
| `1 ≤ vi ≤ 1000` | `vi` is the difficulty rating for each problem, ranging from 1 to 1000. Problems with similar `vi` values are alike, so we’ll need to space out problems with close ratings.                         |
| `1 ≤ K ≤ 1000`  | `K` is the minimum difference in `vi` rating required between consecutive problems solved on the same day. With `K` as high as 1000, our solution must manage large jumps in difficulty effectively. |

**Constraints** help ensure our solution works efficiently across all test cases, handling up to 300 problems per test case and working with values as high as 1000 without slowing down!
