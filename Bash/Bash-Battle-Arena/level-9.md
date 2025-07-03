# 🕵️‍♂️ Level 9: Hybrid Directory Monitoring Script

## 📌 Mission

Monitor a directory for:
- 📁 File **creation**
- ✏️ File **modification**
- ❌ File **deletion**

And log these changes with a **timestamp** into a file.

---

## 🧠 Features

- Accepts a directory path as input
- Uses **`fswatch`** if available for **real-time monitoring**
- Falls back to **manual polling** using `find` and `

