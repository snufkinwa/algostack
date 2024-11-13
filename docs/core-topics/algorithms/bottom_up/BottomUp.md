# Bottom-Up Algorithms

<p align="center">
<img src="https://media1.tenor.com/m/csZyghLT3OMAAAAd/db-cooper-iron-man.gif">
</p>

_"Dude, you’re embarrassing me in front of the wizards."_

A **bottom-up algorithm** is like building Iron Man’s suit step-by-step, starting with the smallest pieces and working up to the final, complete suit. This is different from a **recursive algorithm**, which often starts at the top and works backwards. Bottom-up avoids the memory issues that recursion can cause.

Let’s build the suit and learn how bottom-up works!

#### Step-by-Step: Building Iron Man’s Suit from the Bottom-Up

1. **Core Frame (Base Case)**:  
   First, we need the core frame of Iron Man’s suit. This is the “base case,” or the foundation, on which all other parts will attach. Without this core, the suit has nothing to stand on!

2. **Arc Reactor (First Layer)**:  
   Next, we add the Arc Reactor, which powers the entire suit. This is like solving the first small part of a problem in a bottom-up algorithm. It provides the “energy” for everything that follows.

3. **Main Armor Plating (Intermediate Layers)**:  
   Now we attach the main armor piece by piece. Each piece of armor makes the suit stronger and represents an intermediate step in our solution, like adding up small pieces to get closer to the answer.

4. **Repulsors and Flight System (Advanced Layers)**:  
   Adding repulsors to the hands and feet lets Iron Man fly and defend himself. These layers represent more complex parts of the solution, like solving advanced parts of a problem that add big functionality.

5. **Helmet, HUD, and Targeting System (Final Layers)**:  
   Finally, the helmet, HUD, and targeting systems go on. These are the finishing touches, adding precision and control to the suit, just like final steps in a bottom-up algorithm bring everything together for the solution.

6. **Final Activation**:  
   The suit is fully assembled and ready for action! In a bottom-up algorithm, this is when all the small steps combine to create the final solution, which is powerful and complete.

#### Bottom-Up vs. Recursion

- **Bottom-Up** builds solutions one step at a time, just like putting on each piece of Iron Man’s suit from the ground up. It doesn’t use as much memory, so it’s safer and avoids problems.
- **Recursion** starts at the end and works backwards. But this can use a lot of memory, and if there are too many steps, it might break—kind of like when Iron Man’s suit overheats (stack overflow) from using too much power all at once!

<p align="center">
<img src="https://media1.tenor.com/m/cYvFDHgLqDwAAAAd/iron-man-iron-man2.gif">
</p>

#### Example: Multiplying Numbers from 1 to n

We need Iron Man to multiply numbers from 1 up to a big number, like putting together his suit step by step.

A **recursive** way would start from the end and work backwards, adding each part of the suit as it goes. But this can take up a lot of space in memory:

```python
def iron_man_suit(n):
    # Starts from the top and works backwards
    return n * iron_man_suit(n - 1) if n > 1 else 1
```

The **bottom-up** way starts from the beginning and builds up, just like putting each part on Iron Man’s suit, piece by piece:

```python
def iron_man_suit(n):
    suit_strength = 1
    for part in range(1, n + 1):
        suit_strength *= part  # Each part makes the suit stronger
    return suit_strength
```

In the bottom-up way, Iron Man’s suit gets stronger with each part added, like building from the ground up!
