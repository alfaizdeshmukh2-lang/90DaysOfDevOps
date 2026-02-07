**Check running processes**

ps - report a snapshot of the current processes.
```
ubuntu@ip-172-31-33-44:~$ ps
    PID TTY          TIME CMD
   1676 pts/0    00:00:00 bash
   1889 pts/0    00:00:00 ps
ubuntu@ip-172-31-33-44:~$ 
```

top -  program  provides  a  dynamic  real-time  view of a running system.  It can display system summary information as well as a list of processes or
       threads currently being managed by the Linux kernel.  The types of system summary information shown and the types, order and size of information displayed
       for processes are all user configurable and that configuration can be made persistent across restarts.
```
top - 06:39:02 up 19 min,  1 user,  load average: 0.00, 0.02, 0.00
Tasks: 114 total,   1 running, 113 sleeping,   0 stopped,   0 zombie
%Cpu(s):  0.0 us,  0.0 sy,  0.0 ni,100.0 id,  0.0 wa,  0.0 hi,  0.0 si,  0.0 st 
MiB Mem :    914.2 total,     94.1 free,    409.8 used,    570.3 buff/cache     
MiB Swap:      0.0 total,      0.0 free,      0.0 used.    504.4 avail Mem 

    PID USER      PR  NI    VIRT    RES    SHR S  %CPU  %MEM     TIME+ COMMAND                                                                                        
      1 root      20   0   22212  13584   9604 S   0.0   1.5   0:01.28 systemd                                                                                        
      2 root      20   0       0      0      0 S   0.0   0.0   0:00.00 kthreadd                                                                                       
      3 root      20   0       0      0      0 S   0.0   0.0   0:00.00 pool_workqueue_release                                                                         
      4 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 kworker/R-rcu_gp                                                                               
      5 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 kworker/R-sync_wq                                                                              
      6 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 kworker/R-kvfree_rcu_reclaim                                                                   
      7 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 kworker/R-slub_flushwq                                                                         
      8 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 kworker/R-netns                                                                                
     10 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 kworker/0:0H-events_highpri                                                                    
     11 root      20   0       0      0      0 I   0.0   0.0   0:00.09 kworker/0:1-cgroup_destroy                                                                     
     12 root      20   0       0      0      0 I   0.0   0.0   0:00.19 kworker/u8:0-events_power_efficient                                                            
     13 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 kworker/R-mm_percpu_wq                                                                         
     14 root      20   0       0      0      0 I   0.0   0.0   0:00.00 rcu_tasks_rude_kthread                                                                         
     15 root      20   0       0      0      0 I   0.0   0.0   0:00.00 rcu_tasks_trace_kthread                                                                        
     16 root      20   0       0      0      0 S   0.0   0.0   0:00.04 ksoftirqd/0                                                                                    
     17 root      20   0       0      0      0 I   0.0   0.0   0:00.12 rcu_sched                                                                                      
     18 root      20   0       0      0      0 S   0.0   0.0   0:00.00 rcu_exp_par_gp_kthread_worker/0                                                                
     19 root      20   0       0      0      0 S   0.0   0.0   0:00.00 rcu_exp_gp_kthread_worker                                                                      
     20 root      rt   0       0      0      0 S   0.0   0.0   0:00.00 migration/0                                                                                    
     21 root     -51   0       0      0      0 S   0.0   0.0   0:00.00 idle_inject/0                                                                                  
     22 root      20   0       0      0      0 S   0.0   0.0   0:00.00 cpuhp/0                                                                                        
     23 root      20   0       0      0      0 S   0.0   0.0   0:00.00 cpuhp/1                                                                                        
     24 root     -51   0       0      0      0 S   0.0   0.0   0:00.00 idle_inject/1                                                                                  
     25 root      rt   0       0      0      0 S   0.0   0.0   0:00.06 migration/1                                                                                    
     26 root      20   0       0      0      0 S   0.0   0.0   0:00.03 ksoftirqd/1                                                                                    
     28 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 kworker/1:0H-events_highpri                                                                    
     29 root      20   0       0      0      0 S   0.0   0.0   0:00.00 kdevtmpfs                                                                                      
     30 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 kworker/R-inet_frag_wq                                                                         
     31 root      20   0       0      0      0 S   0.0   0.0   0:00.00 kauditd                                                                                        
     32 root      20   0       0      0      0 S   0.0   0.0   0:00.00 khungtaskd                                                                                     
     33 root      20   0       0      0      0 I   0.0   0.0   0:00.11 kworker/u8:1-events_power_efficient                                                            
ubuntu@ip-172-31-33-44:~$
```

