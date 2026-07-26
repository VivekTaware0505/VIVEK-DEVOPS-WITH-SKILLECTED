Introduction Linux 

What is Linux 
Linux is a free, open-source operating system kernel created by linus Torvalds in 1991
an operating system is software that acts as a bridge between the user and the computer hardware
linux is used in 
Servers 
cloud computing
web Hosting 
Android 
supercomputers
embedded systems
IOT devices
Devops platforms



What is an Operating System?
An Operating System manages:

CPU
Memory (RAM)
Storage
Files
Users
Hardware Devices
Running Applications

Without an operating system, a computer cannot be used effectively.

Simple Linux Architecture
+----------------------+
|      User            |
+----------------------+
          |
+----------------------+
|      Shell           |
+----------------------+
          |
+----------------------+
|      Kernel          |
+----------------------+
          |
+----------------------+
|      Hardware        |
+----------------------+


History of Linux
| Year  | Event                                              |
| ----- | -------------------------------------------------- |
| 1969  | Unix operating system developed                    |
| 1991  | Linus Torvalds created the Linux kernel            |
| 1992  | Linux released under the GNU GPL license           |
| 1993  | Debian distribution released                       |
| 1994  | Red Hat Linux introduced                           |
| 2004  | Ubuntu released                                    |
| Today | Linux powers most cloud servers and supercomputers |



What is the Kernel?

The Kernel is the core component of the operating system.

It is responsible for:

Managing CPU
Managing Memory
Managing Hardware
Managing Processes
Managing File Systems
Managing Devices

Think of the kernel as the manager of the entire operating system.
What is the Shell?
The Shell is a command-line interface that allows users to communicate with the kernel.
Popular Linux shells include:
Bash (Bourne Again Shell)
Zsh
Fish
Ksh

Example command:
pwd
The shell sends this command to the kernel, which performs the requested action and returns the result.



Linux Distributions (Distros)
A Linux distribution combines the Linux kernel with system utilities, package managers, and applications.

Common distributions:
| Distribution                    | Common Use                |
| ------------------------------- | ------------------------- |
| Ubuntu                          | Beginners, Servers, Cloud |
| Debian                          | Stable Servers            |
| Red Hat Enterprise Linux (RHEL) | Enterprise Environments   |
| Rocky Linux                     | RHEL-compatible           |
| AlmaLinux                       | RHEL-compatible           |
| Fedora                          | Latest Linux Technologies |
| Kali Linux                      | Security Testing          |
| Arch Linux                      | Advanced Users            |
| openSUSE                        | Desktop and Enterprise    |


Linux vs Windows
| Feature               | Linux                  | Windows                 |
| --------------------- | ---------------------- | ----------------------- |
| Cost                  | Free                   | Usually Paid            |
| Source Code           | Open Source            | Closed Source           |
| Security              | High                   | Good                    |
| Customization         | Extensive              | Limited                 |
| Software Installation | Package Managers       | Installers (.exe/.msi)  |
| Common Usage          | Servers, Cloud, DevOps | Desktop, Gaming, Office |



Why Linux is Important for DevOps

Most DevOps tools run on Linux, including:

Docker
Kubernetes
Jenkins
Nginx
Apache
Git
Ansible
Terraform

Major cloud platforms like AWS, Azure, and Google Cloud primarily use Linux-based servers.





Basic Linux Commands
Display Current Directory
pwd
Display Current User
whoami
Display Current Date and Time
date
Display Calendar
cal

If cal is not installed:

sudo apt update
sudo apt install ncal
Display Linux Kernel Information
uname

Detailed information:

uname -a
Display Operating System Information
cat /etc/os-release



Interview Questions
What is Linux?
Who created Linux?
What is the Linux Kernel?
What is a Shell?
What is a Linux distribution?
Name five popular Linux distributions.
Why is Linux widely used in DevOps?
What is the difference between Linux and Windows?
What command displays the current user?
What command displays kernel information?
