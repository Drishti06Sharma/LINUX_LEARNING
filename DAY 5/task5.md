# 🗓️ **Day 5 — Connect the Commands 🔁: Pipes & Redirection in Linux**

Hey Linux Explorer 👋  

You’ve come a long way — from creating files to finding them like a pro!  
But have you ever thought… 🤔  
What if one command could *send its result* straight into another command — like passing a secret note? 💌  

That’s exactly what **pipes** and **redirection** do!  
They help your commands *work together* like teammates 🧑‍🤝‍🧑  

Let’s dive in and see how this magic works ✨  

---

## 🌟 What You’ll Learn Today
- 🎯 What redirection really means  
- 🪄 How to use `>`, `>>`, and `<`  
- 🔗 How to connect commands with **pipes (|)**  
- ⚡ How to mix and match commands for powerful results  

---

## 🧩 Think of It Like This...

Imagine your commands as **mini machines** in a factory 🏭  

- Machine 1 creates something (output 🧃)  
- Machine 2 needs something to work with (input 🧠)  

If you connect them with pipes (`|`), the output of one becomes the input for the next — no middleman needed!  

---

## 🧭 Part 1 — Redirecting Output (`>` and `>>`)

By default, every command shows its output on your screen.  
But what if you want to **save** that output into a file? 💾  

That’s where **output redirection** comes in!

| Symbol | Meaning | Example |
|---------|----------|----------|
| `>` | Write output to a file (overwrites existing content) | `echo "Hello Linux" > note.txt` |
| `>>` | Append output to a file (adds to existing content) | `echo "Keep practicing!" >> note.txt` |

### 🧪 Try It Yourself:
```bash
echo "Linux is fun!" > notes.txt
cat notes.txt
````

👉 You’ll see: `Linux is fun!`

Now add more:

```bash
echo "Practice makes perfect!" >> notes.txt
cat notes.txt
```

👉 The new line gets *added* instead of replacing the old one!

💡 **Remember:**

* Use `>` when creating or replacing.
* Use `>>` when adding more content.

---

## 📥 Part 2 — Redirecting Input (`<`)

Instead of typing input manually, you can **feed a file’s content** as input to a command.

Example:

```bash
cat < notes.txt
```

➡ Means: “Hey `cat`, read from this file instead of the keyboard!”

---

## 🔗 Part 3 — Piping Commands Together (`|`)

Here comes the coolest part 🕶️
A **pipe (`|`)** connects commands so one’s output becomes the next one’s input.

Think of it as:

```
Command 1 → Output → Command 2 → Result
```

### 💻 Try These Examples:

1. Count how many lines are in a file:

   ```bash
   cat notes.txt | wc -l
   ```

   🧮 `wc -l` = “word count - lines only”

2. List files, but show only the first 5:

   ```bash
   ls -l | head -n 5
   ```

3. Search for “Linux” in `.txt` files and sort them:

   ```bash
   grep "Linux" *.txt | sort
   ```

4. Find all running processes with “bash”:

   ```bash
   ps aux | grep bash
   ```

---

## ⚡ Part 4 — Combine Multiple Pipes

You can chain more than two commands together! 😎

Example:

```bash
cat notes.txt | grep "Linux" | wc -l
```

Breakdown:

1. `cat notes.txt` → show content
2. `grep "Linux"` → keep only lines with “Linux”
3. `wc -l` → count those lines

💥 Boom — 3 commands, one smooth result!

---

## 🧠 Quick Recap

✅ `>` — write/overwrite file
✅ `>>` — add to a file
✅ `<` — take input from a file
✅ `|` — connect commands together

You’ve just learned how to make commands **communicate** like best friends 🤝

---

## 💬 Mini Quiz (write in your notes.md)

1. What’s the difference between `>` and `>>`?
2. What does a pipe (`|`) do?
3. How do you count how many lines have “Linux” in a file?
4. What happens when you run this?

   ```bash
   cat notes.txt | grep "fun" | wc -l
   ```

---

## 💪 Challenge of the Day

Find out how many `.txt` files in your current directory mention the word “Linux”,
and save that number into a file called `result.txt`.

Hint 👇

```bash
find . -name "*.txt" | xargs grep -l "Linux" | wc -l > result.txt
```

Then check your result:

```bash
cat result.txt
```

---

## ✨ Quote of the Day

> “Linux commands are like LEGO blocks — when you connect them, you can build *anything*.” 🧱

