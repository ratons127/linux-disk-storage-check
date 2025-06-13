# linux-disk-storage-check

To check disk space on an AlmaLinux system (or any Linux system), you can use the following commands:

### 1️⃣ Basic disk space usage

```bash
df -h
```

* `df` = disk free
* `-h` = human-readable (shows GB, MB, etc.)

Example output:

```
Filesystem      Size  Used Avail Use% Mounted on
/dev/sda1        50G   30G   18G  63% /
tmpfs            16G     0   16G   0% /dev/shm
```

### 2️⃣ Check specific directory usage

```bash
du -sh /path/to/directory
```

For example:

```bash
du -sh /
```

* `du` = disk usage
* `-s` = summary
* `-h` = human-readable

### 3️⃣ See disk usage of all directories (top level)

```bash
du -h --max-depth=1 /
```

### 4️⃣ Use `lsblk` to check disk partitions

```bash
lsblk
```

### 5️⃣ Use `ncdu` (more interactive, but needs installation)

```bash
sudo dnf install ncdu
ncdu /
```

---

👉 If you tell me whether it's a server or desktop, and whether you want total usage or to troubleshoot full disks, I can give you a more targeted command. Shall I?
