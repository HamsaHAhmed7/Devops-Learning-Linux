# Level 4: Conditional Statements – File Existence and Permissions

## Objective:
Write a Bash script that:
- Checks if a file was passed as an argument
- Verifies if the file exists
- If it exists, checks and prints whether it is:
  - Readable
  - Writable
  - Executable

---

## 🧠 What You’ll Learn:
- How to use command-line arguments in scripts
- How to use `if`, `elif`, and `else` conditionals
- How to test for file permissions with `-r`, `-w`, and `-x`
- How to structure readable and robust condition blocks

---

## 📜 Script:

```bash
#!/bin/bash

# Check if a filename was passed as an argument
if [ -z "$1" ]; then
  echo "Please enter a file name."
  exit 1

# Check if the file exists
elif [ ! -f "$1" ]; then
  echo "$1 does not exist."
  exit 1

# If it exists, check permissions
else 
  echo "$1 exists, now checking the file permissions."

  if [ -r "$1" ]; then
    echo "$1 is readable."
  else
    echo "$1 is not readable."
  fi

  if [ -w "$1" ]; then
    echo "$1 is writable."
  else
    echo "$1 is not writable."
  fi

  if [ -x "$1" ]; then
    echo "$1 is executable."
  else
    echo "$1 is not executable."
  fi
fi

