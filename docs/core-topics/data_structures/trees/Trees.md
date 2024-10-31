# Trees

<p align="center">
<img src="https://media1.giphy.com/media/v1.Y2lkPTc5MGI3NjExNnA1cHY3N3lpbmFzYnpwN2N0eDQ0bDVoMGx0dGVzejN2NGcwbmd3MyZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/QIlBpCE1oWsgxJ23oW/giphy.webp">
</p>

Imagine **Dunder Mifflin** is like a giant computer folder, with everyone’s desks arranged in a **perfect binary tree**. But what’s a binary tree? Well, it’s just a way of saying each desk (or “node”) has up to **two children**—think of each desk as branching off to two more desks below it, like little office families.

```plaintext
                           [Michael's Desk]
                          /                \
              [Jim's Desk]                  [Dwight's Desk]
             /               \              /              \
     [Pam's Desk]       [Ryan's Desk]  [Angela's Desk]   [Kevin's Desk]
      /        \         /         \      /       \        /        \
  [File1]    [File2]  [File3]     [File4] [File5]   [File6]   [Chili Recipe]
```

### Key:

1. **[Michael’s Desk]** - The _root_ of the tree, like the big boss at the top.
2. **[Jim’s Desk]** and **[Dwight’s Desk]** - The first level of branches, each with their own “mini-boss” desks below.
3. **[Pam’s Desk]**, **[Ryan’s Desk]**, **[Angela’s Desk]**, and **[Kevin’s Desk]** - The second level of branches with “files” below them.
4. **[File1]** through **[Chili Recipe]** - The _leaf nodes_ (final files) at the last level.

### The Top Desk: Michael’s Root

At the very top of the tree sits **Michael**—the “root” of the office. His desk branches off into **two main desks** below: **Jim** and **Dwight**. They’re the second-in-command on this tree.

### Jim and Dwight’s Branches

Jim’s desk leads to **Pam’s** on the left (makes sense, she’s the receptionist!) and **Ryan** on the right (the intern). Dwight’s desk, on the other hand, connects to **Angela** and **Kevin**—our trusty accountants. Each desk can branch out, forming an upside-down family tree of sorts.

### Perfectly Full Levels

This is a _perfect_ binary tree—meaning there are no gaps! Every desk has its own little “branch,” filling each level completely. Every new level has double the desks of the one above. So Michael sits on top with 1 desk, Jim and Dwight together make 2 desks, then Pam, Ryan, Angela, and Kevin total 4, and so on. The office just doubles up each level!

<p align = "center">
<img src= "https://media0.giphy.com/media/v1.Y2lkPTc5MGI3NjExc2F6ZDU4MTBpcXRxMDdsNXh0OTVxZmY4NTJocnl5ZWRyMGkzbHQxNCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/R40iFCgNSpknrixgmv/giphy.webp">
</p>

### Chili Files on the Last Level

Every desk also has its own “file,” representing different tasks or, say, _recipes_. So, down on the **last level** of this tree, we might find **Kevin’s famous chili recipe file** sitting proudly as a leaf node. This is the final stop; no more desks or branches below, just pure, unadulterated chili.

### Fun Facts about Binary Trees

1. **Double the Desks**: Every level in a perfect binary tree has double the desks as the one above. So, if Michael’s alone at the top, Jim and Dwight are 2, Pam, Ryan, Angela, and Kevin total 4, and the next row would have 8.
2. **Half the Chili**: About half the desks (or files) are on the last level, like how half the office’s excitement goes into Kevin’s chili day.

<p align="center">
<img src="https://media3.giphy.com/media/v1.Y2lkPTc5MGI3NjExNm5pcm82eTV1ejF1czhob3h4ZGhxbHIwM3hidHd2NXA4Z2Q1MDd6NyZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/SZQBPO4NqHkh6wmdXk/giphy.webp" width="200">
</p>

### Calculating the Total Desks

If we know the height of the tree (the number of levels), we can figure out how many desks we have! For example, if there are **5 levels**, we can add up the desks like this: 1 (Michael) + 2 (Jim and Dwight) + 4 (Pam, Ryan, Angela, Kevin) + 8... and so on.

Or, even easier, we can use a math trick:

total desks = 2<sup>levels</sup> - 1

So, if we know the total desks (nodes), we can also work backward to find the height of the tree.

And that’s how the office works as a **binary tree**! Each desk has its place, everyone’s connected, and the chili recipe lives on the bottom level, ready to be spilled!

<p align="center">
<img src="https://media3.giphy.com/media/v1.Y2lkPTc5MGI3NjExYXRoZDBvbTFreG1iMGJtdjR0NXlwc3hzbnFibTR0d3FiY2VrMG8zYyZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/jYEBdVARBGPXa/giphy.webp">
</p>
