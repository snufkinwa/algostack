# Queues

<p align="center">
<img src="https://media4.giphy.com/media/v1.Y2lkPTc5MGI3NjExYmZranBmNWpjcGR5azR1dzM1eHQxN3E0aGdtM3NjbXhibnpxYzhkYyZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/mEYkuPOOyHcYn5xgDP/giphy.webp">
</p>

### **"By Decree of Lord Farquaad, Line Up!"** 👑

In the land of Duloc, all fairytale creatures must be registered! Lord Farquaad demands a line where each creature waits their turn. The first creature to join the line is the first to be registered and removed from the line—no exceptions! This is what we call a **queue**: first in, first out, just like Lord Farquaad’s registration line!

### **Quick Look at the Registration Queue** 📜

- **Queue Order:** The first creature in line gets registered first **(FIFO)**.
- **Queue Strengths:**
  - **Fast operations:** It’s quick for creatures to join the line or get registered and leave (O(1)).
  - **Space used:** Takes up space for all creatures in line (O(n)).

### **Queue Applications: Duloc Style** 🏰

Queues like this are helpful in many places, just like Lord Farquaad’s system:

- **Search the Land:** Just as guards search the kingdom, **breadth-first search** uses a queue to check each area in order.
- **Print Orders:** Like Duloc’s printer, jobs get printed in the order they’re requested.
- **Page Requests in Duloc:** Web servers use queues so everyone gets a turn, just like fairytale creatures in line.
- **Orderly Processes:** The CPU scheduler also uses a queue so each process (or creature) gets its turn.

### **Queue Mechanics: Joining and Leaving the Line** 🐷

In Duloc, creatures line up in a queue. Let’s see how it works with a **linked list**:

- **Enqueue (Get in Line):** A creature joins the end of the line, no cutting!
- **Dequeue (Step Up!):** The creature at the front gets registered and leaves the line.

Queues could also be implemented with arrays, but just like in Duloc, if you keep shifting creatures up, it can get pretty messy. Linked lists keep the line moving smoothly without the extra work!

---

So, every time a creature gets registered and leaves, another takes their place at the end of the line. This way, Duloc’s fairytale registration follows the perfect order that Lord Farquaad demands before we drop them all in the SWAMP!

<p align="center">
<img src="https://media0.giphy.com/media/v1.Y2lkPTc5MGI3NjExY3ZsOHppOWlwMjEzd2k0aWxzaG45bjg4cjVienhhbjcwOTYyNzZqaSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/T3nwQFJq5lxFii50fR/giphy.webp">
</p>

### Register the Fairytale Creatures (Code Example)

```python
from collections import deque

# Initialize the queue
registration_queue = deque()

# Get in Line! (Enqueue)
registration_queue.append("Pinocchio")
registration_queue.append("Three Little Pigs")
registration_queue.append("Gingerbread Man")
registration_queue.append("Big Bad Wolf")

print("Queue after enqueuing:", list(registration_queue))

# Peek at who's first in line
print("First in line:", registration_queue[0])

# Step Up! (dequeue)
while registration_queue:
    creature = registration_queue.popleft()  # First one in line gets registered
    print(f"{creature} has been registered and removed from the queue.")

print("Queue after dequeuing all:", list(registration_queue))

```
