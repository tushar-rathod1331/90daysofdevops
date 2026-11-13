# Linux & Networking Basics Notes (Day 3)

## 1. File & Directory Commands
1. `pwd` - Print working directory
2. `ls` - List files and directories
3. `cd` - Change directory
4. `mkdir` - Make directory
5. `rmdir` - Remove empty directory
6. `touch` - Create empty file
7. `cp file1 file2` - Copy file1 to file2
8. `mv file1 file2` - Move file or rename file
9. `rm` - Delete file
10. `cat` - View file content
11. `less` - Read file page by page
12. `head` - Show first lines of a file
13. `tail` - Show last lines of a file
14. `grep "word" file.txt` - Search for a specific word in a file
15. `find / -name file.txt` - Search and find files across system
16. `ps` - Show running processes
17. `top` - Live process monitoring
18. `kill PID` - Stop a running process
19. `chmod +x file.sh` - Change file execution permissions
20. `sudo command` - Run command with administrative privileges

---

## 2. Remote Server Access
- `ssh user@ip` - Remote server login

---

## 3. Process Management in Linux
1. `ps aux` - Check all running processes
2. `top` - Real-time process monitor
3. `htop` - Improved process viewer (if installed)
4. `ps aux | grep nginx` - Find specific running process
5. `pstree` - Show process tree hierarchy
6. `kill PID` - Stop process by ID
7. `kill -9 PID` - Force stop process
8. `firefox &` - Run process in background
9. `jobs` - List background jobs
10. `fg` - Bring background process to foreground
11. `systemctl status ssh` - Check service process status
12. `sudo systemctl start ssh` / `sudo systemctl stop ssh` - Start or stop a service

---

## 4. Linux File System Structure
- `/` - Root directory (top level)
- `/home` - User files and folders
- `/etc` - System configuration files
- `/bin` - Essential user commands
- `/var` - Logs and changing data
- `/tmp` - Temporary files
- `/usr` - User applications and programs
- `/dev` - Device files
- `/boot` - Bootloader and Kernel files

---

# 5. Networking Troubleshooting in Linux
*Networking troubleshooting means checking and fixing network problems such as no internet, DNS issues, connection failures, or blocked ports.

1. `ip a` - Check IP address
2. `ping google.com` - Check internet connectivity
3. `ip route` - Check routing table
4. `ss -tuln` - Display open ports and listening services
5. `dig google.com` - Check DNS resolution
6. `traceroute google.com` - Trace network path[cite: 6]
7. `netstat -tulnp` - Check active network connections[cite: 6]

## Daily-Use Networking Commands Summary:
`ip a`, `ping`, `ss`, `nslookup`, `traceroute`, `ssh`, `netstat`, `wget`

# Linux Troubleshooting Practice

## Scenario
Application running slowly on Ubuntu.

## Commands Used

1. uname -a - Check system information
2. ps aux - Check running processes
3. top - Monitor CPU usage
4. free -h - Check memory
5. df -h - Check disk space
6. systemctl status nginx - Check service
7. journalctl -u nginx -n 50 - Check logs
8. ping -c 4 google.com - Check network

## Conclusion
Used Linux commands to check processes,
CPU, memory, disk, services and logs.
