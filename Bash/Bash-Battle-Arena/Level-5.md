# 🧠 Level 5: Boss Battle - Combining Basics

## 🎯 Mission  
Combine what you've learned! Write a script that:

1. Creates a directory named `Battlefield`  
2. Inside `Battlefield`, create files: `knight.txt`, `sorcerer.txt`, and `rogue.txt`  
3. Check if `knight.txt` exists; if it does, move it to a new directory called `Archive`  
4. List the contents of both `Battlefield` and `Archive`

---

## 💻 My Solution

```bash
#!/bin/bash

# Create the Battlefield directory and character files
mkdir Battlefield
touch Battlefield/knight.txt Battlefield/sorcerer.txt Battlefield/rogue.txt

# Check for knight.txt and move it to Archive if found
if [ -f "Battlefield/knight.txt" ]; then
    mkdir -p Archive
    mv Battlefield/knight.txt Archive/
    echo "knight.txt has been moved to Archive."
else
    echo "knight.txt not found."
fi

# List contents of both directories
echo "Contents of Battlefield:"
ls Battlefield

echo "Contents of Archive:"
ls Archive

