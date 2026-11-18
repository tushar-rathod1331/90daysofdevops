## Introduction
The Linux File System Hierarchy organizes all files and directories in a structured way. Every file and directory starts from the root directory (`/`).

---

## Core Directories

### 1. `/` — Root Directory
* It is the starting point of the Linux file system.
* All files and directories are located under `/`.
* **Command:**
  ```bash
  ls -l /
  ```
* **Example items:** `home`, `var`, `etc`, `tmp`
* **I would use this when:** I want to view the main structure of the Linux system.

### 2. `/home` — User Home Directory
* Stores personal files and folders of normal users.
* Each user has a separate home directory.
* **Command:**
  ```bash
  ls -l /home
  ```
* **Example items:** `ubuntu`, `user`
* **I would use this when:** I want to access or manage user files.

### 3. `/root` — Root User Directory
* It is the home directory of the root administrator.
* Stores files and settings belonging to the root user.
* **Command:**
  ```bash
  ls -l /root
  ```
* **Example items:** `.bashrc`, `.profile`
* **I would use this when:** I need to access root administrator files.

### 4. `/etc` — Configuration Directory
* Contains system-wide configuration files.
* Used to configure services, networking, and system settings.
* **Command:**
  ```bash
  ls -l /etc
  ```
* **Example items:** `hostname`, `hosts`, `ssh`
* **I would use this when:** I want to configure Linux service or system settings.

### 5. `/var/log` — Log Directory
* Stores system and application log files.
* Helps DevOps engineers troubleshoot errors and monitor services.
* **Command:**
  ```bash
  ls -l /var/log
  ```
* **Example items:** `syslog`, `auth.log`, `apt`
* **I would use this when:** I want to investigate errors or check application and system logs.

### 6. `/tmp` — Temporary Directory
* Stores temporary files created by applications and users.
* Files may be automatically deleted after some time or during reboot.
* **Command:**
  ```bash
  ls -l /tmp
  ```
* **Example items:** Temporary files and folders
* **I would use this when:** I want to create temporary files during testing or troubleshooting.

---

## Additional Directories

### 7. `/bin` — Essential Commands
* Contains essential command-line programs.
* Used for basic system operation.
* **Command:**
  ```bash
  ls -l /bin
  ```
* **I would use this when:** I want to run basic Linux commands.

### 8. `/usr/bin` — User Commands
* Contains many executable programs and user commands.
* Includes utilities and application commands.
* **Command:**
  ```bash
  ls -l /usr/bin
  ```
* **Example items:** `git`, `python3`, `vim`
* **I would use this when:** I want to execute installed applications and utilities.

### 9. `/opt` — Optional Applications
* Used for installing optional or third-party software.
* Applications may have their own directories inside `/opt`.
* **Command:**
  ```bash
  ls -l /opt
  ```
* **Example items:** Third-party application folders
* **I would use this when:** I want to install or manage additional software.
```
````[cite: 7, 8, 9]
