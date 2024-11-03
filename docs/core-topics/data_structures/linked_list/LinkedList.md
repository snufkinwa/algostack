# Linked List

## 🚂 All Aboard! Facts & Figures

| Operation                     | Worst Case |
| ----------------------------- | ---------- |
| **Space**                     | O(n)       |
| **Add a Passenger at Front**  | O(1)       |
| **Add a Passenger at Back**   | O(1)       |
| **Find a Passenger**          | O(n)       |
| **Add a Station Mid-Journey** | O(n)       |
| **Remove a Station**          | O(n)       |

<p align="center">
<img src="https://media1.tenor.com/m/W8fALvrrkAAAAAAd/kh%C3%B3c.gif">
</p>

Like a train winding through the spirit world, this journey is about connecting one magical station to the next, creating an adventure full of mysteries.

### 🌌 Through the Spirit World: Stops on the Enchanted Line

You’re traveling on the mystical train from _Spirited Away_. Each station along the way welcomes passengers like Chihiro, No-Face, and other spirits. Bound by invisible forces, the train glides from one station to the next. The first stop, or the **head** station, begins the journey, while the last station, or the **tail**, marks the end.

Adding a station at the start or finish is as simple as casting a spell. Adding one mid-journey? Just unlink the line, insert the new stop, and reconnect! Unlike an array, this train isn’t confined to rigid tracks; it moves fluidly, yet each station is seamlessly linked.

### 🎒 A Journey for Little Spirits: The Spirit Stations

At each whimsical stop, friends like Chihiro, No-Face, and other spirits gather to board. Every station is connected to the next, keeping everyone together as they travel across the spirit realm. The **head** station starts the adventure, and the **tail** station concludes it. Need to add new stops? Place them at the beginning, end, or even in the middle—just link them up, and let the journey continue!

### 🌠 The Spirit Line’s Magical Powers: What Makes This Journey Special

- **Quick Additions at the Ends**: Need to add a station at the start or finish? Just link it up—it’s as fast as a blink (O(1) time).
- **Infinite Flexibility**: No need to set the number of stations ahead of time; keep adding stops as long as there’s space in the spirit world.

### 💨 Slower Moments on the Spirit Line

- **Finding Passengers**: To locate a specific spirit, you must pay attention at each station as they eagerly await their stop. This takes O(n) time, as you pass through each point on the mystical line.

<p align="center">
<img src="https://media1.tenor.com/m/ymjJcoSXkxIAAAAd/spirited-away-spirited.gif">
</p>

### 🛠️ Building the Spirit Line

Python doesn’t come with a built-in spirit line (linked list), but it’s easy to create! Here’s how to craft the enchanted stations from _Spirited Away_:

```python
class Station:
    def __init__(self, passenger):
        self.passenger = passenger
        self.next = None

# Adding passengers to the spirit line
station1 = Station("Chihiro")
station2 = Station("No-Face")
station3 = Station("Spirit")

# Connecting the stations
station1.next = station2
station2.next = station3
```

### 🔄 The Two-Way Spirit Line: A Mystical Round-Trip

On the standard spirit line, each station only knows the next stop. But with a **two-way spirit line**, each station knows the one before and after, allowing the journey to flow forward to new stops or backward to revisit memories.

<p align="center">
<img src="https://media1.tenor.com/m/ES2jIoApWwsAAAAd/spirited-away.gif">
</p>

### 🚃 Scattered Stations: A Different Kind of Journey

In most computers, reading memory in a straight line is fast—like a train with all stations perfectly aligned. But on the spirit line, stations can be scattered across the realm, so it takes a bit longer to move from one stop to the next, even though it’s technically still O(n) time in theory.
