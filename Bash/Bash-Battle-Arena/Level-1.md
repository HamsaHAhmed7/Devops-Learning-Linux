# 🧪 Level 1: The Basics

## 🎯 Mission  
Create a directory named `Arena`, and inside it, create three files:  
`warrior.txt`, `mage.txt`, and `archer.txt`.  
Then, list the contents of the `Arena` directory.

---

## 💻 My Solution

```bash
#!/bin/bash

# --------------------------------------------
# Level 1: The Basics - Bash Battle Arena
# Mission:
# Create a directory named Arena and then inside it,
# create three files: warrior.txt, mage.txt, and archer.txt.
# List the contents of the Arena directory.
# --------------------------------------------

# Create the Arena directory if it doesn't exist
mkdir -p Arena

# Navigate into the Arena directory
cd Arena

# Create the required character files
touch warrior.txt     # Warrior character file
touch mage.txt        # Mage character file
touch archer.txt      # Archer character file

# List the contents of the Arena directory
ls -l

