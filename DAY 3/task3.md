# 🗓️ **Day 3 — Working with Files Like a Linux Hero 💪🐧**

Welcome back, Linux Learner! 👋  
You already know how to **create files and folders**, and how to **set permissions**.  
Today, we’ll learn how to **see what’s inside files**, **copy**, **move**, and **delete them safely**.  

Let’s get started 🚀  

---

## 🪄 **What You’ll Learn Today**
✨ See what’s inside a file  
✨ Copy or move files and folders  
✨ Delete things (carefully 😅)  
✨ Check what kind of file something is  

---

## 📘 **Commands of the Day**

| Command | What It Does | Example |
|----------|---------------|---------|
| `cat` | Shows the whole file | `cat notes.txt` |
| `less` | Shows big files page by page | `less story.txt` |
| `head` | Shows the **first few lines** | `head notes.txt` |
| `tail` | Shows the **last few lines** | `tail notes.txt` |
| `cp` | Copies files or folders | `cp file1.txt backup/` |
| `mv` | Moves or renames things | `mv old.txt new.txt` |
| `rm` | Deletes files or folders | `rm old.txt` |
| `file` | Tells you what kind of file it is | `file image.png` |
| `stat` | Shows extra details like size, date, permissions | `stat notes.txt` |

💡 **Tip:**  
When a file is *really big*, use `less` instead of `cat` — it won’t flood your screen 😅  

---

## 🎯 **Tasks for Today**

### 🧠 Task 1 — Viewing Files
1. Make a file:  
   ```bash
   touch demo.txt
````

2. Add text to it:

   ```bash
   echo "I love learning Linux!" > demo.txt
   ```
3. Try these:

   ```bash
   cat demo.txt
   head demo.txt
   tail demo.txt
   less demo.txt
   ```
4. Write in your notes:

   > Which command shows a big file easily? (`cat` or `less`?)

````

### 💼 Task 2 — Copy & Move

1. Make a folder:

   ```bash
   mkdir backup
   ```
2. Copy your file there:

   ```bash
   cp demo.txt backup/
   ```
3. Rename it:

   ```bash
   mv backup/demo.txt backup/my_demo.txt
   ```
4. Check what’s inside the folder:

   ```bash
   ls backup
   ```

🎉 Yay! You just copied and renamed your first file!

---

### ⚠️ Task 3 — Delete (Be Careful!)

1. Make a test file:

   ```bash
   touch temp.txt
   ```
2. Delete it:

   ```bash
   rm temp.txt
   ```
3. Want to delete a folder?

   ```bash
   rm -r backup
   ```

⚠️ **Be careful!** Once deleted, it’s gone forever.
✅ Use this safer version:

```bash
rm -ri backup
```

It asks before deleting each file.

---

### 🔍 Task 4 — File Info Detective 🕵️

1. Run:

   ```bash
   file demo.txt
   ```

   → It tells you what type of file it is (text, image, etc.)
2. Run:

   ```bash
   stat demo.txt
   ```

   → You’ll see when it was made, changed, and its size in bytes!

---

## 💡 **Challenge of the Day**

Write a one-line command that:

1. Creates a file named `today.txt`
2. Writes “I completed Day 3 🎉” into it
3. Displays it on the screen
   👉 *(Hint: Combine `echo`, redirection `>`, and `cat`)*

---


## 🏁 **Summary**

Today you learned how to:
✅ See file content (`cat`, `less`, `head`, `tail`)
✅ Copy, move, and rename files (`cp`, `mv`)
✅ Delete files safely (`rm`, `rm -ri`)
✅ Check file details (`file`, `stat`)

You’re now a **File Operation Hero 🦸‍♀️**

---

✨ **Quote of the Day:**

> “In Linux, every file has a story — your job is to read, move, or clean them wisely.” 💬

See you on **Day 4** 🧭 — where we’ll learn the *search powers* of `grep` and `find` 🔍

👩‍💻 **Happy Learning!**

```

---
