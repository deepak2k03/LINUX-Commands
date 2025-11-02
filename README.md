# 🐧 Basic Linux Commands – Explained with Examples

This README demonstrates a few **basic Linux shell commands** executed on an **Ubuntu** terminal, along with explanations of what each command does.

---

## 🧩 1. `date`

```bash
ubuntu@ip-172-31-3-73:~$ date
Sat Nov  1 22:56:33 UTC 2025
```

**Description:**  
Displays the **current system date and time**.

✅ **Usage:**  
You can use it to check or log timestamps for tasks or scripts.

---

## 📂 2. `ls`

```bash
ubuntu@ip-172-31-3-73:~$ ls
```

**Description:**  
Lists all **files and directories** in the current working directory.

✅ **Tip:**  
- Use `ls -l` for a **long listing** (shows permissions, owner, size, date).  
- Use `ls -a` to show **hidden files** (those starting with a `.`).

---

## 🗂️ 3. `mkdir`

```bash
ubuntu@ip-172-31-3-73:~$ mkdir devops
```

**Description:**  
Creates a **new directory (folder)** named `devops`.

✅ **After creation:**
```bash
ubuntu@ip-172-31-3-73:~$ ls
devops
```

Now, the new folder `devops` appears in the directory list.

---

## 🔍 4. `ls -l`

```bash
ubuntu@ip-172-31-3-73:~$ ls -l
total 4
drwxrwxr-x 2 ubuntu ubuntu 4096 Nov  1 22:57 devops
```

**Description:**  
Displays a **detailed list** of files and directories, showing:
- **Permissions** (`drwxrwxr-x`)  
- **Number of links**  
- **Owner** (`ubuntu`)  
- **Group** (`ubuntu`)  
- **File size** (in bytes)  
- **Last modified date**  
- **File or directory name**

---

## 📍 5. `pwd`

```bash
ubuntu@ip-172-31-3-73:~$ pwd
/home/ubuntu
```

**Description:**  
Prints the **current working directory** — i.e., the folder you’re currently in.

---

## 📄 6. `touch`

```bash
ubuntu@ip-172-31-3-73:~$ touch newfile.txt
```

**Description:**  
Creates a **new empty file** named `newfile.txt` if it doesn’t already exist.  
If it exists, it updates its **timestamp** (modification time).

✅ **After creation:**
```bash
ubuntu@ip-172-31-3-73:~$ ls
devops  newfile.txt
```

---

## 📦 7. `mkdir`

```bash
ubuntu@ip-172-31-3-73:~$ mkdir cloud
```

**Description:**  
Creates another directory named `cloud`.

✅ **Now listing all files:**
```bash
ubuntu@ip-172-31-3-73:~$ ls -l
total 8
drwxrwxr-x 2 ubuntu ubuntu 4096 Nov  1 23:01 cloud
drwxrwxr-x 2 ubuntu ubuntu 4096 Nov  1 22:57 devops
-rw-rw-r-- 1 ubuntu ubuntu    0 Nov  1 23:01 newfile.txt
```

---

## 📄 8. `cd`

```bash
ubuntu@ip-172-31-3-73:~$ cd devops
```

**Description:**  
Used to change directory

✅ **After changing directory:**
```bash
ubuntu@ip-172-31-3-73:~/devops$ pwd
/home/ubuntu/devops
```

---

## 📄 9. `cd ..`

```bash
ubuntu@ip-172-31-3-73:~$ cd ..
```

**Description:**  
Used to come one step out of the directory

✅ **After changing directory:**
```bash
ubuntu@ip-172-31-3-73:~$ pwd
/home/ubuntu
```

---

## 📄 10. `rm`

```bash
ubuntu@ip-172-31-3-73:~/devops$ touch devops_file.txt
ubuntu@ip-172-31-3-73:~/devops$ ls
devops_file.txt
```

**Description:**  
Used to remove a file from the directory directory

✅ **After deleting file:**
```bash
ubuntu@ip-172-31-3-73:~/devops$ rm devops_file.txt
ubuntu@ip-172-31-3-73:~/devops$ ls
ubuntu@ip-172-31-3-73:~/devops$
```
---

## 📄 11. `rm -r`

```bash
ubuntu@ip-172-31-3-73:~$ ls
cloud  devops  newfile.txt
ubuntu@ip-172-31-3-73:~$ rm -r cloud
```

**Description:**  
Used to recursively delete the contents of a directory and then the directory itself

✅ **After deleting directory:**
```bash
rmdir folder_name

```
---

## 📄 12. `rmdir

```bash
rmdir folder_name
```

**Description:**  
Used to remove only empty directories



## 🖊️ 13. `echo` and `cat` Commands

### `touch demo.txt`
```bash
ubuntu@ip-172-31-3-73:~$ touch demo.txt
```
Creates an **empty file** named `demo.txt`.

### `echo`
```bash
ubuntu@ip-172-31-3-73:~$ echo "hello deepak"
hello deepak
```
Prints text to the terminal.

### Redirecting Output using `>`
```bash
ubuntu@ip-172-31-3-73:~$ echo "hello deepak" > demo.txt
```
The `>` operator redirects output into a file (creates or overwrites it).

### `cat`
```bash
ubuntu@ip-172-31-3-73:~$ cat demo.txt
hello deepak
```
Displays file contents or merges multiple files.

---
## 14. `head` — Display Beginning of File
**Description:**  
Shows the first few lines (default: 10) of a file.

**Usage:**
```bash
head [filename]
```
**Examples:**
```bash
head file.txt
head -n 5 file.txt    # Show first 5 lines
```

