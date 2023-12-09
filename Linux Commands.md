# Linux Commands Classification and Usage

This is a cheatsheet README.md file that provides information on the classification and detailed usage of common Linux commands.

## Navigation Commands

### 1. cd: Change Directory
   - **Usage:** `cd <directory>`
   - **Description:** This command is used to change the current working directory. Provide the target directory as an argument to navigate to. To navigate to the parent directory, use `cd ..`. This will move one level up in the directory structure.

```bash
# Change to the root directory
cd /
# Change to the home directory
cd ~

# Change to the parent directory
cd ..

# Change to a custom directory
cd /usr/bin
```

## File and Directory Management Commands

### 2. ls: List
   - **Usage:** `ls [options] [file/directory]`
   - **Description:** Lists files and directories in the current directory. The optional arguments can modify the output:
      - `-l`: Long format, displaying detailed information about files and directories.
      - `-a`: Shows hidden files, including those starting with a dot (`.`).
      - `-h`: Human-readable sizes (e.g., KB, MB).
   - **Example:** `ls -lah` - Lists files in long format, including hidden files, with human-readable sizes.

```bash
# List files in the current directory in long format with human-readable sizes
ls -lah

# List all files, including hidden ones
ls -a
```

### 3. cp: Copy
   - **Usage:** `cp <source> <destination>`
   - **Description:** Copies files or directories from the source to the destination. Use this command to duplicate files or create backups.

```bash
# Copy a file to a specific directory
cp file.txt /path/to/destination

# Copy a directory and its contents to a new location
cp -r source_directory /path/to/destination
```

### 4. mv: Move/Rename
   - **Usage:** `mv <source> <destination>`
   - **Description:** Moves files or directories from the source to the destination. Also used for renaming files or directories.
```bash
# Move a file to a specific directory
mv file.txt /path/to/destination

# Rename a file
mv old_file.txt new_file.txt
```

### 5. rm: Remove/Delete
   - **Usage:** `rm [options] <file/directory>`
   - **Description:** Removes or deletes files or directories. Exercise caution, as this action is irreversible. Options like `-r` are used for recursive deletion.
```bash
# Remove a file
rm file.txt

# Remove a directory and its contents recursively
rm -r directory
```

### 6. mkdir: Make Directory
   - **Usage:** `mkdir <directory>`
   - **Description:** Creates a new directory with the specified name.
```bash
# Create a new directory
mkdir new_directory
```
### 7. rmdir: Remove Directory
   - **Usage:** `rmdir <directory>`
   - **Description:** Removes an empty directory. Use with caution, as it does not work for directories containing files.
```bash
# Remove an empty directory
rmdir empty_directory
```
### 8. touch: Touch
   - **Usage:** `touch <filename>`
   - **Description:** Creates an empty file or updates the access/modification time of an existing file.
```bash
# Create a new empty file
touch new_file.txt

# Update the access/modification time of a file
touch existing_file.txt

# To create more than one file - 
# each of the parameters will be created as an individual file
touch hello world creating multiple files

# this will create multiple files -
# hello1, hello2, hello3, hello4 ... up to hello10
touch hello{1..10}

# create a file in the future
touch -d tommorow create_this_file_tommorow.txt
```



## File Reading, Exploring, Searching

### 9. cat: Concatenate
- **Usage:** `cat <filename>`
- **Description:** Displays the content of a file. Useful for viewing the entire content of small files.
```bash
# Display the content of a file
cat file.txt
```

### 10. grep: Global Regular Expression Print
- **Usage:** `grep <pattern> <filename>`
- **Description:** Searches for a specific pattern in the content of one or more files. Useful for text pattern matching.

```bash
# Search for a pattern in a file
grep "pattern" file.txt
```

## File Editing


### 11. vim: Vim
- **Usage:** `vim [filename]`
- **Description:** Vim is a powerful and highly configurable text editor. It has a steeper learning curve but offers advanced features and modes.
```bash
# Open or create a file for editing with Vim
vim file.txt
```

### 12. nano: Nano
- **Usage:** `nano [filename]`
- **Description:** Nano is a simple and user-friendly text editor for the command line. It provides basic text editing capabilities.
```bash
# Open or create a file for editing with Nano
nano file.txt
```

### 13. echo: Echo
- **Usage:** echo `[options] [string]`
- **Description:** Displays a message or string on the terminal. It is also used to redirect text into a file or append to an existing file.
```bash
# Display a simple message
echo "Hello, Linux!"

# Redirect text into a file
echo "Content to be written to a file" > output.txt

# Append text to an existing file
echo "Additional content" >> output.txt
```

## Permission and Ownership Commands

### 14. chmod: Change Mode
- **Usage:** `chmod <permissions> <filename>`
- **Description:** Changes file permissions, specifying them using a numeric or symbolic representation.
```bash
# Change file permissions to read, write, and execute for the owner
chmod 700 file.txt
```
### 15. chown: Change Owner
- **Usage:** `chown <owner>:<group> <filename>`
- **Description:** Changes the owner and/or group of a file. Specify the new owner and group.
```bash
# Change the owner of a file
chown newowner:newgroup file.txt
```
## Process Management Commands

### 16. ps: Process Status
- **Usage:** `ps [options]`
- **Description:** Displays information about running processes. Options can be used to customize the output.
```bash
# Display a list of all running processes
ps aux
```
### 17. kill: Kill
- **Usage:** `kill <process_id>`
- **Description:** Terminates a process with the specified process ID.
```bash
# Terminate a process with a specific ID
kill 1234
```
## Network Commands

### 18. ssh: Secure Shell
- **Usage:** `ssh [user@]hostname [command]`
- **Description:** Connects to a remote machine securely using the SSH protocol. You can specify the remote user, hostname, and optional command to execute remotely.
```bash
# Connect to a remote machine with a specific username and execute a command
ssh username@hostname "ls -l"
```

These commands form the foundation of Linux command-line operations. Refer to the respective man pages (`man <command>`) for detailed information on each command and its options.

## Author / Contributor

These snippents were gathered and organized by **Vladimir Balabanov** / username: __Grrr1337__.

## Useful YouTube links:

[60 Linux Commands you NEED to know (in 10 minutes)](url=https://www.youtube.com/watch?v=gd7BXuUQ91w)
