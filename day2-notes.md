# 1. Initialize a new Git repository locally (skip if already inside a Git repo)
git init

# 2. Create the file and add your notes content
cat << 'EOF' > day2-notes.md
# Day 2 DevOps Notes: Linux Commands & Fundamentals

## 1. Basic Navigation & File Operations
* **ls**: Lists files and directories in the current location.
* **ls -l**: Lists files in long format showing detailed permissions, size, and modification date.
* **mkdir <dir_name>**: Creates a new directory.
* **pwd**: Prints the absolute path of the current working directory.
* **touch <file_name>**: Creates an empty file.
* **clear**: Clears the terminal screen.
* **cd <dir>**: Changes the working directory.
* **cd ..**: Moves back one directory level (parent directory).
* **rm <file_name>**: Removes a file.
* **rmdir <dir_name>**: Removes an empty directory.

## 2. File Content Reading & Text Processing
* **cat <file>**: Displays the contents of a file.
* **zcat <file.gz>**: Views contents of compressed (.gz) files without uncompressing them.
* **head -n 5 <file>**: Displays the top 5 lines of a file.
* **tail -n 5 <file>**: Displays the last 5 lines of a file.
* **tail -f <file>**: Real-time log monitoring; updates as lines are added.
* **less <file>**: Opens a file in a paginated, scrollable view.
* **cp <source> <dest>**: Copies files or directories.
* **mv <source> <dest>**: Renames or moves files and directories.
* **wc <file>**: Displays line, word, and byte counts.
* **cut -b <file>**: Cuts specified byte positions from a file.
* **tee <file>**: Reads standard input and writes it simultaneously to screen and file.
* **sort <file>**: Sorts lines of text alphabetically.
* **diff <file1> <file2>**: Shows line-by-line differences between two files.

## 3. Links in Linux
* **Hard Link (`ln <target> <link_name>`)**: Points directly to the inode of the original file.
* **Soft Link (`ln -s <target> <link_name>`)**: Creates a symbolic link (shortcut) pointing to the path of the original file.

## 4. SSH & Service Management
* **ssh**: Secure Shell used for encrypted remote access.
* **ssh-keygen**: Generates SSH public and private key pairs for authentication.
* **ssh -i <path_to_private_key> user@ip**: Connects to a remote server using a specific private key file.
* **sudo apt update**: Updates package list repository.
* **sudo apt install openssh-server**: Installs OpenSSH server software.
* **sudo systemctl status ssh**: Checks the active status of the SSH service.
* **ip a**: Displays IP address details for system network interfaces.

## 5. Linux Init Systems & Systemd
The Init Process (PID 1) is the parent process in Linux that initializes the system after booting and launches background services.

### Historical & Current Systems
* **SysVinit**: Traditional init system using runlevels (0–6).
* **Upstart**: Event-based init system introduced by Ubuntu, faster than SysVinit.
* **systemd**: Modern standard init system offering parallel service execution, fast boot times, and managed via systemctl.

### Why systemd is Important
* Faster boot speeds.
* Simplified system and service management.
* Integrated logging and resource monitoring (journalctl).

## 6. Linux Process States
* **Running (R)**: Process is actively executing or ready to execute on CPU.
  * Example: Running browser applications.
* **Sleeping (S)**: Process is waiting for an event or input/output (e.g., disk read, network data).
  * Example: `cat` command waiting for input.
* **Zombie (Z)**: Process has completed execution, but its exit status has not been collected by the parent process.
  * Command to check: `ps aux | grep Z`
EOF

# 3. Stage the newly created file for commit
git add day2-notes.md

# 4. Commit the file with a descriptive message
git commit -m "Add Day 2 DevOps Linux commands and fundamentals"

# 5. Rename default branch to main
git branch -M main

# 6. Connect your local repository to your remote GitHub repo
# (Replace YOUR_USERNAME and YOUR_REPO with your actual GitHub details)
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git

