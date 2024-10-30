# Lists (Dynamic Arrays) 🌙✨

<p align="center">
<img src= "https://media1.tenor.com/m/AN9GH-Zv1vYAAAAC/sailor-moon-transform.gif">
</p>

In programming, a **list** (or dynamic array) is like Sailor Moon’s collection of **transformation brooches**: flexible and expandable as new brooches are obtained. Each brooch in the collection has a specific spot, easily accessible by its position, and new brooches are added seamlessly as the collection grows.

### **Characteristics**

- **Space-Saving Magic:** Only uses the space it needs and only grows bigger when it's full.
- **Grows with New Brooches:** Expands on its own whenever we add more brooches (or **elements**).
- **Quick Access:** All brooches are stored side-by-side, so the computer can find them super fast!

### **Performance**

| Operation         | Average Case | Worst Case | Description                                                       |
| ----------------- | ------------ | ---------- | ----------------------------------------------------------------- |
| **Space**         | \(O(n)\)     | \(O(n)\)   | Adjusts memory to hold elements, no waste.                        |
| **Lookup**        | \(O(1)\)     | \(O(1)\)   | Accessing a brooch by position is very fast.                      |
| **Append**        | \(O(1)\)     | \(O(n)\)   | Quick on average; occasionally resizes to fit more.               |
| **Insert/Delete** | \(O(n)\)     | \(O(n)\)   | Rearranging brooches takes time, especially in large collections. |

---

### How Dynamic Arrays Grow 🌱

**Magic Expanding Power!**

- **Size vs. Space:** The collection’s **size** is how many brooches are in it right now, and **space** is how many it can hold.
- **Double the Space:** When the collection is full, it magically doubles in space so we can fit more brooches! Doubling means moving each brooch to a bigger place, which takes some extra time.

<p align="center">
<img src= "https://media.tenor.com/9gK4CTNScYYAAAAi/stars-nite.gif" width="250">
</p>

**Adding New Brooches**

- Adding a brooch is usually fast because we already have space.
- But if we run out of space, adding a new one takes a bit longer since we need to move everything to the bigger place.

---

### Operations on the Brooch Collection

1. **Start with an Empty Collection**

   ```python
   brooch_collection = []
   ```

2. **Adding Brooches**

   - **Append at End:**  
     Adds a new brooch to the end. Average \(O(1)\).
     ```python
     brooch_collection.append("Prism Compact")
     ```
   - **Insert at Specific Spot:**  
     Inserts at a chosen position. Costly if it shifts others, \(O(n)\).
     ```python
     brooch_collection.insert(1, "Heart Moon Brooch")
     ```

3. **Accessing Brooches**

   - **By Position:**  
     Fast access via position. \(O(1)\).
     ```python
     brooch_collection[2]  # Get the 3rd brooch
     ```
   - **Negative Indexing:**  
     Retrieve from the end with a negative number.
     ```python
     brooch_collection[-1]  # Last brooch in the collection
     ```

4. **Updating Brooches**

   - Change a brooch at a specific position. Still \(O(1)\).

   ```python
   brooch_collection[0] = "Crisis Compact"
   ```

5. **Removing Brooches**

   - **Remove by Name:**  
     Removes the first matching brooch. Could be \(O(n)\) if at the end.
     ```python
     brooch_collection.remove("Prism Compact")
     ```
   - **Remove by Position (Pop):**  
     Removes by position and returns it. \(O(n)\) if not the last.
     ```python
     brooch_collection.pop(2)
     ```

6. **Advanced Brooch Operations**

   - **Slicing the Collection:**  
     Extracts a subset. Creates a new list; slicing takes \(O(k)\), where \(k\) is slice length.
     ```python
     brooch_collection[1:3]  # Brooches at positions 1 and 2
     ```
   - **Extend with New Brooches:**  
     Adds a list of new brooches to the end.
     ```python
     brooch_collection.extend(["Cosmic Compact", "Eternal Moon Compact"])
     ```
   - **List Comprehension:**  
     Condensed way to filter or modify brooches.
     ```python
     brooch_collection = [brooch for brooch in brooch_collection if "Moon" in brooch]
     ```

7. **Sorting and Reversing**

   - **Sort:** Orders brooches alphabetically or by another rule. Efficient but rearranges everything, \(O(n \log n)\).
     ```python
     brooch_collection.sort()
     ```
   - **Reverse:** Flips the order of brooches in place. \(O(n)\).
     ```python
     brooch_collection.reverse()
     ```

8. **Looping and Checking**
   - **Loop Through Each Brooch:**  
     Runs code for each item.
     ```python
     for brooch in brooch_collection:
         print(brooch)
     ```
   - **Check for Specific Brooch:**
     ```python
     if "Prism Compact" in brooch_collection:
         print("Brooch found!")
     ```

[Check out the practice section!](./practice/Practice.md)

<p align="center">
<img src= "https://media1.tenor.com/m/IqT94xBTBFwAAAAC/sailormoon-in-the-name-of-the-moon.gif">
</p>
