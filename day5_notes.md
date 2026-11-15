
## Day 5: File Creation, Redirection, and Reading

### Task
* Creating a file
* Writing text to a file
* Appending new lines
* Reading the file back

### Guidelines
* Create a file named `notes.txt`
* Write 3 lines into the file using redirection (`>` and `>>`)
* Use `cat` to read the full file
* Use `head` and `tail` to read part of the file
* Use `tee` once to write and display at the same time
* Keep it short (8–12 lines total in the file)

### Command Flow

1. **Create the file:**
   ```bash
   touch notes.txt
   ```
2. **Write the first line (overwrite/create):**
   ```bash
   echo "Line 1" > notes.txt
   ```
3. **Append the second line:**
   ```bash
   echo "Line 2" >> notes.txt
   ```
4. **Append the third line and display output simultaneously:**
   ```bash
   echo "Line 3" | tee -a notes.txt
   ```
5. **Read the full file:**
   ```bash
   cat notes.txt
   ```
6. **Read the first 2 lines:**
   ```bash
   head -n 2 notes.txt
   ```
7. **Read the last 2 lines:**
   ```bash
   tail -n 2 notes.txt

   
 ### Practical
 <img width="1600" height="785" alt="WhatsApp Image 2026-11-15 at 6 12 42 PM" src="https://github.com/user-attachments/assets/4a3165ed-615e-4660-9b61-33608b49b3ce" />

