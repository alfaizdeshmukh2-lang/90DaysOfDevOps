<h1>RUN BOOK FOR SSH SERVICE</h1> 

<H2>Environment basics </H2>

* Command : `uname -a`

OUTPUT: `Linux LAPTOP-L7BUS1JF 6.6.87.2-microsoft-standard-WSL2 #1 SMP PREEMPT_DYNAMIC Thu Jun  5 18:30:46 UTC 2025 x86_64 x86_64 x86_64 GNU/Linux`
* COMMAND NAME :- `lsb_release -a`

OUTPUT :-
```No LSB modules are available.
Distributor ID: Ubuntu
Description:    Ubuntu 24.04.3 LTS
Release:        24.04
Codename:       noble
```
## Filesystem sanity

* Command :- mkdir /tmp/runbook-demo

Observation :-Directory created successfully

* Command :- cp /etc/hosts /tmp/runbook-demo/hosts-copy && ls -l /tmp/runbook-demo

Observation : Copy host file and list down permission.

## CPU / Memory 

`top = real-time system monitoring tool`

`htop = Interactive process viewer for Linux.`

## Disk / IO

* df -h :df = Disk Filesystem
```
  Filesystem      Size  Used Avail Use% Mounted on
none            1.9G     0  1.9G   0% /usr/lib/modules/6.6.87.2-microsoft-standard-WSL2
none            1.9G  4.0K  1.9G   1% /mnt/wsl
drivers         231G  138G   94G  60% /usr/lib/wsl/drivers
/dev/sdd       1007G  2.0G  954G   1% /
none            1.9G  100K  1.9G   1% /mnt/wslg
none            1.9G     0  1.9G   0% /usr/lib/wsl/lib
rootfs          1.9G  2.7M  1.9G   1% /init
none            1.9G  540K  1.9G   1% /run
```

* du -sh /var/log 
```
du = Disk Usage (directory size)
-s = summary (only total size)
-h = human-readable (MB/GB)
```

## Network 

* ss -tulpn 
```
ss = Socket Statistics
It shows network connections and listening ports.

Options meaning:

-t → TCP connections

-u → UDP connections

-l → Listening ports only

-p → Show process using the port

-n → Show numeric ports (don’t resolve names)
```

* curl -I http://localhost
```
curl = Command-line tool to make HTTP requests
-I = Fetch only HTTP headers (not full page)
```

* Logs

* journalctl -u <service> -n 50
* Ex : journalctl -u ssh -n 50
```
journalctl = Tool to read systemd logs

-u <service> → Show logs for a specific service
-n 50 → Show last 50 lines only
```
