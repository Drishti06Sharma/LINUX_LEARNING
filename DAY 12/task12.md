# 🗓️ **Day 12 — Crontab & Task Scheduling ⏰🤖**

Hey future SysAdmin! 👩‍💻👨‍💻  
Have you ever wanted your computer to do things *by itself* — like run backups every night or send a report every morning?  
Well, say hello to **Crontab** — your very own task robot 🤖  

---

## 💡 **What is Crontab?**

🕒 **Crontab** (short for *Cron Table*) is a Linux utility that lets you schedule commands or scripts to run **automatically** at specific times or intervals.

Think of it like setting an **alarm clock**, but for your commands ⏰  

Examples:
- Run a backup every night at 12 AM  
- Clean temp files every Sunday  
- Send an email reminder every morning  

---

## 🧠 **What You’ll Learn Today**

✨ What cron and crontab are  
✨ How to schedule automatic tasks  
✨ How to view, edit, and remove cron jobs  
✨ Understanding the timing format (the 5 stars ⭐)  

---

## 🧩 **Step 1 — Check If Cron Is Running**

Run this command to make sure cron service is active:
```bash
sudo service cron status
````

✅ If it’s running — great!
If not, start it with:

```bash
sudo service cron start
```

---

## ⚙️ **Step 2 — Open Crontab**

Each user has their *own* cron table (crontab).
To open and edit yours, run:

```bash
crontab -e
```

You’ll see a file like this:

```
# Edit this file to introduce tasks to be run by cron.
# Each line represents a scheduled job.
```

---

## 🕵️ **Step 3 — Crontab Syntax (The 5-Star Format) ⭐⭐⭐⭐⭐**

Here’s the magic formula 👇

```
*  *  *  *  *  command_to_run
│  │  │  │  │
│  │  │  │  └── Day of week (0 - 6) [Sunday=0]
│  │  │  └───── Month (1 - 12)
│  │  └──────── Day of month (1 - 31)
│  └─────────── Hour (0 - 23)
└────────────── Minute (0 - 59)
```

Example:

```
30 9 * * 1 echo "Good Morning Drishti!" >> ~/monday.txt
```

💬 This runs every **Monday at 9:30 AM**, adding the message to `monday.txt`.

---

## 🧩 **Step 4 — Examples You’ll Love 💕**

| Schedule                        | Syntax                | Meaning                        |
| ------------------------------- | --------------------- | ------------------------------ |
| Every minute                    | `* * * * * command`   | Runs continuously every minute |
| Every day at midnight           | `0 0 * * * command`   | Perfect for daily backups      |
| Every Sunday at 6 AM            | `0 6 * * 0 command`   | Weekly cleanup task            |
| Every 5 minutes                 | `*/5 * * * * command` | Runs every 5 minutes           |
| At 2:30 PM on 1st of each month | `30 14 1 * * command` | Monthly task                   |

---

## 🧠 **Step 5 — View and Delete Your Crontab**

👉 View all your cron jobs:

```bash
crontab -l
```

👉 Delete all cron jobs (careful ⚠️):

```bash
crontab -r
```

---

## 🧰 **Step 6 — Real Example: Daily Backup Script**

Let’s say you created a script called `backup.sh` inside `~/scripts/`.
You want it to run **every day at 10 PM**.

1️⃣ Open crontab:

```bash
crontab -e
```

2️⃣ Add this line:

```
0 22 * * * /home/drishti/scripts/backup.sh
```

3️⃣ Save & exit.
🎉 Boom — your system now runs it daily at 10 PM automatically!

---

## 🧩 **Step 7 — Check Cron Logs**

To confirm if cron is running your jobs:

```bash
grep CRON /var/log/syslog
```

🕵️ This shows what cron has been doing behind the scenes!

---



## 🏁 **Summary**

✅ You learned what **Crontab** is
✅ Understood the **5-star timing format** ⭐⭐⭐⭐⭐
✅ Created your own scheduled jobs
✅ Learned how to check and remove them
✅ Built your first **automated Linux task** 💪

You’ve just unlocked **Linux automation superpowers! ⚡🤖**

---

## 💡 **Challenge of the Day**

Create a cron job that:

* Prints `"Stay consistent, Drishti!"` every day at 9 AM 🕘
* Saves it inside a file `motivation.txt` in your home directory

👉 Hint:

```bash
0 9 * * * echo "Stay consistent, Drishti!" >> ~/motivation.txt
```

Run it for a few days and see your motivational notes appear daily 💪🌞

---

✨ **Quote of the Day:**

> “Automation doesn’t replace effort — it multiplies it.” ⚙️✨

---
