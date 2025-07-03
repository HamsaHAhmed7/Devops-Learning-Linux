# 🔍 Level 8: Multi-File Searcher

## 🧠 Mission

Create a Bash script that:

- Accepts a **directory** and a **search word/phrase**
- Searches across all `.log` files in that directory
- Outputs the names (and lines) of the files that contain the word or phrase
- Handles both **interactive** and **argument-based** usage

---

## 📜 Script

```bash
#!/bin/bash

# Accept directory and search term as args or prompt if missing
directory="$1"
search_term="$2"

# Prompt for directory if not provided
if [ -z "$directory" ]; then
  echo -n "Enter directory path: "
  read directory
fi

# Validate that the path is a directory
if [ ! -d "$directory" ]; then
  echo "Provided path is not a directory."
  exit 1
fi

# Prompt for search term if not provided
if [ -z "$search_term" ]; then
  echo -n "Enter search word/phrase: "
  read search_term
fi

echo "🔎 Searching for '$search_term' in .log files in '$directory'..."

# Perform the search
results=$(find "$directory" -type f -name "*.log" -exec grep -Hn "$search_term" {} \;)

# Show results or fallback message
if [ -z "$results" ]; then
  echo "❌ No matches found."
  exit 1
else
  echo "✅ Matches found:"
  echo "$results"
  exit 0
fi

