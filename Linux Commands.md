# Linux Commands Classification and Usage

This is a **CheatSheet** README.md file that provides information on the classification and detailed usage of common **Linux commands**.

# Table of Contents
1. [Navigation Commands](#1-cd-change-directory)
2. [File and Directory Management Commands](#2-ls-list-the-files-in-the-directory)
3. [File Compression and Archive Commands](#9-zip-zip-a-file-or-directory)
4. [File Comparison and Sorting Commands](#11-cmp-compare-two-files)
5. [File Reading, Exploring, Searching](#13-cat-display-the-file-contents)
6. [File Editing](#15-vim-open-a-file-in-the-vim-text-editor)
7. [Permission and Ownership Commands](#18-chmod-change-mode-permissions-of-a-file)
8. [Process Management Commands](#20-ps-process-status--running-processes)
9. [Network Commands](#22-ssh-secure-shell--connect-to-a-vm)
10. [User Information Commands](#24-whoami-display-the-name-of-the-current-user)


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

### 2. ls: List the files in the directory
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

### 3. cp: Copy a file or a directory
   - **Usage:** `cp <source> <destination>`
   - **Description:** Copies files or directories from the source to the destination. Use this command to duplicate files or create backups.

```bash
# Copy a file to a specific directory
cp file.txt /path/to/destination

# Copy a directory and its contents to a new location
cp -r source_directory /path/to/destination
```

### 4. mv: Move/Rename file or directory
   - **Usage:** `mv <source> <destination>`
   - **Description:** Moves files or directories from the source to the destination. Also used for renaming files or directories.
```bash
# Move a file to a specific directory
mv file.txt /path/to/destination

# Rename a file
mv old_file.txt new_file.txt
```

### 5. rm: Remove/Delete file or directory
   - **Usage:** `rm [options] <file/directory>`
   - **Description:** Removes or deletes files or directories. Exercise caution, as this action is irreversible. Options like `-r` are used for recursive deletion.
```bash
# Remove a file
rm file.txt

# Remove a directory and its contents recursively
rm -r directory
```

### 6. mkdir: Create a Directory
   - **Usage:** `mkdir <directory>`
   - **Description:** Creates a new directory with the specified name.
```bash
# Create a new directory
mkdir new_directory
```
### 7. rmdir: Remove/Delete a Directory
   - **Usage:** `rmdir <directory>`
   - **Description:** Removes an empty directory. Use with caution, as it does not work for directories containing files.
```bash
# Remove an empty directory
rmdir empty_directory
```
### 8. touch: Create a file
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

## File Compression and Archive Commands
### 9. zip: Zip a file or directory
- **Usage**: `zip [options] <archive_name> <files/directories>`
- **Description**: Compresses files and directories into a zip archive.
```bash
# Create a zip archive of a file
zip archive.zip file.txt

# Create a zip archive of multiple files
zip archive.zip file1.txt file2.txt

# Create a zip archive of a directory and its contents
zip -r archive.zip directory
```

### 10. unzip: Unzip an archive file
- **Usage**: `unzip [options] <archive_name>`
- **Description**: Extracts files from a zip archive.
```bash
# Extract files from a zip archive
unzip archive.zip

# Extract files from a zip archive into a specific directory
unzip archive.zip -d /path/to/destination
```


## File Comparison and Sorting Commands
### 11. cmp: Compare two files
- Usage: `cmp [options] <file1> <file2>`
- Description: Compares two files byte by byte.
```bash
# Compare two files
cmp file1.txt file2.txt
```

### 12. diff: Display the difference between two files
- Usage: `diff [options] <file1> <file2>`
- Description: Displays the differences between two files.
```bash
# Show differences between two files
diff file1.txt file2.txt
```

## File Reading, Exploring, Searching

### 13. cat: Display the file contents
- **Usage:** `cat <filename>`
- **Description:** Displays the content of a file. Useful for viewing the entire content of small files.
```bash
# Display the content of a file
cat file.txt
```

### 14. grep: Search for a string/pattern (Global Regular Expression Print)
- **Usage:** `grep <pattern> <filename>`
- **Description:** Searches for a specific pattern in the content of one or more files. Useful for text pattern matching.

```bash
# Search for a pattern in a file
grep "pattern" file.txt
```

## File Editing

### 15. vim: Open a file in the Vim text editor
- **Usage:** `vim [filename]`
- **Description:** Vim is a powerful and highly configurable text editor. It has a steeper learning curve but offers advanced features and modes.
```bash
# Open or create a file for editing with Vim
vim file.txt
```

### 16. nano: Open a file in the Nano text editor
- **Usage:** `nano [filename]`
- **Description:** Nano is a simple and user-friendly text editor for the command line. It provides basic text editing capabilities.
```bash
# Open or create a file for editing with Nano
nano file.txt
```

### 17. echo: Display a message or append text to a file
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

### 18. chmod: Change Mode Permissions of a file
- **Usage:** `chmod <permissions> <filename>`
- **Description:** Changes file permissions, specifying them using a numeric or symbolic representation.
```bash
# Change file permissions to read, write, and execute for the owner
chmod 700 file.txt
```
### 19. chown: Change Owner
- **Usage:** `chown <owner>:<group> <filename>`
- **Description:** Changes the owner and/or group of a file. Specify the new owner and group.
```bash
# Change the owner of a file
chown newowner:newgroup file.txt
```
## Process Management Commands

### 20. ps: Process Status / Running processes
- **Usage:** `ps [options]`
- **Description:** Displays information about running processes. Options can be used to customize the output.
```bash
# Display a list of all running processes
ps aux
```
### 21. kill: Kill a process
- **Usage:** `kill <process_id>`
- **Description:** Terminates a process with the specified process ID.
```bash
# Terminate a process with a specific ID
kill 1234
```
## Network Commands

### 22. ssh: Secure Shell ( connect to a VM )
- **Usage:** `ssh [user@]hostname [command]`
- **Description:** Connects to a remote machine securely using the SSH protocol. You can specify the remote user, hostname, and optional command to execute remotely.
```bash
# Connect to a remote machine with a specific username and execute a command
ssh username@hostname "ls -l"
```

### 23. curl: cURL
- **Usage**: `curl [options] <URL>`
- **Description**: Transfers data to or from a network server. Supports many protocols, commonly used are HTTP and FTP.
```bash
# Download a file from a URL
curl -O https://example.com/file.txt

# Send a POST request with data
curl -X POST -d "data=example" https://api.example.com/endpoint
```

## User Information Commands

### 24. whoami: Display the name of the current user
- **Usage:** `whoami`
- **Description:** Displays the current username.
```bash
# Display the current username
whoami
```

### 25. useradd: Create a new user
- **Usage:** `useradd [options] <username>`
- **Description:** Creates a new user account. Options can be used to specify additional settings.
```bash
# Create a new user account
useradd newuser

# Create a user with a home directory and specific shell
useradd -m -s /bin/bash newuser
```

### 26. adduser: Create a new user (with advanced options)
- **Usage:** `adduser [options] <username>`
- **Description:** Adds a new user account interactively, prompting for additional information such as password and user details.
- **Options**:
    - `-m, --create-home:` Create the user's home directory.
    - `-s, --shell <shell>:` Specify the login shell for the user.
    - `-g, --gid <group>:` Specify the initial login group for the user.
    - `-G, --groups <groups>:` Specify additional groups for the user.

```bash
# Add a new user account interactively
adduser newuser
```
```bash
# Add a new user with a home directory and specific shell
adduser -m -s /bin/bash newuser

# Add a new user and assign to a specific group
adduser -g staff newuser

# Add a new user, assign to a group, and add to additional groups
adduser -g staff -G wheel,users newuser
```

## Author / Contributor

These snippents were gathered and organized by **Vladimir Balabanov** / username: __Grrr1337__.

## Useful YouTube links:

[60 Linux Commands you NEED to know (in 10 minutes)](url=https://www.youtube.com/watch?v=gd7BXuUQ91w)
