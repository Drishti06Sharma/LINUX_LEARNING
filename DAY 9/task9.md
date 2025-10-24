# 🗓️ **Day 9 — Networking Like a Linux Pro 🌐⚡**

Hey hey, Linux Star 🌟!  
Today we’re entering one of the coolest parts of Linux — **Networking**! 💻✨  

---

## 🧠 **What You’ll Learn Today**

✨ How to check your network connection  
✨ How to find your IP address  
✨ How to test if a site is reachable  
✨ How to check open ports  
✨ How to download files via terminal  

---

## 📘 **Commands of the Day**

| Command | What It Does | Example |
|----------|---------------|---------|
| `ifconfig` / `ip addr` | Shows your network info (IP, MAC, etc.) | `ip addr` |
| `ping` | Checks if a website/server is reachable | `ping google.com` |
| `hostname` | Shows your system name | `hostname` |
| `curl` | Fetches or downloads data from the internet | `curl https://example.com` |
| `wget` | Downloads files from URLs | `wget https://example.com/file.txt` |
| `netstat -tuln` | Shows open ports & connections | `netstat -tuln` |
| `traceroute` | Shows path your data takes to reach a website | `traceroute google.com` |
| `nslookup` | Finds the IP address of a website | `nslookup openai.com` |

---

## 🌍 **Task 1 — Check Network Details**

Let’s see your IP address and connection details 👇  
```bash
ip addr
````

or

```bash
ifconfig
```

💡 You’ll see something like:

```
inet 192.168.1.5
```

That’s your **local IP address** (like your digital name in the network!).

---

## 📶 **Task 2 — Test Internet Connection**

Try:

```bash
ping google.com
```

If you see responses like:

```
64 bytes from 142.250.183.206: icmp_seq=1 ttl=115 time=20.1 ms
```

🎉 Yay! Your internet is working perfectly!

Press `Ctrl + C` to stop the ping.

---

## 🧑‍💻 **Task 3 — Who Am I Online?**

Check your device name:

```bash
hostname
```

Or find your **public IP address** using:

```bash
curl ifconfig.me
```

This tells what your IP looks like to the world 🌎

---

## 🕵️ **Task 4 — Find Website Info**

Want to see what IP a website uses?

```bash
nslookup openai.com
```

It’ll show something like:

```
Name: openai.com
Address: 104.18.7.218
```

That’s the web server’s IP address! 🔢

---

## 📡 **Task 5 — Check Active Ports**

See what connections and services are active:

```bash
netstat -tuln
```

💬 You’ll get info about:

* **t**: TCP connections
* **u**: UDP connections
* **l**: Listening ports
* **n**: Show numeric IPs instead of names

⚠️ Use this to monitor which apps are listening on your system — super useful for admins!

---

## 📥 **Task 6 — Download a File**

Try downloading something simple:

```bash
wget https://example.com/sample.txt
```

Or with `curl`:

```bash
curl -O https://example.com/sample.txt
```

✅ The file will appear in your current directory!

---

## 🏁 **Summary**

Today you learned how to:
✅ Check your internet connection (`ping`)
✅ View IP and device info (`ip addr`, `hostname`)
✅ Look up websites (`nslookup`, `traceroute`)
✅ Download files from the internet (`wget`, `curl`)
✅ Monitor active network ports (`netstat`)

You’re officially a **Network Explorer 🌐🕵️‍♀️**

---

## 💡 **Challenge of the Day**

Write one command that:
1️⃣ Checks your IP address
2️⃣ Finds the IP of `github.com`
3️⃣ Pings it 3 times

👉 *Hint:* Combine `ip addr`, `nslookup`, and `ping -c 3`

If you do this successfully — you’ve mastered Linux networking 💪🐧

---

✨ **Quote of the Day:**

> “The network is the heart of the internet — and now, you know how to listen to its heartbeat.” 💓