pgrep--pkill, pidwait - look up, signal, or wait for processes based on name and other attributes

SYNOPSIS
       pgrep [options] pattern
       pkill [options] pattern
       pidwait [options] pattern

DESCRIPTION
       pgrep  looks  through  the  currently  running processes and lists the process IDs which match the selection criteria to stdout.  All the criteria have to
       match.  For example,

              $ pgrep -u root sshd

       will only list the processes called sshd AND owned by root.  On the other hand,

              $ pgrep -u root,daemon

       will list the processes owned by root OR daemon.

       pkill will send the specified signal (by default SIGTERM) to each process instead of listing them on stdout.

       pidwait will wait for each process instead of listing them on stdout.

Screen - This command is used to create a virtual terminal session that can be detact and reattached at any time.

**service Command**
```
ubuntu@ip-172-31-33-44:~$ systemctl status nginx
● nginx.service - A high performance web server and a reverse proxy server
     Loaded: loaded (/usr/lib/systemd/system/nginx.service; enabled; preset: enabled)
     Active: active (running) since Sat 2026-02-07 06:19:16 UTC; 39min ago
       Docs: man:nginx(8)
    Process: 548 ExecStartPre=/usr/sbin/nginx -t -q -g daemon on; master_process on; (code=exited, status=0/SUCCESS)
    Process: 568 ExecStart=/usr/sbin/nginx -g daemon on; master_process on; (code=exited, status=0/SUCCESS)
   Main PID: 576 (nginx)
      Tasks: 3 (limit: 1017)
     Memory: 3.5M (peak: 3.9M)
        CPU: 17ms
     CGroup: /system.slice/nginx.service
             ├─576 "nginx: master process /usr/sbin/nginx -g daemon on; master_process on;"
             ├─577 "nginx: worker process"
             └─578 "nginx: worker process"

Feb 07 06:19:16 ip-172-31-33-44 systemd[1]: Starting nginx.service - A high performance web server and a reverse proxy server...
Feb 07 06:19:16 ip-172-31-33-44 systemd[1]: Started nginx.service - A high performance web server and a reverse proxy server.
ubuntu@ip-172-31-33-44:~$
```

**systemctl list-units**
  ```
  UNIT                                                                         LOAD   ACTIVE SUB       DESCRIPTION                                                   >
  proc-sys-fs-binfmt_misc.automount                                            loaded active running   Arbitrary Executable File Formats File System Automount Point >
  sys-devices-pci0000:00-0000:00:04.0-nvme-nvme0-nvme0n1-nvme0n1p1.device      loaded active plugged   Amazon Elastic Block Store cloudimg-rootfs
  sys-devices-pci0000:00-0000:00:04.0-nvme-nvme0-nvme0n1-nvme0n1p14.device     loaded active plugged   Amazon Elastic Block Store 14
  sys-devices-pci0000:00-0000:00:04.0-nvme-nvme0-nvme0n1-nvme0n1p15.device     loaded active plugged   Amazon Elastic Block Store UEFI
  sys-devices-pci0000:00-0000:00:04.0-nvme-nvme0-nvme0n1-nvme0n1p16.device     loaded active plugged   Amazon Elastic Block Store BOOT

```
***inspect ssh service**
```
ubuntu@ip-172-31-33-44:~$ systemctl status ssh
● ssh.service - OpenBSD Secure Shell server
     Loaded: loaded (/usr/lib/systemd/system/ssh.service; disabled; preset: enabled)
    Drop-In: /usr/lib/systemd/system/ssh.service.d
             └─ec2-instance-connect.conf
     Active: active (running) since Sat 2026-02-07 06:20:32 UTC; 56min ago
TriggeredBy: ● ssh.socket
       Docs: man:sshd(8)
             man:sshd_config(5)
    Process: 1258 ExecStartPre=/usr/sbin/sshd -t (code=exited, status=0/SUCCESS)
   Main PID: 1260 (sshd)
      Tasks: 1 (limit: 1017)
     Memory: 5.9M (peak: 9.4M)
        CPU: 1.436s
     CGroup: /system.slice/ssh.service
             └─1260 "sshd: /usr/sbin/sshd -D -o AuthorizedKeysCommand /usr/share/ec2-instance-connect/eic_run_authorized_keys %u %f -o AuthorizedKeysCommandUser ec2->
```
