# Arrays 🍣

Picture an **array** like a sushi conveyor belt. Each plate (or **index**) has a fixed position, starting from 0, and you can grab any plate directly by its position. Easy access to all the tasty data!

<p align= "center">
<img src = "https://i.pinimg.com/originals/66/2b/f8/662bf8a76c65ad66b25a63ace4bc2315.gif">
</p>

**Characteristics**:

- **Fixed size**: We must decide how many plates (elements) the conveyor belt can hold upfront.
- **Index-based access**: You can reach any plate by its position on the belt.
- **Data type consistency**: Each plate on the belt should have the same kind of item (e.g., all strings, all integers, etc.).

**Performance**:

- **Space**: \(O(n)\), where \(n\) is the number of plates on the belt.
- **Lookup (by index)**: \(O(1)\), direct access to any plate by its position.
- **Append (if space available)**: \(O(1)\), if there’s room for more plates on the belt.
- **Insert/Delete**: \(O(n)\) in the worst case, since all plates might need to be shifted around.

### Example in Java

Here’s how you might set up your sushi plates in JavaScript:

```java
// Initializing a conveyor belt of sushi plates with a fixed size
String[] sushiPlates = new String[3];

// Adding elements to the array
sushiPlates[0] = "Salmon Nigiri";
sushiPlates[1] = "Fatty Tuna Sashimi";
sushiPlates[2] = "Eel Hand Roll";

```

<p align="center">
<img src = "https://media1.tenor.com/m/7VDdXsqIYFYAAAAC/code-syntax-error.gif" width ="300"></p><br>

**Always remember: stick to one language during a coding test!** It’s not the time to show off our knowledge of multiple languages.<br>

> ### 📝 Python-Specific Note on Arrays
>
> Python does not have traditional fixed-size arrays like some other languages. Instead, it offers **lists**, which act as dynamic arrays. For cases where a fixed-type array is required, Python provides the `array` module, which supports specific data types like integers (`'i'`), floats (`'f'`), and others.
>
> **Important**: The `array` module **does not support strings**. If you need a fixed-type array of strings, consider using the `NumPy` library, which allows you to create arrays with a specified data type, including strings.
>
> That said, **lists are generally preferred in Python** because they are more flexible and efficient. Fixed-size arrays are more common in other languages.

### Python Example Using the `array` Module

If a fixed-type array is needed in Python, here’s how to create one using the `array` module:

```python
from array import array

# Creating a fixed-type array of integers
arr = array("i", [1, 2, 3])

# Accessing an element (O(1))
print(arr[1])  # Output: 2

# Inserting an element (O(n) due to shifting elements)
arr.insert(1, 4)  # arr becomes [1, 4, 2, 3]
```

### Using `NumPy` for Fixed-Type String Arrays

We still want sushi! Give us an array of strings, using **NumPy**:

```python
import numpy as np

# Creating a fixed-type array of strings
sushi_conveyor = np.array(["Salmon Nigiri", "Fatty Tuna Sashimi", "Eel Hand Roll"], dtype=str)

# Accessing an element (O(1))
print(sushi_conveyor[1])  # Output: Fatty Tuna Sashimi

# Inserting an element (creates a new array)
sushi_conveyor = np.insert(sushi_conveyor, 1, "Shrimp Tempura Roll")
print(sushi_conveyor)  # Output: ['Salmon Nigiri' 'Shrimp Tempura Roll' 'Fatty Tuna Sashimi' 'Eel Hand Roll']
```
