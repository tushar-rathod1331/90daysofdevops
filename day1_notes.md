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
