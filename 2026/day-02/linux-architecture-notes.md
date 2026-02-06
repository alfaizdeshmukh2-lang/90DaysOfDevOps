DAY-02 TASK
Today’s goal is to understand how Linux works under the hood.

short note explaination:

1)The core components of Linux (kernel, user space, init/systemd) Ans : a)Kernal:The kernal is the core part of an operating system. b)It acts as an bridge between hardware and the software. c)Without kernal application cant talk to hardware.

2)USER SPACE : User space is the restricted , protected memory area where all user application-like web browser, file manages, and terminal app-run.

3)a)init: init is the first process that starts after the Linux kernal boots - PID OF UNIT = 1 - IT starts all other services and process. - It contain system startup and shutdown. b) systemd : systemd is amodern replacement for init used in most linux distribation (UBUNTU , CENTOS , RHEL , AMAZON LINUX)

Process Creation and Management in Linux
1)How processes are created and managed. A process is a program that is currently running in memory. Each process has: 1.PID (Process ID) – unique number 2.PPID (Parent Process ID) – the process that started it 3.Memory, CPU time, and resources.

How Processes Are Created in Linux ans: Processes are mainly created using these system calls: fork() Creates a child process by copying the parent process. Child gets a new PID. exec() Loads a new program into the process memory. Often used after fork().

Process States in Linux a)A process can be in different states: b)Running (R) – currently executing c)Sleeping (S) – waiting for input d)Stopped (T) – paused e)Zombie (Z) – finished but not cleaned up

What is systemd?

Ans : systemd is the init system and service manager in modern Linux. It is the first process started by the kernel (PID 1).

What systemd Does ans:

Starts System Services Examples: -Networking -SSH -Logging

Manages Services -systemctl start nginx -systemctl stop nginx -systemctl restart nginx

Short Interview Answer

Process creation: In Linux, processes are created using fork() and exec(). The kernel manages them using scheduling, signals, and priorities.

systemd: systemd is the first process (PID 1) that starts all services, manages them, handles booting, logging, and dependencies.
