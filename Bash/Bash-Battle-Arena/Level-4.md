# 📁 Level 4: File Manipulation

## 🎯 Mission  
Create a script that copies all `.txt` files from the `Arena` directory to a new directory called `Backup`.

---

## 💻 My Solution

```bash
#!/bin/bash

if [ -d Arena ]; then
    cp Arena/*.txt Backup/
fi

