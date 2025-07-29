# 13 linux_commands_every_engineer_should_know :

## Overview 
lets see the basic commands and explination

# What is `pwd`?

`pwd` is a Linux command that stands for **Print Working Directory**.

It displays the **absolute path** of your current directory in the shell.

---

## ✅ Example:

```bash
pwd

## ✅ Output:
```bash
/home/karna/downloads/bash/bash-scripting-detailed-course/01-Introduction/basic-linux-commands


# What is `cd`?

`cd` stands for **Change Directory** in Linux.  
It is used to **navigate between directories** in the filesystem.

---

## ✅ Syntax:
```bash
cd [directory_name/_path]

## ✅ EXAMPLES:

### go to your home directory :
```bash
cd ~
### move one level up:
```bash
cd ..
### Go to the previous directory:
```bash
cd -

### ✅ Key Points:
- .  → Refers to the current directory.

- .. → Refers to the parent directory.

- ~ → Refers to the home directory.


## What is `ls`?

`ls` is a Linux command used to **list files and directories** in the current directory.

---

## ✅ Syntax:
```bash
ls [options] [directory]

#✅ Examples:
## 1. List all files in the current directory:
```bash
ls
## 2. List files in long format (with details like permissions, size, date):
```bash
ls -l
## 3. List hidden files (files starting with .):
```bash
 ls -a
## 4. List files in human-readable format:
```bash
ls -lh
## 5. List all files including hidden, in long format:
```bash
ls -la
## 6. List files in a specific directory:
```bash
ls /home/karna/downloads

# What is `cat`?

`cat` (short for **concatenate**) is a Linux command used to **display the contents of a file**, create files, and concatenate multiple files.

---

## ✅ Examples:

1. **Display the contents of a file:**
```bash
cat file.txt

2.Display the contents of multiple files:
```bash
cat file1.txt file2.txt

3.Create a new file using cat:
```bash
cat > newfile.txt
# Type your text and press CTRL+D to save and exit
4.Append text to an existing file:
```bash
cat >> existingfile.txt
# Type your text and press CTRL+D to save and exit
5.Display file contents with line numbers:
```bash
cat -n file.txt

6.Combine multiple files into one:
```bash
cat file1.txt file2.txt > combined.txt
 
 # What is `| grep`?

`grep` is a Linux command used to **search for a specific pattern or text within the output of another command or inside files**.

When combined with a pipe (`|`), it filters the output of the previous command.

---

## ✅ Syntax:
```bash
command | grep "pattern"

✅ Examples:
1.Search for a specific word in the output of ls:

```bash
ls | grep "file"
(This will show only files or directories containing the word "file".)

2.Search for a running process by name:
```bash
ps aux | grep "nginx"
(Displays all processes related to nginx.)

3.Find a specific user in /etc/passwd:
```bash
cat /etc/passwd | grep "karna"
(Shows lines containing the word "karna".)

4.Search for a word in a log file:
```bash
cat /var/log/syslog | grep "error"
(Displays all lines that contain the word "error".)

5.Case-insensitive search using -i:
```bash
ls | grep -i "file"
(Searches for "file", "File", or "FILE".)

6.Search recursively in files using grep -r:
```bash
grep -r "main" /home/karna/projects

# What is `cp`?

`cp` stands for **copy** in Linux.  
It is used to **copy files and directories** from one location to another.

---

## ✅ Syntax:
```bash
cp [options] source destination

✅ Examples:
1.Copy a file to another location:
```bash
cp file.txt /home/karna/backup/
2.Copy a file and rename it:
```bash
cp file.txt newfile.txt
3.Copy multiple files to a directory:
```bash
cp file1.txt file2.txt /home/karna/backup/
4.Copy an entire directory recursively:
```bash
cp -r myfolder /home/karna/backup/
5.Copy a file and preserve original file attributes (timestamps, permissions):
```bash
6.cp -p file.txt /home/karna/backup/
Show progress during copy using -v (verbose):
```bash
cp -v file.txt /home/karna/backup/

✅ Key Points:
-Use -r for directories.

-Use -p to preserve attributes.

-Use -v for verbose output.


#command -8
# What is `wc`?

`wc` stands for **word count** in Linux.  
It is used to **count lines, words, and characters in files or input**.

---

## ✅ Syntax:
```bash
wc [options] [file]

✅ Common Options:
-l → Count lines.

-w → Count words.

-c → Count bytes (characters).

-m → Count characters.

-L → Display length of the longest line.

✅ Examples:
Count lines, words, and characters in a file:
```bash
wc file.txt
(Output format: lines words bytes filename)

2.Count only lines:
```bash
wc -l file.txt
Count only words:

3.Count only words
```bash
wc -w file.txt

4.Count only characters:
```bash
wc -m file.txt

5.Count all for multiple files:
```bash
wc file1.txt file2.txt

6.Combine with cat and | (pipe) to count words from command output:
```bash
cat file.txt | wc -w

# Command-9
# What is `find`?

`find` is a Linux command used to **search for files and directories in a specified location based on conditions such as name, size, type, or modified date**.

---

## ✅ Syntax:
```bash
find [path] [options] [expression]

✅ Common Options:
-name → Search by file name.

-type → Search by type (f for file, d for directory).

-size → Search by file size.

-mtime → Search by modification time.

-exec → Run a command on the found files.

✅ Examples:
1.Find a file by name in the current directory:

```bash
find . -name "file.txt"

2.Find a file in a specific directory:

```bash
find /home/karna/documents -name "report.docx"

3.Find all directories named backup:

```bash
find /home/karna -type d -name "backup"

4.Find files larger than 10MB:

```bash
find /home/karna -type f -size +10M

5.Find files modified in the last 2 days:

```bash
find /home/karna -type f -mtime -2

6.Find and delete all .tmp files:

```bash
find /home/karna -type f -name "*.tmp" -exec rm -f {} \;

7.Find and display detailed info using ls -l:

```bash
find /home/karna -type f -name "*.sh" -exec ls -l {} \;

