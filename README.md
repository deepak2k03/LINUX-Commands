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



## 🖊️ 9. `echo` and `cat` Commands

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
