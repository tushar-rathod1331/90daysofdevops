# Linux & Networking Basics Notes (Day 1)

## 1. How the Internet Works
- The Internet works using **Fiber cables**.

## 2. What is a Server?
- **Server:** Serves data.
- **Client:** Requests data to be sent.

## 3. Difference Between Web Server and Application Server
| Server Type | Function |
| :--- | :--- |
| **Web Server** | Serves static data |
| **Application Server** | Serves dynamic data |

## 4. Types of Applications
- **Standalone:** Functions without net (e.g., Feedback forms)
- **Web Application:** Requires net (e.g., Instagram)

## 5. Linux vs Windows
| Linux | Windows |
| :--- | :--- |
| Developing / Programming | Antivirus |
| Networking | Versions (XP, etc.) |
| No antivirus needed | |

## 6. Software / Remote Location Server Tools
1. **RDP:** Remote Desktop Protocol
2. **SSH:** Secure Shell

## 7. Kernel & Shell
- **Kernel:** Main part / brain of Linux.
- **Shell:** Acts as a gateway between the Kernel and the User.
- **Architecture Flow:** `User -> Shell -> Kernel`
  - Example command flow: `command [mkdir]` -> Shell -> Kernel -> Linux

---

## 8. Bootloader
- Loads the operating system into memory during startup.

## 9. Desktop Environment
- Provides the graphical interface (GUI) for the user.

## 10. Linux System Architecture
![Uploading linux architecture (2).png…]()




## 11. Hardware Information Commands
- **CPU Information & System Monitoring:**
  - `top`
  - `df -h`
  - `free`

## 12. Linux File System
- Starts from the **root folder** represented by `/`.
- **Directory Hierarchy:**
  ```text
  / (Root)
  ├── home
  ├── user
  ├── bin
  ├── etc
  └── var

  
# Linux Architecture – How Linux Works Under the Hood

## 1. Core Components of Linux

Linux operating system consists of three important components:

### A. Kernel
- The kernel is the core part of Linux.
- It acts as a bridge between software and hardware.
- It manages CPU, memory, devices, and processes.
- It controls communication between hardware and software.

### B. User Space
- User space is where users and applications work.
- It includes commands, shells, applications, and utilities.
- Users interact with Linux through the terminal or GUI.

Examples:
- ls
- pwd
- mkdir
- vim
- Bash

### C. Init / systemd
- Init is the first process started by the Linux kernel.
- Modern Linux distributions commonly use systemd.
- It starts and manages system services.
- It helps manage the boot process.

Example:
```bash
sudo systemctl start ssh
```

## 2. How Processes Are Created and Managed

A process is a program that is currently running in Linux.

### Process Creation Steps

1. A user runs a command.
2. The shell creates a child process using fork().
3. The child process uses exec() to run a new program.
4. The kernel allocates CPU and memory resources.
5. The process runs until it finishes or is terminated.

### Important Process Commands

| Command | Use |
|---|---|
| ps | Display running processes |
| top | Monitor processes in real time |
| pgrep | Find process IDs |
| kill | Send a signal to a process |
| pstree | Display process hierarchy |

### Practical Commands

```bash
ps aux
top
pgrep ssh
pstree
```

To stop a process:

```bash
kill PID
```

Replace PID with the actual process ID.

## 3. What Is systemd and Why Does It Matter?

systemd is the system and service manager used by many modern Linux distributions.

### Main Functions of systemd

1. Starts services during system boot.
2. Manages background services.
3. Starts and stops services.
4. Monitors system services.
5. Collects system logs through journald.
6. Manages system startup and shutdown.

### Important systemd Commands

| Command | Purpose |
|---|---|
| systemctl status ssh | Check SSH service status |
| sudo systemctl start ssh | Start SSH service |
| sudo systemctl stop ssh | Stop SSH service |
| sudo systemctl restart ssh | Restart SSH service |
| systemctl list-units --type=service | List service units |
| journalctl -u ssh | View SSH service logs |

## 4. Real-World Example

Suppose your Linux server restarts after a power failure.

1. The Linux kernel starts.
2. The kernel launches systemd (PID 1).
3. systemd starts required services.
4. SSH and other services become available.
5. Users connect to the server and run applications.
6. The kernel manages CPU, memory, and running processes.

This is how Linux works behind the scenes.

## 5. Practical Tasks – Run These Commands in Ubuntu

```bash
# Check kernel version
uname -r

# Check PID 1
ps -p 1 -f

# Check running processes
ps aux

# Monitor processes
top

# Check systemd services
systemctl list-units --type=service

# Check SSH service
systemctl status ssh

# View system logs
journalctl -n 20
```



