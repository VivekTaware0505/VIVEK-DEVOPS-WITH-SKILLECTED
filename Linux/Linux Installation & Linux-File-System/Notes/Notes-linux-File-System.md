What is a Linux File System?

The Linux File System is the way Linux stores and organizes files and directories.

Unlike Windows, Linux has only one root directory (/). Every file, directory, disk, USB drive, and partition is attached somewhere under this single root.

Example:
/
├── bin
├── boot
├── dev
├── etc
├── home
├── lib
├── media
├── mnt
├── opt
├── proc
├── root
├── run
├── sbin
├── srv
├── sys
├── tmp
├── usr
└── var


Linux Directory Hierarchy
                  /
          (Root Directory)
                 │
 ┌──────┬──────┬──────┬──────┬──────┐
 │      │      │      │      │
bin    etc    home   var    usr
 │
Applications  
Everything starts from the Root Directory (/).






Important Directories
1️⃣ / (Root Directory)

The top-most directory.

Every file and folder exists inside it.

Example:

ls /
2️⃣ /home

Stores personal files of users.

Example:

/home/vivek

Usually contains:

Documents
Downloads
Desktop
Pictures
Videos

Command:

cd /home
3️⃣ /root

Home directory of the root (administrator) user.

Example:

/root

Normal users cannot access it without appropriate permissions.

4️⃣ /bin

Contains essential user commands.

Examples:

ls
cp
mv
pwd
cat

Check:

ls /bin
5️⃣ /sbin

Contains important system administration commands.

Examples:

fsck
reboot
shutdown
6️⃣ /etc

Contains system configuration files.

Examples:

/etc/passwd
/etc/hostname
/etc/hosts
/etc/os-release

View:

ls /etc
7️⃣ /usr

Stores installed applications, libraries, and documentation.

Common subdirectories:

/usr/bin
/usr/lib
/usr/share
8️⃣ /var

Stores data that changes frequently.

Examples:

Log files
Cache
Mail
Print queue

Common location:

/var/log
9️⃣ /tmp

Stores temporary files.

Files here may be deleted automatically after reboot.

Example:

cd /tmp
🔟 /boot

Contains files required to start Linux.

Includes:

Linux Kernel
GRUB Bootloader files
1️⃣1️⃣ /dev

Contains device files.

Examples:

/dev/sda
/dev/null
/dev/tty

Linux treats hardware devices as files.

1️⃣2️⃣ /proc

A virtual file system providing information about the running kernel and processes.

Examples:

/proc/cpuinfo
/proc/meminfo

View CPU details:

cat /proc/cpuinfo
1️⃣3️⃣ /sys

Contains information about hardware and kernel devices.

Mainly used by the kernel and system tools.

1️⃣4️⃣ /media

Used to automatically mount removable devices.

Examples:

USB drives
DVDs
1️⃣5️⃣ /mnt

Used for manually mounting file systems.

Example:

sudo mount /dev/sdb1 /mnt



Absolute Path vs Relative Path
| Absolute Path                    | Relative Path                 |
| -------------------------------- | ----------------------------- |
| Starts from `/`                  | Starts from current directory |
| Example: `/home/vivek/Documents` | Example: `Documents`          |


Example:

cd /home/vivek/Documents

Relative:

cd Documents
Navigation Commands

Current directory:

pwd

List files:

ls

Change directory:

cd

Go to home:

cd ~

Go to root:

cd /

Go back one directory:

cd ..

Go to previous directory:

cd -


Interview Questions
What is the Linux File System?
What is the root directory?
What is stored in /home?
What is the difference between /home and /root?
What is the purpose of /etc?
Why is /var important?
What is /proc?
What is the difference between /media and /mnt?
What is an absolute path?
What is a relative path?




Key Learnings
Learned the Linux File System hierarchy.
Understood the purpose of major directories.
Learned absolute and relative paths.
Practiced navigation commands.
Explored virtual file systems like /proc.
