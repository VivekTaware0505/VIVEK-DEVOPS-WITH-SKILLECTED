Why Users & Groups Matter
Linux is a multi-user operating system.
Different people can use the same server with different permissions.


| User       | Role                  |
| ---------- | --------------------- |
| root       | System Administrator  |
| vivek      | DevOps Engineer       |
| developer1 | Application Developer |
| tester1    | QA Engineer           |


Using users and groups improves:

Security
Access control
Collaboration
Accountability


Types of Users
1. Root User
Superuser
User ID (UID): 0
Can access every file


Regular User
Example:

vivek

Regular users have limited permissions.


System Users
Created automatically for services.

Examples:

www-data
mysql
daemon
nobody

They run background services instead of allowing people to log in.
Can install software
Can create/delete users
Can change system settings


What is a Group?
A group is a collection of users.

Instead of assigning permissions to every user individually, you assign permissions to the group.
Example:

developers
├── vivek
├── rahul
└── priya


mportant Files
/etc/passwd

Stores user account information.

View:

cat /etc/passwd

Example:

vivek:x:1000:1000:Vivek:/home/vivek:/bin/bash
Username
Password Placeholder
UID
GID
Description
Home Directory
Login Shell








/etc/group

Stores group information.

View:

cat /etc/group
/etc/shadow

Stores encrypted passwords.

View (requires root):

sudo cat /etc/shadow
User IDs (UID)

Check your UID:

id

Example:

uid=1000(vivek)
gid=1000(vivek)
groups=1000(vivek),27(sudo)
Group IDs (GID)

Every group has a unique Group ID.

Display:

id
Create a User
sudo useradd john

Create home directory automatically:

sudo useradd -m john
Set Password
sudo passwd john
Switch User
su john

Return to previous user:

exit
Delete User

Delete user only:

sudo userdel john

Delete user and home directory:

sudo userdel -r john
Create a Group
sudo groupadd developers
Add User to Group
sudo usermod -aG developers john

Explanation:

-a → Append
-G → Supplementary group
View User Groups
groups

Or:

id
Change Primary Group
sudo usermod -g developers john
Lock User
sudo passwd -l john
Unlock User
sudo passwd -u john
Sudo

Instead of logging in as root, Linux allows trusted users to execute administrative commands using:

sudo

Example:

sudo apt update

Advantages:

Better security
Accountability
Reduced risk of accidental system damage
Real DevOps Examples

Create a deployment user:

sudo useradd -m deploy

Create a developers group:

sudo groupadd developers

Add the deployment user:

sudo usermod -aG developers deploy



Interview Questions
What is the difference between a user and a group?
What is the UID of the root user?
What is the purpose of /etc/passwd?
What is stored in /etc/shadow?
What is the difference between useradd and usermod?
How do you add a user to a group?
What does sudo do?
Why should you avoid logging in as root for daily work?
What command displays a user's UID and groups?
What is the difference between a primary group and a supplementary group?



Key Learnings
Learned different types of Linux users.
Understood groups and group management.
Created users and groups.
Added users to groups.
Managed passwords.
Learned how sudo provides administrative access.

Verify:

id deploy



