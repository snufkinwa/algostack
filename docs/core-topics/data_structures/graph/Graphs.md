# Graphs 🌌🪐✨

Imagine you’re an astronaut traveling to distant planets connected by mysterious wormholes! In computer science, **graphs** are like space maps that help us understand how planets and other things connect.

<p align="center">
<img src="https://media1.tenor.com/m/lhhcz6ynjx8AAAAd/interstellar-wormhole.gif">
</p>

### What’s a Graph?

A **graph** is a special map with two main parts:

- **Nodes (or vertices)**: These are the planets or destinations you visit.
- **Edges**: These are the paths or "wormholes" that let you travel between planets.

So, a graph is simply a collection of planets (nodes) connected by paths (edges).

---

#### Example: Galactic Tree Map

Here’s a simple galactic map in a tree structure, showing how nodes and edges might appear in space.

```
       Galactic Map
     -----------------
        Galaxy Core      <-- root
           |
           |
         Planet A       <-- first exploration
        /         \
   Nebula B       Planet C
    |
    |
 Asteroid Belt D

```

---

#### Why Graphs are Cool (Strengths and Weaknesses)

- **Great for Connections**: Graphs help us understand links between things, like how planets connect, or how friends connect on social networks.
- **Scaling Challenges**: When there are many planets (nodes), it takes longer to map all the paths. So big graphs can be hard to explore!

#### Space Map Types (Graph Types)

1. **Directed and Undirected**:

   - **Directed Graph**: Imagine a one-way wormhole; you can only go from Planet A to Planet B.
   - **Undirected Graph**: A two-way wormhole lets you travel back and forth.

2. **Weighted and Unweighted**:

   - **Weighted Graph**: Wormholes with numbers show travel time or difficulty. A high number means it’s a long or tough journey!
   - **Unweighted Graph**: All wormholes are simple paths without any special numbers.

3. **Cyclic and Acyclic**:

   - **Cyclic Graph**: If you can loop back to where you started, it’s like a roundabout in space.
   - **Acyclic Graph**: No loops, just paths to explore with no way to end up back where you began.

4. **Coloring**:
   - **Legal Coloring**: This means no two planets connected by a wormhole have the same color.

<p align="center">
<img src="https://media0.giphy.com/media/v1.Y2lkPTc5MGI3NjExbmx1NThpOTN4c25uOGlzOXV6a25temd5NHNmemp2bzBpd3pmaTM3dCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9cw/9iSlGflR0l9987MiFs/giphy.webp">
</p>

### How We Draw Graphs (Different Ways to Show Connections)

When we draw our space maps, we have different ways of showing how planets connect by wormholes. Here’s how:

1. **Edge List**: Imagine you have a list that says, "Planet A goes to Planet B" and "Planet B goes to Planet C." This list only shows which planets connect:

   ```python
   graph = [[Planet A, Planet B], [Planet B, Planet C]]
   ```

2. **Adjacency List**: Each planet lists its neighbors. So, if Planet B connects to Planet A and Planet C:

   ```python
   graph = {
       "Planet A": ["Planet B"],
       "Planet B": ["Planet A", "Planet C"],
       "Planet C": ["Planet B"]
   }
   ```

3. **Adjacency Matrix**: A map showing “0” for no wormhole and “1” for a wormhole. For three planets, it might look like:
   ```python
   graph = {
       [0, 1, 0],
       [1, 0, 1],
       [0, 1, 0]
   }
   ```

### The Galatic Maze: Thorne’s Escape Adventure 🐸

Meet Thorne, our bold space-hopping frog, navigating through the maze of stars and planets. Some planets are safe to land on, while others are dangerous asteroid fields that could end Thorne’s journey. A few rare star gates offer a path to escape the maze, while massive gas giants exert gravitational pulls that whisk Thorne’s ship to far-off planets.

Thorne moves randomly between planets, with each move equally likely to go in any safe direction. Your task is to calculate the probability that Thorne escapes the maze through a star gate rather than falling into a black hole or getting stuck.

<p align="center">
<img src="https://img.pikbest.com/origin/10/41/18/375pIkbEsTGmj.jpg!w700wp">
</p>

---

Galatic Maze Details

- Planets (nodes): Each cell in the maze.
- Wormholes (edges): Connect pairs of planets that aren’t otherwise adjacent.
- Goal: Calculate the probability of Thorne escaping through a star gate.

This version provides an adventure-focused theme around the [Frog in Maze](https://www.hackerrank.com/challenges/frog-in-maze/problem) problem while aligning with graph traversal concepts like nodes, edges, and probabilistic outcomes.

```
1. Set Up the Maze
   - Read input for maze dimensions (n x m) and number of gas giants.
   - Initialize a 2D list (maze) to store each cell's content:
       - Record obstacles, asteroid fields, star gates, empty cells, and Thorne’s start position.
   - Track positions of gas giant entries for linking in step 3.

2. Build Thorne’s Galaxy Map
   - Initialize an empty graph dictionary to represent the galaxy map.
   - For each free cell (planet) in the maze:
       - Add it as a node in the graph.
       - For each of its neighboring cells (up, down, left, right):
           - If it’s a free cell, link the current planet to this neighbor.

3. Add Gas Giant Pulls
   - For each gas giant pair, create a bidirectional connection:
       - Update the graph to link both entry cells directly to each other.

4. Calculate Thorne’s Odds of Escape
   - Use BFS starting from Thorne’s starting cell:
       - Initialize a queue with the start position and probability of 1.
       - For each cell Thorne visits, check if it's a star gate, asteroid field, or has no free neighbors:
           - Track probabilities for reaching a star gate, hitting an asteroid field, or getting “stuck.”
       - Otherwise, for each free neighboring cell:
           - Divide the probability equally among neighbors and add each to the queue.

5. Compute Escape Chances
   - For each cell Thorne visits during BFS:
       - If he reaches a star gate, add its probability to the escape count.
       - If he reaches an asteroid field, add its probability to the lost count.
       - If no unvisited neighbors are available, add this probability to the “stuck” count.

6. Show the Results
   - Calculate the final escape probability:
       - Print the probability of Thorne escaping via a star gate.
```
