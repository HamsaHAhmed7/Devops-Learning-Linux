# Level 2: File Operations – Create, Write, and Read

## Objective:
Write a Bash script that:
- Creates a directory
- Navigates into it
- Creates a file inside it
- Writes text into the file
- Displays the contents of the file

---

## 🧠 What You’ll Learn:
- How to use variables in scripts
- How to create directories and files
- How to write to and read from files
- How to handle basic errors gracefully

---

## 📜 Script:

```bash
#!/bin/bash

# Set variables
DIR_NAME="example"
FILE_NAME="test1.txt"
FILE_CONTENT="This is a test file."

# Create the directory
mkdir -p "$DIR_NAME"

# Navigate into the directory or exit if failed
cd "$DIR_NAME" || { echo "Failed to enter directory $DIR_NAME"; exit 1; }

# Create the file and write content
echo "$FILE_CONTENT" > "$FILE_NAME"
echo "File '$FILE_NAME' created with content."

# Display the file contents
echo "Displaying contents of $FILE_NAME:"
cat "$FILE_NAME"

