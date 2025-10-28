# 🗓️ **Day 13 — Process Management in Linux 🧠⚙️**

Hey Tech Star 🌟  
Ever wondered what happens *behind the scenes* when you open an app, run a command, or even just type `ls`?  
Well… Linux quietly starts **processes** — tiny programs that keep everything running smoothly 👾  

Today, you’ll learn how to **see, manage, stop, and control** those processes like a real System Administrator 🧑‍💻💪  

---

## 🧠 **What is a Process?**

A **process** is simply a program in execution.  
Every command you run creates a process!  

For example 👇  
```bash
firefox
````

This command starts a Firefox **process**.
Linux gives it a unique ID (called **PID** — Process ID).

---

## 🧩 **What You’ll Learn Today**

✨ Viewing running processes
✨ Finding process IDs (PID)
✨ Killing unresponsive processes
✨ Checking real-time CPU & memory usage
✨ Managing background & foreground jobs

---

## ⚙️ **Command 1 — `ps` (Process Status)**

📋 Shows a snapshot of all running processes.

```bash
ps
```

Output example:

```
PID  TTY      TIME     CMD
1234 pts/0    00:00:01 bash
1356 pts/0    00:00:05 firefox
```

💡 **PID** = Process ID
💡 **CMD** = Command used to start it

👉 To see *all* processes running in the system:

```bash
ps aux
```

---

## ⚙️ **Command 2 — `top` (Live Process Viewer)**

🖥️ Shows real-time system activity — like Task Manager in Windows!

```bash
top
```

You’ll see:

* CPU usage
* Memory usage
* Running process list
* Which process is using the most resources

💡 Press:

* `q` → to quit
* `k` → to kill a process
* `P` → sort by CPU
* `M` → sort by memory

🎮 It’s like monitoring your system live!

---

## ⚙️ **Command 3 — `htop` (Advanced Process Viewer)**

If installed, `htop` is like `top` but more colorful and user-friendly 🌈

Install it:

```bash
sudo apt install htop
```

Run it:

```bash
htop
```

Use your arrow keys to navigate, and `F9` to kill a process easily! 🕹️

---

## ⚙️ **Command 4 — `kill` (Stop a Process)**

If an app freezes or misbehaves, you can **end** it manually.

Find its PID first:

```bash
ps aux | grep firefox
```

Then kill it:

```bash
kill 1356
```

If it’s stubborn 😤:

```bash
kill -9 1356
```

⚠️ Use `-9` carefully — it *forces* the process to stop immediately.

---

## ⚙️ **Command 5 — `jobs`, `bg`, and `fg` (Background/Foreground Control)**

Run a process in the background:

```bash
firefox &
```

The `&` symbol runs it without blocking your terminal.

Check background jobs:

```bash
jobs
```

Bring it back to the foreground:

```bash
fg %1
```

Or send it back again:

```bash
bg %1
```

💬 This is super handy when multitasking in a terminal!

---


## 🧩 **Bonus Tip — See Who’s Logged In**

```bash
who
```

This command shows all users currently logged into your system 👥

And for system resource summary:

```bash
uptime
```

It shows how long your system’s been running and its load averages.

---

## 🏁 **Summary**

✅ You learned about **processes** and **PIDs**
✅ You viewed live system activity with `top` and `htop`
✅ You learned how to **kill** misbehaving processes
✅ You handled **background & foreground jobs**
✅ You’re now ready to *control Linux like a boss!* 😎

---

## 💡 **Challenge of the Day**

🧩 Task 1 — Open any app like `gedit` in background:

```bash
gedit &
```

🧩 Task 2 — Find its PID using:

```bash
ps aux | grep gedit
```

🧩 Task 3 — Kill it using the PID:

```bash
kill <PID>
```

🧩 Task 4 — Run `top` and observe which processes use the most CPU 💻

---

## ✨ **Quote of the Day:**

> “Control your processes, and you control your system.” 🧠⚙️

---
