What is Linux Architecture?

Linux Architecture refers to the overall design and internal structure of the Linux operating system.
It explains how different components of Linux communicate with each other to execute user commands and manage hardware resources.
Every Linux command you type goes through several layers before reaching the hardware.



Linux Architecture Diagram
                    USER
                      │
                      ▼
        +-------------------------+
        |     User Applications   |
        | (Chrome, VS Code, Git)  |
        +-------------------------+
                      │
                      ▼
        +-------------------------+
        |         Shell           |
        |   (Bash, Zsh, Fish)     |
        +-------------------------+
                      │
            System Calls (API)
                      │
                      ▼
        +-------------------------+
        |        Kernel           |
        +-------------------------+
        | Process Management      |
        | Memory Management       |
        | File System             |
        | Device Drivers          |
        | Networking              |
        | Security                |
        +-------------------------+
                      │
                      ▼
        +-------------------------+
        |       Hardware          |
        | CPU RAM Disk Network    |
        +-------------------------+



Components of Linux Architecture
1️⃣ User Applications
These are the programs you use every day.

Examples:

Firefox
Chrome
VS Code
Git
Docker
Jenkins

Applications cannot directly access hardware.
They request services from the kernel.


2️⃣ Shell

The Shell is the command interpreter.
It accepts commands from the user.

Example:

ls

The shell converts this command into system calls and sends them to the kernel.
Popular shells:

Bash
Zsh
Fish
Ksh



3️⃣ System Calls
System Calls act as the bridge between User Space and Kernel Space.

Example:
When you execute:

cat file.txt

The program requests the kernel to:
Open the file
Read the file
Display the contents

The kernel performs these tasks through system calls.
Common system calls:

open()
read()
write()
close()
fork()
exec()



4️⃣ Kernel
The Kernel is the heart of Linux.
Responsibilities:

Process Management
Memory Management
CPU Scheduling
Device Management
File System Management
Networking
Security

Without the kernel, Linux cannot function.
Kernel Components
Process Management

Controls:
Running programs
Scheduling
Creating processes
Terminating processes

Example command:

ps
Memory Management
Responsible for:

RAM allocation
Virtual memory
Swapping
Cache management

Example:
free -h
File System

Linux stores everything as files.
Examples:

/etc
/home
/var
/proc

Example command:

ls /
Device Drivers

Drivers allow Linux to communicate with hardware.

Examples:
Keyboard
Mouse
USB
Printer
Wi-Fi Adapter
Graphics Card
Networking

The kernel manages:
IP Addresses
TCP
UDP
Routing
Firewalls

Example:

ip addr
Security
Kernel security features include:


User permissions
File permissions
Authentication
Process isolation

User Space vs Kernel Space   
| User Space                            | Kernel Space                       |
| ------------------------------------- | ---------------------------------- |
| Runs applications                     | Runs the kernel                    |
| Limited hardware access               | Full hardware access               |
| Safer                                 | Highly privileged                  |
| Errors usually affect one application | Errors can affect the whole system |




Linux Boot Process (Overview)
Power ON
      │
      ▼
BIOS / UEFI
      │
      ▼
Bootloader (GRUB)
      │
      ▼
Linux Kernel
      │
      ▼
Systemd (Init System)
      │
      ▼
Login Screen / Terminal












Linux Commands

Display kernel information:

uname -r

Display architecture:

uname -m

Display CPU information:

lscpu

Display memory information:

free -h

Display block devices:

lsblk

Display running processes:

ps aux

Display system uptime:

uptime

Display logged-in users:

who





Interview Questions
What is Linux Architecture?
What is the role of the Kernel?
What is User Space?
What is Kernel Space?
What are System Calls?
What is the difference between Shell and Kernel?
What are Device Drivers?
Explain the Linux boot process.
What is Process Management?
What is Memory Management?




Key Learnings
Learned the internal architecture of Linux.
Understood the interaction between the user, shell, kernel, and hardware.
Learned the purpose of system calls.
Compared User Space and Kernel Space.
Practiced commands to inspect CPU, memory, storage, and processes.
