# 🗓️ **Day 11 — Environment Variables & PATH 🌱⚙️**

Hello, Linux Legend! 💪🐧  
Have you ever wondered **how Linux knows where to find commands** like `ls` or `python`? 🤔  

That magic happens because of something called **Environment Variables**!  
Let’s uncover the mystery in a fun way 🕵️‍♀️  

---

## 🧠 **What You’ll Learn Today**

✨ What environment variables are  
✨ How to view them  
✨ How to create your own variables  
✨ What the `PATH` variable does  
✨ How to make variables permanent  

---

## 💬 **What Are Environment Variables?**

Think of environment variables as **sticky notes** your system uses to remember important info. 🗒️  

For example:
- Your username 🧍
- Your home directory 🏠
- The places Linux should look for programs (the `PATH` 🌍)

They’re used by the system and apps to know “where things are” and “how to behave.”  

---

## 📘 **Commands of the Day**

| Command | What It Does | Example |
|----------|---------------|---------|
| `printenv` | Shows all environment variables | `printenv` |
| `echo $VARIABLE` | Shows the value of a variable | `echo $HOME` |
| `export` | Creates a new variable | `export MYNAME="Drishti"` |
| `unset` | Deletes a variable | `unset MYNAME` |
| `env` | Lists current environment variables | `env` |
| `PATH` | Tells Linux where to find commands | `echo $PATH` |
| `source` | Reloads configuration files | `source ~/.bashrc` |

---

## 🧩 **Task 1 — See Your Variables**

Run:
```bash
printenv
````

👀 You’ll see a long list — that’s all the environment variables!

Try checking specific ones:

```bash
echo $USER
echo $HOME
echo $SHELL
```

💬 These tell you your username, home directory, and default shell!

---

## 🧠 **Task 2 — Create Your Own Variable**

Try this:

```bash
export MYNAME="Drishti"
```

Now display it:

```bash
echo $MYNAME
```

✨ Output: `Drishti`

This variable exists only for this session — once you close the terminal, it disappears.

---

## 🧮 **Task 3 — The PATH Variable (The Star of the Show ⭐)**

Run:

```bash
echo $PATH
```

You’ll see something like:

```
/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

This means when you type a command (like `ls`),
Linux looks inside these folders to find it 👇

```
/usr/bin/ls
```

💡 So if a command isn’t in one of these folders, Linux won’t find it!

---

## 🚀 **Task 4 — Add Your Own Path**

Let’s say you made your own script in `/home/drishti/scripts`.
You can add that folder to your PATH like this:

```bash
export PATH=$PATH:/home/drishti/scripts
```

Now Linux can find your custom commands too! 🧙‍♀️

Try checking again:

```bash
echo $PATH
```

---

## 🔁 **Task 5 — Make It Permanent**

To make your variable or PATH change *stay forever*,
add it to your **~/.bashrc** file (or ~/.zshrc if you use Zsh):

1. Open file:

   ```bash
   nano ~/.bashrc
   ```
2. Add this line at the bottom:

   ```bash
   export MYNAME="Drishti"
   export PATH=$PATH:/home/drishti/scripts
   ```
3. Save and reload:

   ```bash
   source ~/.bashrc
   ```

✅ Now it’ll load every time you open the terminal!

---

## 🏁 **Summary**

Today you learned how to:
✅ See all environment variables (`printenv`, `env`)
✅ Create and remove variables (`export`, `unset`)
✅ Understand the PATH variable 🌍
✅ Add custom paths for your scripts
✅ Make your variables permanent

You’re now a **PATH & Environment Wizard 🧙‍♀️⚙️**

---

## 💡 **Challenge of the Day**

1️⃣ Create a variable `FAV_CMD` and set it to your favorite Linux command (like `ls`).
2️⃣ Add it permanently to your `.bashrc`.
3️⃣ Check if it’s available every time you open a new terminal!

Bonus 🌟:
Try adding a folder to your PATH and run a script from there.

---

✨ **Quote of the Day:**

> “The right PATH leads to success — even in Linux.” 😄

