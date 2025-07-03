
---

### 🔹 **Level 11: Automated Disk Space Report (`level11.md`)**

```markdown
# Level 11: Automated Disk Space Report

## Objective:
Monitor a directory's disk space and warn if it exceeds a set threshold.

## Script:
```bash
#!/bin/bash

DIRECTORY="Arena"
THRESHOLD=1

USAGE=$(du -sm "$DIRECTORY" | awk '{print $1}')

if [ "$USAGE" -gt "$THRESHOLD" ]; then
    echo "Warning: Disk usage for $DIRECTORY is at $USAGE%!"
else
    echo "Disk usage for $DIRECTORY is at $USAGE%. All is well."
fi

