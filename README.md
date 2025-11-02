# 🐧 Basic Linux Commands – Explained with Examples

This README demonstrates commonly used **Linux shell commands**, along with examples and explanations.  
These commands work on most Linux distributions (like Ubuntu, Fedora, Arch, etc.) and are essential for beginners.  

---

## 🧩 1. `date` – Display Current Date and Time  
```bash
date
```
**Description:**  
Shows the current system date and time.  

---

## 📁 2. `ls` – List Directory Contents  
```bash
ls
ls -l
ls -a
```
**Description:**  
Displays files and directories in the current working directory.  
- `-l` → detailed list view  
- `-a` → shows hidden files  

---

## 🏗️ 3. `mkdir` – Make Directory  
```bash
mkdir myfolder
```
**Description:**  
Creates a new directory named `myfolder`.  

---

## 💻 4. `pwd` – Print Working Directory  
```bash
pwd
```
**Description:**  
Displays the full path of the current working directory.  

---

## 📄 5. `touch` – Create Empty File  
```bash
touch file.txt
```
**Description:**  
Creates an empty file or updates the timestamp if it already exists.  

---

## 🚶 6. `cd` – Change Directory  
```bash
cd Documents
cd ..
cd /
```
**Description:**  
- Moves to another directory.  
- `cd ..` → go one level up.  
- `cd /` → go to the root directory.  

---

## 🗑️ 7. `rm` – Remove Files  
```bash
rm file.txt
rm -r folder
```
**Description:**  
Removes a file or directory (`-r` for recursive delete).  

---

## 🧹 8. `rmdir` – Remove Empty Directory  
```bash
rmdir oldfolder
```
**Description:**  
Deletes an **empty** directory.  

---

## 💬 9. `echo` – Display Text or Variables  
```bash
echo "Hello, Linux!"
```
**Description:**  
Prints text or variable values to the terminal.  

---

## 📜 10. `cat` – View File Content  
```bash
cat file.txt
```
**Description:**  
Displays file contents, combine multiple files, or redirect output.  

---

## 🪄 11. `head` – Display Beginning of File  
```bash
head -n 5 file.txt
```
**Description:**  
Shows the first 5 lines of a file.  

---

## 🔚 12. `tail` – Display End of File  
```bash
tail -n 5 file.txt
```
**Description:**  
Displays the last 5 lines of a file.  

---

## 📖 13. `less` – Scroll Through File  
```bash
less file.txt
```
**Description:**  
Lets you scroll through file contents interactively.  
Use `q` to quit.  

---

## 📘 14. `more` – View File Page by Page  
```bash
more file.txt
```
**Description:**  
Displays file contents one screen at a time.  

---

## 🔁 15. `cp` – Copy Files or Directories  
```bash
cp source.txt destination.txt
cp -r folder1 folder2
```
**Description:**  
Copies files or directories (`-r` for recursive).  

---

## 📦 16. `mv` – Move or Rename Files  
```bash
mv file.txt /home/user/Documents/
mv oldname.txt newname.txt
```
**Description:**  
Moves or renames files and directories.  

---

## 🔢 17. `wc` – Word Count  
```bash
wc file.txt
wc -l file.txt
wc -w file.txt
wc -c file.txt
```
**Description:**  
Counts lines (`-l`), words (`-w`), and bytes (`-c`) in a file.  

---

## 🔗 18. `ln` – Create Links  
```bash
ln file.txt hardlink.txt
ln -s file.txt softlink.txt
```
**Description:**  
- **Hard link:** Points to the same inode (both remain valid until data deleted).  
- **Soft (symbolic) link:** Shortcut to the original file (breaks if the original is deleted).  

---

## ✂️ 19. `cut` – Extract Columns from File  
```bash
cut -d " " -f1 names.txt
```
**Description:**  
Extracts specific fields from lines using a delimiter.  

---

## 🧾 20. `tee` – Read and Write Simultaneously  
```bash
ls | tee files.txt
```
**Description:**  
Reads input and writes it to both standard output and a file.  

---

## 🧮 21. `sort` – Sort File Contents  
```bash
sort file.txt
sort -r file.txt
```
**Description:**  
Sorts lines alphabetically or numerically.  
Use `-r` for reverse order.  

---

## ⚖️ 22. `diff` – Compare Files Line by Line  
```bash
diff file1.txt file2.txt
```
**Description:**  
Shows differences between two files.  

---

## ✍️ 23. `vi` – Basic Text Editor  
```bash
vi file.txt
```
**Description:**  
A classic command-line text editor.  
**Modes:**  
- `i` → insert mode  
- `Esc` → command mode  
- `:w` → save  
- `:q` → quit  
- `:wq` → save and quit  

---

