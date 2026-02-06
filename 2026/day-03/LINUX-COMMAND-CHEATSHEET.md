## Process Management Commands (Linux)

| Command | Description | Example |
|--------|-------------|---------|
| ps | Displays information about running processes | ps aux |
| top | Shows real-time CPU, memory, and process usage | top |
| htop | Interactive process viewer (if installed) | htop |
| kill | Terminates a process using PID | kill 1234 |
| killall | Terminates processes by name | killall firefox |
| jobs | Shows background jobs in current shell | jobs |
| bg | Runs a stopped job in background | bg %1 |
| fg | Brings background job to foreground | fg %1 |
| nohup | Runs a process even after logout | nohup script.sh & |
| nice | Starts a process with priority | nice -n 10 command |
| renice | Changes priority of running process | renice 10 -p 1234 |
| pgrep | Finds process ID by name | pgrep ssh |
| pkill | Kills process by name | pkill nginx |


## Linux File System Commands

| Command | Purpose | Example |
|---------|---------|---------|
| pwd | Show present working directory | pwd |
| ls | List files and directories | ls -l |
| cd | Change directory | cd /home/user |
| mkdir | Create directory | mkdir testdir |
| rmdir | Remove empty directory | rmdir testdir |
| touch | Create empty file | touch file.txt |
| cp | Copy files or directories | cp file.txt backup.txt |
| mv | Move or rename files | mv file.txt newfile.txt |
| rm | Delete files or directories | rm file.txt |
| rm -r | Delete directory with contents | rm -r mydir |
| cat | View file content | cat file.txt |
| less | View large files page by page | less file.txt |
| head | Show first lines of file | head file.txt |
| tail | Show last lines of file | tail file.txt |
| df -h | Show disk usage | df -h |
| du -sh | Show directory size | du -sh folder |
| find | Search files | find /home -name file.txt |
| locate | Quickly find files | locate file.txt |
| chmod | Change file permissions | chmod 755 script.sh |
| chown | Change file owner | chown user file.txt |

## Linux Network Troubleshooting Commands

| Command | Purpose | Example |
|---------|---------|---------|
| ping | Check connectivity to a host | ping google.com |
| ip a | Show IP address and interfaces | ip a |
| ip r | Show routing table | ip r |
| ifconfig | Show network interfaces (older command) | ifconfig |
| netstat -tuln | Show listening ports | netstat -tuln |
| ss -tuln | Show listening ports (modern alternative) | ss -tuln |
| traceroute | Show route to destination | traceroute google.com |
| tracepath | Similar to traceroute (no root needed) | tracepath google.com |
| nslookup | Check DNS resolution | nslookup google.com |
| dig | Detailed DNS lookup | dig google.com |
| host | Simple DNS lookup | host google.com |
| curl | Test HTTP/HTTPS connectivity | curl http://example.com |
| wget | Download and test connectivity | wget http://example.com |
| arp -a | Show ARP table | arp -a |
| route -n | Show routing table (older) | route -n |
| mtr | Network diagnostic (ping + traceroute) | mtr google.com |
| tcpdump | Capture network packets | tcpdump -i eth0 |
| nmap | Scan open ports | nmap localhost |
