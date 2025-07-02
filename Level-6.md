# 🧾 Level 6: Argument Parsing

## 🎯 Mission  
Write a script that accepts a filename as an argument and prints the number of lines in that file.  
If no filename is provided, display a message saying `'No file provided'`.

---

## 💻 My Solution

```bash
#!/bin/bash

if [ -z "$1" ]; then
    echo "No file provided"
    exit 1
fi

if [ ! -f "$1" ]; then
    echo "File not found!"
    exit 1
fi

LINE_COUNT=$(wc -l < "$1")
echo "The file '$1' has $LINE_COUNT lines."
📝 Notes
$1 represents the first argument passed to the script.

-z "$1" checks if the argument is missing.

-f "$1" ensures the file exists and is a regular file.

wc -l < "$1" counts the number of lines using input redirection for clean output.

Script exits with exit 1 if validation fails — this is good practice.