## 💡 24. `vim` – Improved Vi Editor  
```bash
vim file.txt
```
**Description:**  
Enhanced version of `vi` with syntax highlighting, plugins, and better navigation.  
**Shortcuts:**  
- `i` → insert  
- `Esc` → command  
- `:w` → save  
- `:q` → quit  
- `u` → undo  
- `/word` → search word  

---

# 🐧 Essential Linux System Commands – Explained with Examples

This README covers commonly used **Linux system administration commands** used for connecting to servers, monitoring system performance, and managing processes.  

---

## 🔐 1. `ssh` — Secure Shell Login

**Purpose:**  
Connects securely to a remote machine (like an AWS EC2 instance) over a network.

**Syntax:**
```bash
ssh -i "your-key.pem" username@public-ip
```

**Example:**
```bash
ssh -i "linux-for-devops-key.pem" ubuntu@13.233.101.24
```

**Explanation:**
- `-i` → path to your private key file.  
- `username` → depends on OS (`ubuntu`, `ec2-user`, etc.)  
- `public-ip` → EC2 instance IP address.  

---

## 💾 2. `df` — Disk Filesystem Usage

**Purpose:**  
Displays information about disk space usage of mounted file systems.

**Syntax:**
```bash
df -h
```

**Example Output:**
```
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvda1       20G   15G  4.2G  78% /
```

**Options:**
- `-h` → human-readable (MB/GB units).

---

## 📦 3. `du` — Disk Usage

**Purpose:**  
Shows how much disk space files or directories are using.

**Syntax:**
```bash
du -sh /var/log
```

**Explanation:**
- `-s` → summary of total size  
- `-h` → human-readable format  

---

## 🧠 4. `ps` — Process Status

**Purpose:**  
Displays currently running processes.

**Syntax:**
```bash
ps aux
```

**Output Example:**
```
USER       PID %CPU %MEM COMMAND
root         1  0.0  0.2 /sbin/init
ubuntu     452  0.3  1.1 /usr/bin/python3
```

**Options:**
- `a` → all users  
- `u` → show user details  
- `x` → include processes not attached to a terminal  

---

## 📊 5. `top` — Real-Time Process Monitoring

**Purpose:**  
Displays a dynamic, real-time view of system processes and resource usage.

**Usage:**
```bash
top
```

**Keys:**
- `q` → quit  
- `k` → kill a process  
- `M` → sort by memory  
- `P` → sort by CPU  

---

## 🔍 6. `fuser` — Identify Processes Using a File

**Purpose:**  
Shows which processes are accessing a specific file, directory, or port.

**Syntax:**
```bash
fuser /var/log/syslog
```

**Example:**
```bash
fuser -v /dev/sda1
```

**Options:**
- `-v` → verbose mode  
- `-k` → kill all processes using that file  

---

## ⚔️ 7. `kill` — Terminate a Process

**Purpose:**  
Sends a signal to terminate a process by its Process ID (PID).

**Syntax:**
```bash
kill <pid>
```

**Example:**
```bash
kill 1234
```

**Force kill:**
```bash
kill -9 1234
```

**Explanation:**  
`-9` sends the SIGKILL signal, forcing immediate termination.

---

## 🔁 8. `nohup` — Run Commands That Ignore Hangups

**Purpose:**  
Runs a command immune to hangups (e.g., when you close your terminal).

**Syntax:**
```bash
nohup command > output.log 2>&1 &
```

**Example:**
```bash
nohup python3 app.py > app.log 2>&1 &
```

**Explanation:**
- `nohup` → ignore hangup signals  
- `> app.log` → redirect output  
- `2>&1` → redirect errors too  
- `&` → run in background  

---

## 🧮 9. `free` — Memory Usage

**Purpose:**  
Displays amount of free and used memory in the system.

**Syntax:**
```bash
free -h
```

**Example Output:**
```
              total        used        free      shared  buff/cache   available
Mem:           1.9G        987M        654M         31M        278M        743M
Swap:            0B          0B          0B
```

---

## ⚙️ 10. `vmstat` — Virtual Memory Statistics

**Purpose:**  
Reports information about processes, memory, paging, block IO, and CPU activity.

**Syntax:**
```bash
vmstat 2 5
```

**Explanation:**
- The above runs every **2 seconds**, **5 times**.  

**Output Columns:**
- `procs` → process status  
- `memory` → swap and free memory  
- `cpu` → usage breakdown (user/system/idle)  

---

### 🧾 Summary

| Command | Purpose |
|----------|----------|
| ssh | Securely connect to remote systems |
| df | Show disk space usage |
| du | Show directory size usage |
| ps | List active processes |
| top | Monitor system processes |
| fuser | Identify which process is using a file/port |
| kill | Terminate processes |
| nohup | Run long jobs immune to terminal close |
| free | Display RAM usage |
| vmstat | System performance overview |
