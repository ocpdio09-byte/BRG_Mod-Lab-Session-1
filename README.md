# Bridging Modules Labs
## Student Information ## 
Student Name : LEE WEI HANG\
Kaplan Student ID : CT0381772\
Murdoch Student ID : 36060222

---

# Session 1 
## Session 1a - Setting Up Linux ##
* Successfully installed VirtualBox as VirtualMachine
* VirtualBox - https://www.virtualbox.org/
* Downloaded ubuntu-24.04.4-desktop-amd64
* Ubuntu - https://ubuntu.com/download/desktop
* config VM with 8192MB Base Memory and 2 Processors core
* Succesfully booted and ran Ubuntu on VirtualBox

## Session 1a - Basic command line navigation and utilities.
- `pwd` - prints current working directorys
  - helps to show output of the current path
  - Exmaple : `/home/ubuntu`

- `ls` - list files and directory 
  - Shows all current path directory content
  - Examples:
    - `ls` -> to show basic lsiting
    - `ls -a` -> show all entires including hidden files
    - `ls -l` -> used a long list format showing all detailed information
  - Writting in `ls -al` allows to show all hidden files with their detailed information

- `cd` - Changes directory or Directory Navigation
  - Goes to a specific Directory
  - Examples:
    - `cd Documents` -> goes to Documents directory
    - `cd ..` -> return to prev directory
    - `cd ~` -> return to home directory (e.g `/home/ubuntu`)

- `mkdir` - Creates a new directory
  - Examples:
    - `mkdir dlr1` -> creates a new directory name dlr1
 
- `touch` - Create an empty file
  - Examples
    - `touch test` -> create test file(empty)
    
- `man` - shows manual
  - Examples
    - `man ls` -> shows manual of ls
    - `man man` -> shows manual of manual
    
- `mv` - move a file or directory
  - Examples:
    - `mv test dlr1` -> move test file into dlr1
    - `mv dlr1/test /home/ubuntu` -> move test file from dlr1 to /home/ubuntu
      
- `/` - root directory also known as base of the file
  - Basically to include it infront of a directory and use cd to access it.

- `ping` - Check connection
  - `ping www.google.com` - continuously check connection with google

- `echo` - display text
  -`echo "Hello World" > text.txt` - pipe text "Hello World" into text directory
  
## Session 1b: Exploring Linux ##
# Session 1b : Linux Services
- `systemctl list-units --type=service` - List active running services
  -Display all Current running services
- `systemctl list-units --type=service --all` - List All services
  -shows all services including inactive and failed
- `sudo apt install openssh-server` - installing of SSH server to listen
- `sudo systemctl start ssh` - Manually Start SSH services
- `sydo systemctl stop SSH` - Manually Stop SSH services
- `sudo systemctl status ssh` - show SSH service status
  - Shows specifically whether it is
  - active (Running as normal)
  - inactive (Dead)
  - failed (Encountered an error) 
- `systemctl list-units --type=service | grep ssh` - Pick a specific service
- `sudo systemctl enable SSH` - Starts SSH services automatically on boot
- `systemctl list-unit-files --type=service` - shows all enabled services

# Session 1b : Linux Searching Filesystems
- Creating files for searching.
  - `mkdir lab1b` -> Creates a diretory
  - `touch file.txt file2.txt notes.log` -> creates 3 empty files for future uses.
  - `echo "Hello World" > file1.txt` -> pipe text into .txt file
  - `echo "This is Lab 1 B" > file2.txt` -> pipe text into .txt file
  - `echo "Error" > notes.log` -> pipe text into .log file to show error later.
-`find [path] -name "filename` -> find function to find a path of A specific file
  -`. -name "file.txt"` -> shows file1.txt path
  -`. -name "*.txt"` -> shows all .txt file path
  -`. -type d` -> shows directories
-`grep` -> search inside the files
  -`grep "Lab" file2.txt` -> prints line and highlight the search text inside the file
  -`grep -i "LAB" file2.txt` -> same as previopus byt case insensitive search
  -`grep "Hello *` -> case sensitive search shows file name and highkighted text inside
  -`grep -r "Error"` -> perform a recursive search through all files and display case sensitive
-Combitionation uses of grep and find
  -`find . -name "*.txt" -exec grep "Lab" {} \;`
    -Searches all the txt file and execlude the file that contains the word Lab.

# Session 1b : Permission
---

## Session 2 ##
