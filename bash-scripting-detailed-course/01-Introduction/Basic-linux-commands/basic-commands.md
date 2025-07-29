# 🐧 Linux Basic Commands – Complete Notes

---

## ✅ 1. What is `pwd`?
`pwd` stands for **Print Working Directory** in Linux.  
It displays the absolute path of your current directory in the shell.

### ✅ Example:
```bash
pwd
✅ Output:
bash
Copy
Edit
/home/karna/downloads/bash/bash-scripting-detailed-course/01-Introduction/basic-linux-commands
✅ 2. What is cd?
cd stands for Change Directory in Linux.
It is used to navigate between directories in the filesystem.

✅ Syntax:
bash
Copy
Edit
cd [directory_name/_path]
✅ Examples:
Go to your home directory:

bash
Copy
Edit
cd ~
Move one level up:

bash
Copy
Edit
cd ..
Go to the previous directory:

bash
Copy
Edit
cd -
✅ Key Points:
. → Current directory

.. → Parent directory

~ → Home directory

✅ 3. What is ls?
ls lists files and directories in the current directory.

✅ Syntax:
bash
Copy
Edit
ls [options] [directory]
✅ Examples:
bash
Copy
Edit
ls                # List all files
ls -l             # Long format
ls -a             # Show hidden files
ls -lh            # Human-readable format
ls -la            # All files in long format
ls /home/karna/downloads  # List files in specific directory
✅ 4. What is cat?
cat (short for concatenate) is used to display file contents, create files, and merge multiple files.

✅ Examples:
bash
Copy
Edit
cat file.txt                        # Display file content
cat file1.txt file2.txt             # Display multiple files
cat > newfile.txt                   # Create a new file (CTRL+D to save)
cat >> existingfile.txt             # Append text (CTRL+D to save)
cat -n file.txt                     # Display content with line numbers
cat file1.txt file2.txt > combined.txt  # Combine files
✅ 5. What is | grep?
grep searches for a specific pattern inside files or command outputs.
When combined with a pipe (|), it filters the output of the previous command.

✅ Syntax:
bash
Copy
Edit
command | grep "pattern"
✅ Examples:
bash
Copy
Edit
ls | grep "file"                  # Search for files
ps aux | grep "nginx"             # Find running process
cat /etc/passwd | grep "karna"    # Find user info
cat /var/log/syslog | grep "error" # Search for "error" in logs
ls | grep -i "file"               # Case-insensitive search
grep -r "main" /home/karna/projects # Recursive search
✅ 6. What is cp?
cp copies files and directories.

✅ Syntax:
bash
Copy
Edit
cp [options] source destination
✅ Examples:
bash
Copy
Edit
cp file.txt /home/karna/backup/      # Copy file
cp file.txt newfile.txt              # Copy and rename
cp file1.txt file2.txt /home/karna/backup/ # Copy multiple files
cp -r myfolder /home/karna/backup/   # Copy directory recursively
cp -p file.txt /home/karna/backup/   # Preserve attributes
cp -v file.txt /home/karna/backup/   # Verbose mode
✅ Key Points:
Use -r for directories

Use -p to preserve attributes

Use -v for verbose output

✅ 7. What is wc?
wc stands for word count. It counts lines, words, and characters.

✅ Syntax:
bash
Copy
Edit
wc [options] [file]
✅ Common Options:
-l → Count lines

-w → Count words

-m → Count characters

✅ Examples:
bash
Copy
Edit
wc file.txt          # Full count
wc -l file.txt       # Line count
wc -w file.txt       # Word count
wc -m file.txt       # Character count
cat file.txt | wc -w # Word count via pipe
✅ 8. What is find?
find searches for files and directories based on conditions like name, size, and time.

✅ Syntax:
bash
Copy
Edit
find [path] [options] [expression]
✅ Examples:
bash
Copy
Edit
find . -name "file.txt"                       # Find file by name
find /home/karna -type d -name "backup"      # Find directory by name
find /home/karna -type f -size +10M          # Find files larger than 10MB
find /home/karna -type f -mtime -2           # Find files modified in last 2 days
find /home/karna -type f -name "*.tmp" -exec rm -f {} \; # Delete tmp files
find /home/karna -type f -name "*.sh" -exec ls -l {} \;  # List .sh files with details
