# linuxcomms
Basic Linux Commands
Find the processes running on a Linux machine:

ps aux / top

Find the users currently logged in:

who

Find the uptime of the machine:

uptime

Find the RAM usage:

free -h

Find the disk usage:

df -h

Find the inode usage:

df -hi

Find the ulimit of a user:

ulimit -a

Find the ulimit of a process (replace <pid> with the process ID):

cat /proc/3/limits (For process with pid 3)

Find the file descriptors used by a process (replace <pid> with the process ID):

ls -l /proc/3/fd (Avoiding critical processes)

Find the top 5 processes by memory usage:

ps aux --sort=-%mem | head -n 6

Find the top 5 processes by CPU usage:

ps aux --sort=-%cpu | head -n 6

Find the top 5 processes by network usage:

nethogs

Find the top 5 processes by disk I/O usage:

iotop

Find the network traffic and bandwidth usage of the machine:

iftop

Given a file as input, find the processes using that file:

lsof /harshit/home/documents/file.txt

List files opened by a process (replace <pid> with the process ID):

lsof -p 3

List processes listening on a specific port (replace 22 with the port number):

lsof -i :22

Find the status of a service (replace httpd with the service name)

systemctl status httpd

Find zombie processes on a machine:

ps aux | grep 'zo'

Find the environment variables set on a machine:

printenv

Display processes started by a user (replace <username> with the username):

ps -u harshit

Kill a process (replace <pid> with the process ID):

kill 3

List open ports:

netstat -tuln

Find the permissions set for a file (replace /path/to/your/file with the file path):

ls -l /harshit/home/documents/files.txt
