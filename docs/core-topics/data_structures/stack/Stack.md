# Stack 🧙✨

You’re a wizard, and we need to practice spells! Every time you learn a new spell, you write it down on the top page of your spell notebook. But here’s the magical twist: you always cast the _last spell_ you wrote down _first_! This way of practicing is called **Last In, First Out (LIFO)**.

Here’s what your spell notebook might look like:

    Page 3: Wingardium Leviosa
    Page 2: Lumos
    Page 1: Expelliarmus

When it’s time to cast, you start with the top spell – _Wingardium Leviosa_! After that, you’ll cast _Lumos_, and finally _Expelliarmus_. You cast spells in the reverse order you learned them, just like a magical Spell Stack!

<p align="center">
<img src="https://media1.tenor.com/m/DYYLLQKAqOsAAAAC/dumbledore-harry-potter.gif">
</p>

## **Quick Facts! (for Wizards & Witches)** 🧹

| Spell Power       | Magic Speed |
| ----------------- | ----------- |
| Spell Storage     | O(n)        |
| Adding Spells     | O(1)        |
| Using Spells      | O(1)        |
| Peeking at Spells | O(1)        |

## **Magic Trick: Last In, First Out!** 🎩

The Spell Stack always takes the **last spell** you learned and pulls it out **first** when you need it.

<p align="center">
<img src="https://media0.giphy.com/media/v1.Y2lkPTc5MGI3NjExaml3aGZleHVndndpOXh6N3JzbmhkZWFkbmlzN3dtbWs0bWwwMjc1ayZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/EXmLHydTBn7gc/200.webp">
</p>

### **Why is the Stack Awesome?** 🌟

1. **Quick Magic!** The Spell Stack lets you add or pull out spells super fast. Perfect for when you need a spell _right now_!

2. **Smart Magic!** Only the latest spell comes out first, so you’re always ready for the newest danger.

### **How Wizards Use Spell Stacks** ⚡️

- **Quick Spell Access**: The Spell Stack helps you reach your most recent spells quickly, so you’re always ready in a duel!

- **Organized Practice**: Practicing spells with the Spell Stack means you can focus on your newest spells first, keeping them fresh.

- **Charm Order**: The Spell Stack keeps your spells neatly organized and easy to grab when it’s time to cast them. 📚

## **How to Build Your Own Spell Stack!** 🛠

You can make a Spell Stack with **two tools**:

### **Potion List** 🧪

Just keep adding new spells on top and remove from the top when needed!

```python
# Potion List version of Spell Stack
spell_stack = []

# Adding spells to the stack
spell_stack.append("Expelliarmus")        # Adding Expelliarmus spell
spell_stack.append("Lumos")               # Adding Lumos spell
spell_stack.append("Wingardium Leviosa")  # Adding Wingardium Leviosa spell

# Using the latest spell (Last In, First Out)
print("Using spell:", spell_stack.pop())  # Uses "Wingardium Leviosa"
print("Next spell ready:", spell_stack.pop())  # Uses "Lumos"
print("Another spell ready:", spell_stack.pop())  # Uses "Expelliarmus"
```

### **Wizard Array** 🧙‍♂️

Stack up your spells in an array, and always pull from the top!

```python
class SpellStack:
    def __init__(self):
        self.spells = []  # This is our Wizard Array

    def add_spell(self, spell):
        print(f"Adding {spell} spell to the stack!")
        self.spells.append(spell)

    def use_spell(self):
        if self.spells:
            return f"Using spell: {self.spells.pop()}"
        else:
            return "No spells left to use!"

# Let’s try it out
wizard_stack = SpellStack()
wizard_stack.add_spell("Expecto Patronum")
wizard_stack.add_spell("Accio")
wizard_stack.add_spell("Alohomora")

print(wizard_stack.use_spell())  # Uses "Alohomora"
print(wizard_stack.use_spell())  # Uses "Accio"
print(wizard_stack.use_spell())  # Uses "Expecto Patronum"
print(wizard_stack.use_spell())  # No spells left
```
