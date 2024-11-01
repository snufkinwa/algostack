# Dictionaries (Hash Tables)

### **What's a Hash Table?**

Think of the Matrix as a **big room full of secret doors**! Each door has a **special number** on it, called an **index**. You need to find the right door to get the **data pill** hidden behind it! But don’t worry; we’ve got a trick to help you find it quickly.

#### **How Do We Use It?**

We can hide each data pill behind a door, and each pill has a **key code** so we can remember where to find it. The **Hash Function** is the trick that **turns a key code into a door number**.

- **Hashing**: Think of hashing like **Agent Smith** making lots of copies of himself, but each copy gets its own door in the Matrix. The hashing trick makes sure each key has a door it points to. Sometimes two keys want the same door—that’s called a **glitch**!

#### Agent Protocols: Mission Speed Guide

| **Mission**  | **Average Speed** | **Slowest Speed** |
| ------------ | ----------------- | ----------------- |
| Space        | O(n)              | O(n)              |
| Insert Data  | O(1)              | O(n)              |
| Look Up Data | O(1)              | O(n)              |
| Delete Data  | O(1)              | O(n)              |

<p align="center">
<img src="https://media1.tenor.com/m/lXXuvTUGsnwAAAAd/wtf-haxxor-matrix.gif">
</p>

---

#### **What's So Cool About Hash Tables?**

- **Super-Fast Lookups**: Like **Agent Neo** zooming to any spot in the Matrix! Usually takes **O(1)** time.
- **Flexible Keys**: Anything can be a key—like words or numbers! Just make sure they’re hashable, meaning they have a Matrix code that turns them into a number.

#### **But Watch Out for Glitches!**

- **Glitch (Collision)**: Sometimes, two keys try to go to the same door. We fix this with a **linked list**—a special chain that lets us keep both keys safe in the same spot.
- **No Order**: We can’t always go from the smallest to the biggest in a hash table. It’s like all doors have different codes, so if we want to find the **first or last** thing, we have to check all doors.
- **One-Way Street**: You can look up a value by its key quickly, but finding the key from a value means checking every spot.

---

#### Matrix Code Nodes

In the Matrix, we call hash tables **dictionaries**. Look at this cool data:

```python
# Matrix Pills and Their Effects (like a Dictionary!)
matrix_pills = {
    'red_pill': 'truth',
    'blue_pill': 'illusion',
    'purple_pill': 'mixed reality',
}
```

This dictionary maps each pill type to its effect in the Matrix! It’s built on top of an **array** for efficient access.

<p align="center">
<img src="https://media1.tenor.com/m/PhnZUt2djmkAAAAd/matrix-elmo.gif">
</p>

---

#### **Decoding Keys: The Hash Code Hack**

1. Take each letter in the key and **find its letter number** (ASCII value). Then, add them up to get a "big number."

   - Example: For the key "Matrix," we get:
     - **M** = 77
     - **a** = 97
     - **t** = 116
     - **r** = 114
     - **i** = 105
     - **x** = 120
   - Adding these gives us **629**.

2. Use the **modulus trick** to convert this big number into a smaller number that fits our Matrix array.
   - If our array has 30 slots, we calculate:
     \[
     629 \% 30 = 29
     \]
   - So, **29** is the index in our Matrix array where we can store or find the data associated with "Matrix"!

#### **Handling Glitches (Collisions)**

Sometimes keys want the same spot—just like glitches in the Matrix! Here’s how we handle it:

- **Glitch Link: The Chain of Nodes**: At each door, we have a **linked list** holding all the keys that want the same spot. **Agent Neo** uses this chain to follow each link and find the right data node, keeping all the information secure.

---

#### Unlocking the Matrix: Sets of Unique Data Nodes

A **set** is like a hash table but without any values. It’s just **keys**!

1. **Add Keys**: We can store unique Matrix items with no repeats.
   ```python
   matrix_effects = set()
   matrix_effects.add('truth')
   ```

#### Dictionary Node Control (Reality Code Reference)

1. **Add New Data**:
   ```python
   matrix_pills['purple_pill'] = 'mixed reality'
   ```
2. **Look Up Data**:
   ```python
   effect = matrix_pills['red_pill']
   ```
3. **Remove Data**:
   ```python
   matrix_pills.pop('blue_pill')
   ```
