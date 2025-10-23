# 🗓️ **Day 7 — Networking Basics 🌐: Talk to the World from Your Terminal!**

Hey Tech Explorer 👋  

## 🌟 What You’ll Learn
✨ Check your network & IP address  
✨ Test connections using `ping`  
✨ Download files from the internet using `curl`  
✨ See open ports & active connections using `netstat` and `ss`  
✨ Know who’s online on your system ⚙️  

---

## 🧭 Part 1 — Check Your IP Address

Your **IP address** is like your digital home address 🏠 on the internet.  

To see it, use:
```bash
ifconfig
````

or (modern version):

```bash
ip a
```

📘 **Output Example:**
You’ll see something like:

```
inet 192.168.1.10
```

That’s your system’s **local IP address**.

💡 *If `ifconfig` isn’t found, install it using:*

```bash
sudo apt install net-tools
```

---

## 🛰️ Part 2 — Test Connection with `ping`

Want to see if your internet is working? Or if a website is reachable?
Use the **ping** command — it’s like asking, “Hey, are you there?” 🫶

### 💻 Example:

```bash
ping google.com
```

📈 You’ll see replies like:

```
64 bytes from google.com: time=30ms
```

That means the site is responding ✅

To stop pinging, press **Ctrl + C**

---

## 🌐 Part 3 — Check Who You’re Connected To

Use `netstat` or the newer `ss` command to view network connections 👀

### 🔍 Show all active connections:

```bash
netstat -tuln
```

or

```bash
ss -tuln
```

🧠 **Flags Meaning:**

* `t` → TCP connections
* `u` → UDP connections
* `l` → listening ports
* `n` → show numbers instead of names

💡 Try:

```bash
sudo ss -tulpn
```

👉 Shows which **process** (like Chrome or VS Code) is using each port.

---

## 📡 Part 4 — Who Am I Talking To? (`hostname` & `who`)

🖥️ To check your system’s **name on the network:**

```bash
hostname
```

👥 To see who’s logged in:

```bash
who
```

💬 Example Output:

```
drishti  tty1  Oct 22 10:00
```

That means user **drishti** is logged in.

---

## 📥 Part 5 — Download Files from the Internet 🌐

Want to grab something from the web directly into your Linux terminal? 😎

Use **`curl`** or **`wget`**.

### 💻 Example:

```bash
curl -O https://example.com/file.txt
```

or

```bash
wget https://example.com/file.txt
```

💡 `-O` saves it with the same name.
Try it on any safe link to test how files download.

---

## ⚙️ Part 6 — DNS Lookup with `nslookup` or `dig`

Every website name (like `google.com`) maps to an IP.
To see that IP, try:

```bash
nslookup google.com
```

Or the advanced version:

```bash
dig google.com
```

💬 This helps when troubleshooting internet issues — super useful for sysadmins! 🧠

---

## 💪 Challenge of the Day

🎯 1. Find your system’s IP address
🎯 2. Ping `github.com` and note the response time
🎯 3. List all your active connections
🎯 4. Download a small file from the internet using `wget`
🎯 5. Use `nslookup` to find the IP of your favorite website

*(Bonus: Record all your findings in a file called `network_log.txt`)*

```bash
ifconfig > network_log.txt
ping -c 3 github.com >> network_log.txt
ss -tuln >> network_log.txt
```

Now open it:

```bash
cat network_log.txt
```

Cool, right? 😎

---

## 🧾 Quick Recap

![xwe](<_- visual selection (5).png>)

You’ve just unlocked the power to **see and control your network** like a pro! ⚡

---

## ✨ Quote of the Day

> “Networking isn’t just about cables — it’s about connections, both human and digital.” 💬