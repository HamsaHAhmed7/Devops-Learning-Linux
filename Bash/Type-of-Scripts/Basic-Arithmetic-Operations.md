# Level 3: Basic Arithmetic – Four Operations in Bash

## Objective:
Write a Bash script that asks the user to enter two numbers, then performs **addition**, **subtraction**, **multiplication**, and **division**, and displays all the results.

---

## 🧠 What You’ll Learn:
- How to use `read` to collect user input
- How to use `$((...))` for integer arithmetic
- How to handle division safely using `bc`
- Basic conditional logic for error checking

---

## 📜 Script:

```bash
#!/bin/bash

echo "Please enter your first number:"
read number1

echo "Please enter your second number:"
read number2

# Perform operations
sum=$((number1 + number2))
diff=$((number1 - number2))
product=$((number1 * number2))

# Handle division by zero
if [ "$(echo "$number2 == 0" | bc)" -eq 1 ]; then
  quotient="Error: Division by zero is not allowed."
else
  quotient=$(echo "scale=2; $number1 / $number2" | bc)
fi

# Display results
echo "Results:"
echo "Addition: $sum"
echo "Subtraction: $diff"
echo "Multiplication: $product"
echo "Division: $quotient"

