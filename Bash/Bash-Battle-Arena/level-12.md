
---

### 🔹 **Level 12: Simple Configuration File Parser (`level12.md`)**

```markdown
# Level 12: Simple Configuration File Parser

## Objective:
Read a config file and display key-value pairs.

## Script:
```bash
#!/bin/bash

CONFIG_FILE="settings.conf"

if [ ! -f "$CONFIG_FILE" ]; then
    echo "Configuration file does not exist."
    exit 1
fi

while IFS='=' read -r key value; do
    echo "Key: $key, Value: $value"
done < "$CONFIG_FILE"

