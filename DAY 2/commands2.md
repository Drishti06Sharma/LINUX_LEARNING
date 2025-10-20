# 🛡️ **Day 2 — File Permissions & Ownership in Linux**

Welcome to **Day 2** of your Linux Learning Adventure! 🐧
Yesterday, you mastered the basics — creating files, moving between directories, and organizing your space.
Today, we’ll uncover how **Linux protects your files** and how **you become the boss** of who can access them 💪

---

## 🎬 **1. Understanding File Permissions — Who Can Do What**

Every file in Linux is like a small kingdom 👑
And in your kingdom, there are three kinds of people:

| Role           | Who They Are             | Example               |
| -------------- | ------------------------ | --------------------- |
| **User (u)**   | The Owner — *you!* 🧍‍♀️ | You created the file  |
| **Group (g)**  | Your team 👩‍💻👨‍💻     | Members of your group |
| **Others (o)** | Everyone else 🌍         | Any random user       |

Each one has **three powers**:

* 🕵️ **Read (r)** — Can *look inside*
* ✍️ **Write (w)** — Can *edit or modify*
* 🚀 **Execute (x)** — Can *run* the file (if it’s a program or script)

---

## 🔎 **2. Peek at the Permissions**

To see the power distribution:

```bash
ls -l
```

Example Output:

```
-rw-r--r--  1 drishti  users  1200 Oct 19  notes.txt
```

🔍 **Breakdown:**

* `-` → It’s a **file** (a directory would show `d`)
* `rw-` → Owner: can read + write
* `r--` → Group: can only read
* `r--` → Others: can only read

📜 So the rule says:

> “Drishti can read and write, others can only read.”

Fair enough. But what if you want to change the rules?
That’s where your magic wand comes in... 🪄

---

## ⚙️ **3. `chmod` — The Magic Wand of Permissions**

> **CH**ange **MOD**e = `chmod`
> You use it to **grant or remove powers** for users, groups, and others.

---

### 🧩 **Method 1: The Numeric (Secret Code) Method**

Each permission has a secret value:

| Permission  | Code | Meaning           |
| ----------- | ---- | ----------------- |
| Read (r)    | 4    | You can open/view |
| Write (w)   | 2    | You can modify    |
| Execute (x) | 1    | You can run/enter |

Add them up to form codes for each group.

| User   | Permissions | Code | Symbol         |
| ------ | ----------- | ---- | -------------- |
| Owner  | rwx         | 7    | Full power     |
| Group  | r-x         | 5    | Read + execute |
| Others | r-x         | 5    | Read + execute |

So this command 👇

```bash
chmod 755 script.sh
```

means:

```
rwxr-xr-x
```

👑 You (owner): everything
👨‍👩‍👧 Group: read & run
🌍 Others: read & run

💡 **Tip:** Think of 755 as “Boss has all keys, others can peek and ring the doorbell.” 🔔

---

### 🎨 **Method 2: The Symbolic (Plain English) Method**

Not a fan of numbers? No problem!
You can use letters like `u`, `g`, `o`, and `a` to assign powers.

| Symbol | Meaning |
| ------ | ------- |
| `u`    | User    |
| `g`    | Group   |
| `o`    | Others  |
| `a`    | All     |

| Operator | Action               |
| -------- | -------------------- |
| `+`      | Add permission       |
| `-`      | Remove permission    |
| `=`      | Set exact permission |

Examples:

```bash
chmod u+x file.sh      # Give yourself execute permission
chmod g-w notes.txt    # Remove write from your group
chmod a=r file.txt     # Everyone can only read
chmod u=rw,g=r,o= file.txt  # Fine control for each level
```

🎭 **Pro Move:** Combine them!

```bash
chmod ug+w file.txt
```

➡️ You and your team both get write access!

---

## 💥 **4. Real-Life Permission Scenarios**

| Situation                                | Command                 | What It Does                        |
| ---------------------------------------- | ----------------------- | ----------------------------------- |
| 🧠 You wrote a script and want to run it | `chmod +x script.sh`    | Adds execute power                  |
| 🔒 You want a private file               | `chmod 700 secrets.txt` | Only you can open it                |
| 🌍 You’re sharing a read-only file       | `chmod 644 report.txt`  | Others can view, not edit           |
| 💾 You made a public script              | `chmod 755 runme.sh`    | Everyone can run, only you can edit |

⚠️ **Avoid:**

```bash
chmod 777 file.txt
```

Because that means *everyone can do everything!* 😱
(That’s like leaving your house keys under the welcome mat.)

---

## 🎯 **5. Fun Mini Challenge**

Try this step-by-step in your terminal 🧑‍💻

1️⃣ Create a file

```bash
touch magic.txt
```

2️⃣ Check its default permissions

```bash
ls -l
```

3️⃣ Make it private (only you can read/write)

```bash
chmod 600 magic.txt
```

4️⃣ Let your group read it

```bash
chmod g+r magic.txt
```

5️⃣ Then make it readable for everyone

```bash
chmod a+r magic.txt
```

6️⃣ Now remove execute rights from everyone

```bash
chmod a-x magic.txt
```

✨ **Bonus Twist:**
Run this just for fun and see what happens:

```bash
chmod 000 magic.txt
```

👉 Even *you* lose access! 😆
Recover it:

```bash
chmod 644 magic.txt
```

---

## 🧭 **6. Quick Permission Map**

| Code | User | Group | Others | Ideal For                    |
| ---- | ---- | ----- | ------ | ---------------------------- |
| 777  | rwx  | rwx   | rwx    | 💀 Avoid this unless testing |
| 755  | rwx  | r-x   | r-x    | Scripts / web files          |
| 700  | rwx  | ---   | ---    | Private stuff                |
| 644  | rw-  | r--   | r--    | Normal files                 |
| 600  | rw-  | ---   | ---    | Config or password files     |

---

## 🧠 **7. Lightning Quiz**

| Question                                                   | Your Answer |
| ---------------------------------------------------------- | ----------- |
| 1️⃣ What does `chmod 755 file` mean?                       |             |
| 2️⃣ How do you make a script executable only for yourself? |             |
| 3️⃣ What’s wrong with using `chmod 777` everywhere?        |             |
| 4️⃣ Which command removes write permission from the group? |             |
| 5️⃣ What does `chmod a=r file.txt` do?                     |             |

---

## 🚀 **Wrap-Up**

🎉 You just learned to use the Linux permission wand `chmod` like a wizard 🧙‍♀️
Now you can control *who sees what* and *who touches what*.

💬 Remember:

> “With great power comes great permission.” — *A Linux user, probably*

