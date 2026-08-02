Why are File Permissions Important?

  Linux is a multi-user operating system.
  Different users have different responsibilities.

Example:

Developer → Can modify source code.
Tester → Can only read files.
System Administrator → Has full access.
Normal User → Limited permissions.

Permissions help protect the system from unauthorized access.

File Permission Structure
ls -l

-rwxr-xr--
│││ │ │
│││ │ └── Others
│││ └──── Group
│└─────── Owner
└──────── File Type


File Types
| Symbol | Meaning          |
| ------ | ---------------- |
| `-`    | Regular File     |
| `d`    | Directory        |
| `l`    | Symbolic Link    |
| `c`    | Character Device |
| `b`    | Block Device     |


Permission Types 
| Symbol | Meaning       | Value |
| ------ | ------------- | ----: |
| `r`    | Read          |     4 |
| `w`    | Write         |     2 |
| `x`    | Execute       |     1 |
| `-`    | No Permission |     0 |




Permission Classes

Linux divides permissions into three categories.
| User Type  | Description                   |
| ---------- | ----------------------------- |
| Owner (u)  | File creator/owner            |
| Group (g)  | Members of the assigned group |
| Others (o) | Everyone else                 |


Meaning:

Owner → Read, Write, Execute
Group → Read, Execute
Others → Read only



Numeric (Octal) Permissions
| Number | Permission  |
| -----: | ----------- |
|      7 | rwx (4+2+1) |
|      6 | rw- (4+2)   |
|      5 | r-x (4+1)   |
|      4 | r--         |
|      3 | -wx         |
|      2 | -w-         |
|      1 | --x         |
|      0 | ---         |



Examples:

chmod 755 script.sh
chmod 644 notes.txt
chmod 700 secret.sh



Meaning:

755
Owner  → rwx
Group  → r-x
Others → r-x
644
Owner  → rw-
Group  → r--
Others → r--
700
Owner  → rwx
Group  → ---
Others → ---




Symbolic Permissions
Add execute permission:

chmod +x script.sh

Remove write permission:

chmod -w notes.txt

Add read permission for group:

chmod g+r notes.txt

Give owner all permissions:

chmod u+rwx file.txt

Remove execute from others:

chmod o-x script.sh



Changing File Ownership
Change owner:

sudo chown vivek file.txt

Change owner and group:

sudo chown vivek:developers file.txt



Changing Group
sudo chgrp developers file.txt




View Current User
whoami
View Groups
groups


Default Permissions

Create a file:

touch demo.txt
ls -l demo.txt

Create a directory:

mkdir demo
ls -ld demo

Observe the default permissions assigned by Linux.

Real DevOps Examples
Make a deployment script executable
chmod +x deploy.sh
Restrict a private key
chmod 600 id_rsa

SSH will often refuse to use a private key if it's too permissive.










Allow everyone to execute a script
chmod 755 deploy.sh
Change ownership of a project
sudo chown -R vivek:developers Project/

-R means recursive (apply to all files and subdirectories).
















Interview Questions
What are Linux file permissions?
What do r, w, and x represent?
What is the difference between 644 and 755?
What does chmod do?
What does chown do?
What does chgrp do?
What is the difference between owner, group, and others?
Why is chmod 600 used for SSH private keys?
What does chmod +x do?
What does the -R option do with chown?
Key Learnings
Understood Linux permission model.
Learned symbolic and numeric permissions.
Changed file permissions using chmod.
Changed ownership using chown.
Changed groups using chgrp.
Practiced real DevOps permission management.
