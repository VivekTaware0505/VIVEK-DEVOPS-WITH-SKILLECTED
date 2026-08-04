Process Management

What is a Process?

A Process is a program that is currently running.

Example:

When you execute:

firefox

Linux loads Firefox into memory and creates a process.

Examples of processes:

Bash
SSH
Docker
Nginx
MySQL
Jenkins


Program vs Process
| Program        | Process                 |
| -------------- | ----------------------- |
| Stored on disk | Running in memory       |
| Passive        | Active                  |
| Example: `vim` | `vim` currently running |


Process Life Cycle
New
 │
 ▼
Ready
 │
 ▼
Running
 │
 ├────────────┐
 ▼            ▼
Waiting     Terminated


Process ID (PID)

Every process has a unique Process ID (PID).


View current shell PID:

echo $$

Example Output:

2456




Parent Process ID (PPID)

Every process (except the first one) is created by another process.

View:

ps -ef



View Running Processes

Basic view:

ps

Detailed view:

ps -ef

User-friendly view:

ps aux

Example:

USER   PID  %CPU %MEM COMMAND
vivek 3245  0.3  1.2 bash



Real-Time Monitoring with top

Run:

top

Displays:

Running processes
CPU usage
Memory usage
Load average
Running users

Exit:

q
Better Monitoring with htop

Install:

sudo apt update
sudo apt install htop

Run:

htop

Advantages:

Colorful interface
Easy process navigation
Search feature
Better readability

Exit:

F10
Find a Process

Search using ps:

ps aux | grep ssh

Search by process name:

pgrep ssh
Foreground Process

Runs directly in the terminal.

Example:

nano notes.txt

The terminal remains occupied until you exit.

Background Process

Run in the background:

sleep 300 &

The & sends the process to the background.

View Background Jobs
jobs

Example Output:

[1]+ Running sleep 300 &
Bring Background Job to Foreground
fg %1
Send Foreground Job to Background

Press:

Ctrl + Z

Then:

bg
Kill a Process

Using PID:

kill 3245

Force kill:

kill -9 3245

-9 sends the SIGKILL signal.

Kill by Process Name
killall firefox

Or:

pkill firefox
Process Priority

View priority:

top

Start with lower priority:

nice -n 10 sleep 300

Change priority of a running process:

sudo renice 5 -p 3245
Run Even After Logout (nohup)
nohup python app.py &

Output is stored in:

nohup.out

Useful for:

Scripts
Servers
Long-running jobs



Signals
| Signal       | Description          |
| ------------ | -------------------- |
| SIGTERM (15) | Graceful termination |
| SIGKILL (9)  | Force kill           |
| SIGSTOP      | Pause process        |
| SIGCONT      | Resume process       |






Practical Lab

Run the following:

sleep 300 &
jobs
ps
ps -ef
ps aux
pgrep sleep
top
kill $(pgrep sleep)

Install htop:

sudo apt update
sudo apt install htop
htop

Create another process:

sleep 500 &
jobs
fg %1

Press:

Ctrl + Z

Then:

bg
Real DevOps Examples
Check if Nginx is running
ps aux | grep nginx
Stop a stuck application
kill -9 <PID>
Find Docker process
pgrep docker
Keep a deployment running after logout
nohup ./deploy.sh &
Monitor server resources
top

or

htop
Interview Questions
What is a process?
What is the difference between a program and a process?
What is a PID?
What is PPID?
What is the difference between foreground and background processes?
What does kill -9 do?
What is nohup used for?
What is the difference between kill, killall, and pkill?
What is nice?
What does top display?



Key Learnings
Learned the process lifecycle.
Viewed running processes.
Understood PID and PPID.
Managed foreground and background jobs.
Terminated processes safely.
Monitored CPU and memory usage.
Worked with process priorities.



# My Notes

- A process is a running program.
- Every process has a unique PID.
- `ps` shows running processes.
- `top` and `htop` monitor system performance.
- `kill` terminates a process using its PID.
- `killall` and `pkill` terminate by process name.
- `jobs`, `bg`, and `fg` manage background jobs.
- `nohup` keeps a process running after logout.
