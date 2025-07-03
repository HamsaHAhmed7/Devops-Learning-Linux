# 📁 File Sorting Script (Level 7)

This script lists all `.txt` files in a given directory and displays them sorted by **file size** (from smallest to largest).

---

## 🧠 What the Script Does

- Accepts a **directory path** as an argument.
- Checks if the argument is provided and is a valid directory.
- Lists all `.txt` files in the directory.
- Sorts them by size (smallest first).
- Displays filenames and their human-readable sizes.

---

## 📜 The Script

```bash
#!/bin/bash

# This script lists all the .txt files in a directory and sorts them by file size.

if [ -z "$1" ]; then
  echo "No directory specified. Usage: $0 <directory>"
  exit 1

elif [ ! -d "$1" ]; then
  echo "The specified path is not a directory: $1"
  exit 1

else 
  txt_size_in_a_dir="$(ls -lhS "$1"/*.txt 2>/dev/null | tac | awk '{print $9, $5}')"

  echo "List of .txt files sorted by size in directory $1:"
  echo "$txt_size_in_a_dir"
fi

