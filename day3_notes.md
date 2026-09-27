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
1. `ps aux` - Check all running processes[cite: 4]
2. `top` - Real-time process monitor[cite: 4]
3. `htop` - Improved process viewer (if installed)[cite: 4]
4. `ps aux | grep nginx` - Find specific running process[cite: 4]
5. `pstree` - Show process tree hierarchy[cite: 4]
6. `kill PID` - Stop process by ID[cite: 4]
7. `kill -9 PID` - Force stop process[cite: 4]
8. `firefox &` - Run process in background[cite: 5]
9. `jobs` - List background jobs[cite: 5]
10. `fg` - Bring background process to foreground[cite: 5]
11. `systemctl status ssh` - Check service process status[cite: 5]
12. `sudo systemctl start ssh` / `sudo systemctl stop ssh` - Start or stop a service[cite: 5]

---

## 4. Linux File System Structure
- `/` - Root directory (top level)[cite: 5]
- `/home` - User files and folders[cite: 5]
- `/etc` - System configuration files[cite: 5]
- `/bin` - Essential user commands[cite: 5]
- `/var` - Logs and changing data[cite: 5]
- `/tmp` - Temporary files[cite: 5]
- `/usr` - User applications and programs[cite: 5]
- `/dev` - Device files[cite: 5]
- `/boot` - Bootloader and Kernel files[cite: 5]

---

## 5. Networking Troubleshooting in Linux
*Networking troubleshooting means checking and fixing network problems such as no internet, DNS issues, connection failures, or blocked ports.*[cite: 6]

### Common Commands:
1. `ip a` - Check IP address[cite: 6]
2. `ping google.com` - Check internet connectivity[cite: 6]
3. `ip route` - Check routing table[cite: 6]
4. `ss -tuln` - Display open ports and listening services[cite: 6]
5. `dig google.com` - Check DNS resolution[cite: 6]
6. `traceroute google.com` - Trace network path[cite: 6]
7. `netstat -tulnp` - Check active network connections[cite: 6]

### Daily-Use Networking Commands Summary:
`ip a`, `ping`, `ss`, `nslookup`, `traceroute`, `ssh`, `netstat`, `wget`[cite: 6]
