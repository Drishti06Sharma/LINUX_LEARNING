 **Day 1 — Linux Basics: Level 1 Adventure Mode 🕹️**

> 🎯 **Mission:** Learn 7 core Linux commands — your first step to terminal mastery.

---

## 🌍 **Stage 1: Find Your Path — `pwd`**

💡 **Concept:**
`pwd` shows your current directory — where you are in the system.

```bash
pwd
```

📘 **Example Output:**

```
/home/drishti/Documents
```

🎮 **Try This:**

* Run `pwd`
* Navigate to another directory: `cd Downloads`
* Run `pwd` again

---

## 📦 **Stage 2: Explore Your Surroundings — `ls`**

💡 **Concept:**
`ls` lists the contents of your current directory.

```bash
ls
```

✨ **Useful Variations:**

| Command  | Description                           |
| -------- | ------------------------------------- |
| `ls`     | List visible files                    |
| `ls -a`  | Include hidden files (start with `.`) |
| `ls -l`  | Long listing (details)                |
| `ls -lh` | Long + human-readable sizes           |
| `ls -R`  | List recursively in subfolders        |

🎮 **Try This:**

* Run `ls`
* Then `ls -a`
* Spot hidden files (names starting with `.`)

---

## 🏗️ **Stage 3: Build Your World — `mkdir`**

💡 **Concept:**
Create new folders using `mkdir`.

```bash
mkdir linux_day1
```

💥 **Tip:**
You can make multiple folders at once:

```bash
mkdir day1 day2 day3
```

🎮 **Try This:**

* Create 3 folders with one command

---

## 🧹 **Stage 4: Clean the Arena — `rmdir` & `rm -r`**

💡 **Concepts:**

* `rmdir` removes *empty* folders
* `rm -r` removes folders *with* files

```bash
rmdir empty_folder
rm -r folder_with_files
```

🎮 **Try This:**

* Create and delete a test folder using both commands

---

## 📝 **Stage 5: Create Magic Scrolls — `touch`**

💡 **Concept:**
Use `touch` to create empty files.

```bash
touch notes.txt
```

💬 Create many files at once:

```bash
touch file1.txt file2.txt file3.txt
```

🎮 **Try This:**

* Create 5 files in one command

---

## 🚪 **Stage 6: Move Like a Pro — `cd`**

💡 **Concept:**
`cd` is used to change directories.

| Command          | Action     |
| ---------------- | ---------- |
| `cd folder_name` | Go inside  |
| `cd ..`          | Go back    |
| `cd ~`           | Go to home |

🎮 **Try This:**

* Navigate to:
  `/home/drishti/Documents/linux_day1/practice`
  using only `cd`, `cd ..`, and `pwd`

---

## 📜 **Stage 7: Read Your Scrolls — `cat`**

💡 **Concept:**
Use `cat` to read file contents or combine files.

```bash
cat notes.txt
cat file1.txt file2.txt > merged.txt
```

🎮 **Try This:**

* Merge 3 files into `final.txt`

---

## 🧱 **Final Boss — Build Your Linux Universe**

🎯 **Goal:** Recreate this folder structure using only commands:

```
linux_learning/
├── day1/
│   ├── notes.txt
│   ├── commands.txt
│   └── practice/
```

💡 **Hint:**

```bash
mkdir -p linux_learning/day1/practice
touch linux_learning/day1/notes.txt linux_learning/day1/commands.txt
```

🎮 **Try This:**

* Run the commands
* Use `tree linux_learning` to see the result (install `tree` if needed)

---

## 🧩 **Checkpoint Quiz**

| 🧠 Question                                                | 💬 Your Answer |
| ---------------------------------------------------------- | -------------- |
| 1️⃣ What does `pwd` do?                                    |                |
| 2️⃣ How do you list hidden files?                          |                |
| 3️⃣ What happens if you try `rmdir` on a non-empty folder? |                |
| 4️⃣ Which command moves you back one directory?            |                |
| 5️⃣ How can you create 3 files at once?                    |                |

---

## ✅ **Day 1 Complete!**

You’ve now learned the essential commands:

* `pwd`
* `ls`
* `mkdir`
* `rmdir` / `rm -r`
* `touch`
* `cd`
* `cat`

You're ready for Level 2!

---