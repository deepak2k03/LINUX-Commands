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

✅ **End of Document**  
This guide covers all fundamental Linux commands essential for beginners.  
Practice them regularly to build confidence in the command line.  
