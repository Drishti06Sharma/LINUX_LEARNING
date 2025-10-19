# 🐧 **Day 1 — Linux Basics: Level 1 Adventure Mode 🕹️**

![Level Badge](https://img.shields.io/badge/LEVEL-1-blue?style=for-the-badge\&logo=linux)
![XP Badge](https://img.shields.io/badge/XP-100%2F100-brightgreen?style=for-the-badge)
![Status](https://img.shields.io/badge/STATUS-Explorer-success?style=for-the-badge)

> 🎯 **Mission:** Learn 7 core Linux commands — your first step to terminal mastery.
> 🧭 **Goal:** Reach **Level 2 Explorer** status by completing all tasks, games, and quizzes.
> 🧩 **XP Reward:** +100 XP
> 🏆 **Badge Unlocked:** 🐧 *Terminal Rookie*

```
Progress: [▓▓▓░░░░░░░░░] 30% — The Journey Begins!
```

---

## 🌍 **Stage 1: Find Your Path — `pwd`**

💡 **Concept:**
Your Linux map begins with `pwd`. It shows *where you are* right now.

```bash
pwd
```

📘 **Example Output:**

```
/home/drishti/Documents
```

🎮 **Mini Game — “Where Am I?”**

* Type `pwd`
* Move to another folder (`cd Downloads`)
* Run `pwd` again
  Every unique output = **+5 XP**

---

## 📦 **Stage 2: Explore Your Surroundings — `ls`**

💡 **Concept:**
`ls` lets you *see* what’s inside your current directory.

```bash
ls
```

✨ **Variations:**

| Command  | Description                   |
| -------- | ----------------------------- |
| `ls`     | Lists visible files           |
| `ls -a`  | Shows *all*, even hidden ones |
| `ls -l`  | Detailed list                 |
| `ls -lh` | Human-readable sizes          |
| `ls -R`  | Recursive list                |

🎮 **Game — “Hidden Treasure”**
Run `ls` → now `ls -a` → spot files starting with `.`
Each hidden file found = **+10 XP**

```
Progress: [▓▓▓▓░░░░░░░░] 45% — Explorer Unlocked!
🏅 Badge: 🧭 File Finder
```

---

## 🏗️ **Stage 3: Build Your World — `mkdir`**

💡 **Concept:**
`mkdir` builds new folders — like rooms in your Linux mansion 🏠

```bash
mkdir linux_day1
```

💥 **Bonus:**
Create multiple at once:

```bash
mkdir day1 day2 day3
```

🎮 **Challenge — “Folder Sprint”**
Create 3 folders in under 10 seconds ⏱️ → **+15 XP**

---

## 🧹 **Stage 4: Clean the Arena — `rmdir` & `rm -r`**

💡 **Concept:**
`rmdir` = remove *empty* folders
`rm -r` = remove *anything*, even filled ones ⚠️

```bash
rmdir empty_folder
rm -r folder_with_files
```

🎮 **Mission — “Cleanup Crew”**
Delete 3 old folders using only commands.
🧹 +20 XP → 🪓 **Clean Cutter Badge**

```
Progress: [▓▓▓▓▓░░░░░░░] 60% — Efficiency Rising!
```

---

## 📝 **Stage 5: Create Magic Scrolls — `touch`**

💡 **Concept:**
Create files instantly — blank scrolls for your notes 📜

```bash
touch notes.txt
```

💬 Create many:

```bash
touch file1.txt file2.txt file3.txt
```

🎮 **Quest — “File Crafter”**
Create 5 files in one command → **+10 XP**
🏅 Badge: 🧾 File Crafter

---

## 🚪 **Stage 6: Move Like a Pro — `cd`**

💡 **Concept:**
`cd` = move between worlds (directories).

| Command          | Action    |
| ---------------- | --------- |
| `cd folder_name` | Go inside |
| `cd ..`          | Go back   |
| `cd ~`           | Go home   |

🎮 **Game — “Terminal Maze”**
Reach `/home/drishti/Documents/linux_day1/practice`
(using only `cd`, `cd ..`, `pwd`)
+15 XP → 🚀 **Navigator Badge**

```
Progress: [▓▓▓▓▓▓▓░░░░░] 75% — Movement Mastered!
```

---

## 📜 **Stage 7: Read Your Scrolls — `cat`**

💡 **Concept:**
Read or merge files using `cat`.

```bash
cat notes.txt
cat file1.txt file2.txt > merged.txt
```

🎮 **Mission — “File Fusion”**
Merge 3 files → `final.txt`
🧩 +15 XP → Badge: **Data Alchemist**

---

## 🧱 **Final Boss — Build Your Linux Universe**

💡 **Goal:** Build this using *only* commands 👇

```
linux_learning/
├── day1/
│   ├── notes.txt
│   ├── commands.txt
│   └── practice/
```

🧠 **Hint:**

```bash
mkdir -p linux_learning/day1/practice
touch linux_learning/day1/notes.txt linux_learning/day1/commands.txt
```

🎮 **Bonus XP:** Run `tree linux_learning`
🏆 **Achievement Unlocked:** Builder of Folders (+25 XP)

```
Progress: [▓▓▓▓▓▓▓▓▓▓▓] 100% — Level 1 Complete!
🏅 Badge: 🐧 Linux Explorer
```

---

## 🧩 **Checkpoint Quiz**

| 🧠 Question                                                | 💬 Your Answer |
| ---------------------------------------------------------- | -------------- |
| 1️⃣ What does `pwd` do?                                    |                |
| 2️⃣ How do you list hidden files?                          |                |
| 3️⃣ What happens if you try `rmdir` on a non-empty folder? |                |
| 4️⃣ Which command moves you back one directory?            |                |
| 5️⃣ How can you create 3 files at once?                    |                |

🎯 **Each correct = +5 XP**
🏅 **Perfect Score:** Quiz Champion Badge 🧠

---

## 🏁 **LEVEL 1 COMPLETE!**

🎉 **You earned:**

* 🧭 File Finder
* 🪓 Clean Cutter
* 🧾 File Crafter
* 🚀 Navigator
* 🧩 Data Alchemist
* 🐧 Linux Explorer

✨ **Total XP: 100 / 100**

```
[▓▓▓▓▓▓▓▓▓▓▓] ✅ LEVEL 1 COMPLETE
```

---
