# 🗓️ **Day 10 — Disk Management & Storage 💾📊**

Hey there, Storage Superstar 🌟!  
Have you ever seen this scary message —  
> “No space left on device”? 😨  

Well, today you’ll learn how to **check where your space is going**,  
how to **mount drives**, and **clean up your system like a pro** 🧹✨  

Let’s get started 🚀  

---

## 🧠 **What You’ll Learn Today**

✨ Check available disk space  
✨ See folder sizes  
✨ Mount & unmount drives  
✨ Understand file systems  
✨ Clean up unused files safely  

---

## 📘 **Commands of the Day**

| Command | What It Does | Example |
|----------|---------------|---------|
| `df -h` | Shows disk space usage | `df -h` |
| `du -h` | Shows size of folders/files | `du -h /home` |
| `lsblk` | Lists all disks & partitions | `lsblk` |
| `mount` | Mounts a drive or partition | `sudo mount /dev/sdb1 /mnt` |
| `umount` | Unmounts a drive | `sudo umount /mnt` |
| `blkid` | Shows info about disks (UUID, type) | `sudo blkid` |
| `fdisk -l` | Lists disks with detailed info | `sudo fdisk -l` |
| `df -Th` | Shows disk type + space usage | `df -Th` |
| `du -sh *` | Shows size of everything in current folder | `du -sh *` |

---

## 📊 **Task 1 — Check Disk Space**

Start by checking your disk space:
```bash
df -h
````

💬 You’ll see columns like:

* **Filesystem** — The drive name
* **Used / Available** — How much space is used and free
* **Mounted on** — Where it’s connected in your system

The `-h` means *human-readable* (shows GB/MB instead of bytes) 😄

---

## 📁 **Task 2 — See Folder Sizes**

Wondering which folder eats your space? 🍕
Try:

```bash
du -sh *
```

It shows the size of every folder in your current directory.
For example:

```
1.2G  Videos  
500M  Downloads  
20M   Documents  
```

Now you know who the space-hog is 🕵️‍♀️

---

## 💽 **Task 3 — List Your Drives**

See all attached drives and partitions:

```bash
lsblk
```

Output looks like:

```
sda    100G  
 ├─sda1  512M /boot  
 ├─sda2  99G  /
sdb     32G  
 └─sdb1  32G  
```

💡 `sda` is your main disk, `sdb` could be a USB or external drive!

---

## 🔌 **Task 4 — Mount & Unmount Drives**

### To Mount a Drive:

1. Create a mount point (a folder where you’ll attach it):

   ```bash
   sudo mkdir /mnt/usb
   ```
2. Mount it:

   ```bash
   sudo mount /dev/sdb1 /mnt/usb
   ```

✅ Now you can access your USB contents inside `/mnt/usb`

### To Unmount:

```bash
sudo umount /mnt/usb
```

⚠️ Always unmount before removing a drive physically — or risk data loss!

---

## 🧹 **Task 5 — Clean Your System**

Run these to keep your Linux tidy:

```bash
sudo apt autoremove
sudo apt clean
```

💬 `autoremove` removes unused packages
💬 `clean` clears cache from package downloads

Your system will thank you 🧼💻

---

## 🏁 **Summary**

Today you learned how to:
✅ Check storage space (`df -h`, `du -h`)
✅ See your drives and partitions (`lsblk`, `fdisk -l`)
✅ Mount and unmount devices (`mount`, `umount`)
✅ Clean your system (`apt autoremove`, `apt clean`)

You’re now officially a **Disk Management Expert 💾✨**

---

## 💡 **Challenge of the Day**

1️⃣ Check which folder in your home directory takes the most space
2️⃣ Mount a USB drive (real or virtual)
3️⃣ Clean your system using `sudo apt autoremove`

Bonus: Share how much space your `/home` folder uses 📊

---

✨ **Quote of the Day:**

> “Take care of your disks, and your disks will take care of you.” 💬

---