---

## 15. `tail` — Display End of File
**Description:**  
Shows the last few lines (default: 10) of a file.

**Usage:**
```bash
tail [filename]
```
**Examples:**
```bash
tail file.txt
tail -n 20 file.txt   # Show last 20 lines
tail -f log.txt       # Monitor file in real-time
```

---

## 16. `less` — View File with Navigation
**Description:**  
Opens a file for viewing with scroll capability.

**Usage:**
```bash
less [filename]
```
**Examples:**
```bash
less file.txt
```
**Navigation Keys:**
- `Space` → Next page  
- `b` → Previous page  
- `/word` → Search for “word”  
- `q` → Quit viewer

---

## 17. `more` — View File Page by Page
**Description:**  
Displays text one screen at a time.

**Usage:**
```bash
more [filename]
```
**Examples:**
```bash
more file.txt
```

---

## 18. `mv` — Move or Rename Files
**Description:**  
Moves or renames files and directories.

**Usage:**
```bash
mv [source] [destination]
```
**Examples:**
```bash
mv file.txt /home/user/Documents/       # Move file to Documents folder
mv oldname.txt newname.txt              # Rename a file
```

---

## 19. `wc` — Word Count
**Description:**  
Displays the number of lines, words, and characters in a file.

**Usage:**
```bash
wc [options] [filename]
```
**Examples:**
```bash
wc file.txt         # Displays lines, words, and characters
wc -l file.txt      # Displays only line count
wc -w file.txt      # Displays only word count
```

---

## 20. Hard Link
**Description:**  
A hard link is another name for an existing file. Both names point to the same data on the disk.  
Deleting one does **not** remove the data until all hard links are deleted.

**Usage:**
```bash
ln [existing_file] [link_name]
```
**Example:**
```bash
ln file1.txt file2.txt
```

---

## 21. Soft Link (Symbolic Link)
**Description:**  
A soft link (symbolic link) points to another file by its path.  
If the target file is deleted, the soft link becomes broken.

**Usage:**
```bash
ln -s [target_file] [link_name]
```
**Example:**
```bash
ln -s /home/user/file.txt link_to_file.txt
```

---

## 22. `cut` — Extract Columns from Text
**Description:**  
Extracts specific sections or columns from each line of a file.

**Usage:**
```bash
cut [options] [filename]
```
**Examples:**
```bash
cut -d',' -f1 file.csv   # Extract first column from CSV
cut -c1-5 file.txt       # Extract first 5 characters from each line
```

---

## 23. `tee` — Output to File and Screen Simultaneously
**Description:**  
Reads from standard input and writes to both standard output and files.

**Usage:**
```bash
command | tee [file]
```
**Examples:**
```bash
echo "Hello" | tee hello.txt       # Save and display output
ls | tee list.txt                  # Save list of files to a file
```

---

## 24. `sort` — Sort Lines of Text Files
**Description:**  
Sorts lines alphabetically or numerically.

**Usage:**
```bash
sort [options] [filename]
```
**Examples:**
```bash
sort file.txt              # Sort alphabetically
sort -r file.txt           # Sort in reverse order
sort -n numbers.txt        # Sort numerically
```

---

## 25. `diff` — Compare Files Line by Line
**Description:**  
Shows the differences between two files.

**Usage:**
```bash
diff [file1] [file2]
```
**Examples:**
```bash
diff file1.txt file2.txt
```
Output lines starting with `<` are from the first file, and those with `>` are from the second file.
---
## 🖋️ `vi` and `vim` Editors

### **1. `vi` — Visual Editor**
**Description:**  
`vi` (Visual Editor) is a built-in text editor in almost all Linux systems.  
It allows you to **create, edit, and save text files directly from the terminal**.

**Usage:**
```bash
vi [filename]
```
**Examples:**
```bash
vi notes.txt     # Opens or creates 'notes.txt' in vi editor
```

---

### **2. `vim` — Vi Improved**
**Description:**  
`vim` stands for **Vi IMproved**, an enhanced version of `vi` with features like:
- Syntax highlighting  
- Undo/Redo support  
- Line numbers  
- Better navigation and configuration options  

**Usage:**
```bash
vim [filename]
```
**Examples:**
```bash
vim code.c
```

---

### **3. Modes in `vi` / `vim`**

| Mode | Description |
|------|--------------|
| **Command Mode** | Default mode when you open a file. Used for navigation and commands (delete, copy, paste). |
| **Insert Mode** | Used to type or edit text. Enter this mode by pressing `i`, `a`, or `o`. |
| **Visual Mode** | Used to select text visually for copying, cutting, or formatting. Enter using `v`. |
| **Ex Mode** | Used to execute commands (like saving or quitting) by pressing `:`. |

---

### **4. Common `vi` / `vim` Commands**

| Action | Command |
|---------|----------|
| Enter Insert mode | `i` |
| Save file | `:w` |
| Quit editor | `:q` |
| Save and quit | `:wq` or `:x` |
| Quit without saving | `:q!` |
| Delete a line | `dd` |
| Copy a line | `yy` |
| Paste | `p` |
| Undo last change | `u` |
| Redo change | `Ctrl + r` |
| Search for a word | `/word` |
| Show line numbers | `:set number` |
| Go to a specific line | `:10` (goes to line 10) |

---

### **5. Exiting `vi` / `vim`**
If you’re stuck and can’t exit:
1. Press `Esc` to ensure you’re in **Command Mode**.  
2. Then type:
   - `:wq` → Save and quit  
   - `:q!` → Quit without saving  
