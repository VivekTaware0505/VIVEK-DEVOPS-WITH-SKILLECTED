Why Install Linux?

Linux is the operating system used by most:

Cloud servers
AWS EC2 instances
Docker containers
Kubernetes nodes
Web servers
CI/CD servers

Learning Linux on your own computer prepares you for real production environments.


Different Ways to Install Linux
1. Virtual Machine (Recommended for Beginners)

Examples:

Oracle VirtualBox
VMware Workstation

Advantages:

Safe to experiment.
No changes to your Windows installation.
Easy to take snapshots and restore.

Disadvantages:

Requires more RAM and storage.
Slightly slower than a native installation.
2. Windows Subsystem for Linux (WSL)

WSL allows Linux to run inside Windows without a virtual machine.

Advantages:

Fast.
Easy installation.
Excellent integration with VS Code and Git.

Disadvantages:

Some hardware-related features are limited.
3. Dual Boot

Install Linux alongside Windows.

Advantages:

Full hardware performance.
Suitable for daily Linux use.

Disadvantages:

Disk partitioning is required.
Boot configuration is more complex.
4. Physical Installation

Linux replaces the existing operating system.

Advantages:

Best performance.
Direct access to hardware.

Disadvantages:

Removes the previous operating system unless backed up.
5. Cloud Installation (AWS EC2)

Launch a Linux server on AWS.

Advantages:

Real cloud environment.
Excellent for DevOps practice.
Accessible from anywhere using SSH.


Popular Linux Distributions
| Distribution | Best For                   |
| ------------ | -------------------------- |
| Ubuntu       | Beginners, Servers, DevOps |
| Debian       | Stability                  |
| Fedora       | Latest technologies        |
| Rocky Linux  | Enterprise                 |
| AlmaLinux    | Enterprise                 |
| Kali Linux   | Security Testing           |
| Arch Linux   | Advanced users             |



Minimum Ubuntu Requirements
| Resource | Recommended          |
| -------- | -------------------- |
| RAM      | 4 GB or more         |
| CPU      | Dual Core            |
| Storage  | 25 GB or more        |
| Internet | Required for updates |





Ubuntu Installation Steps (VirtualBox)
Download the Ubuntu ISO.
Install VirtualBox.
Create a new virtual machine.
Allocate RAM (4 GB or more).
Create a virtual hard disk (25 GB or more).
Mount the Ubuntu ISO.
Start the VM.
Follow the installation wizard.
Create a username and password.
Restart the VM after installation.
Ubuntu Installation Steps (WSL)

Enable WSL:

wsl --install

Restart Windows.

List available distributions:

wsl --list --online

Install Ubuntu:

wsl --install -d Ubuntu

Check installed distributions:

wsl --list
AWS EC2 Linux Installation
Sign in to AWS.
Open the EC2 Console.
Launch a new EC2 instance.
Choose Ubuntu Server.
Select an instance type (e.g., t2.micro or t3.micro).
Create or select a key pair.
Configure the security group (allow SSH on port 22).
Launch the instance.
Connect using SSH.

Example:

ssh -i mykey.pem ubuntu@<public-ip>
Verify Installation

Check the operating system:

cat /etc/os-release

Check the kernel version:

uname -r

Check the hostname:

hostname

Check logged-in user:

whoami
Essential Commands

Update package information:

sudo apt update

Upgrade installed packages:

sudo apt upgrade

Check disk usage:

df -h

Check memory usage:

free -h

Check IP address:

ip addr




# My Notes

- Ubuntu is beginner-friendly and widely used in DevOps.
- WSL is useful for Windows users.
- VirtualBox is ideal for learning safely.
- AWS EC2 provides real cloud Linux servers.
- Always update packages after installation.








Interview Questions
What are the different methods to install Linux?
What is WSL?
What is the difference between WSL and VirtualBox?
What are the advantages of using Ubuntu for DevOps?
What is an ISO image?
Why is SSH required for AWS EC2?
Which command checks disk usage?
Which command checks the operating system version?
What are the minimum hardware requirements for Ubuntu?
Why should you update packages after installation?








Key Learnings
Learned multiple Linux installation methods.
Compared VirtualBox, WSL, Dual Boot, Physical Installation, and AWS EC2.
Practiced verification commands.
Understood why Ubuntu is commonly used for DevOps.
