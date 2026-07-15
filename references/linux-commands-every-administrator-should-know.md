# 🐧 Linux Commands Every Administrator Should Know

> Practical Linux administration reference for everyday operations.

## 📖 Table of Contents

-   [🖥️ System Information](#️-system-information)
-   [📂 File & Directory Operations](#-file--directory-operations)
-   [👤 User Management](#-user-management)
-   [⚙️ Process Management](#️-process-management)
-   [🧠 CPU & Memory Monitoring](#-cpu--memory-monitoring)
-   [💾 Disk & Storage](#-disk--storage)
-   [🌐 Networking](#-networking)
-   [📜 Logs & Journals](#-logs--journals)
-   [🔥 Services (systemd)](#-services-systemd)
-   [🔐 Permissions](#-permissions)
-   [📦 Package Management](#-package-management)
-   [🔍 Search](#-search)
-   [🚀 Performance](#-performance)
-   [🛠️ Troubleshooting Workflow](#️-troubleshooting-workflow)

------------------------------------------------------------------------

# 🖥️ System Information

  Command         Description                  Common Use
  --------------- ---------------------------- ------------------------
  `hostnamectl`   Show hostname, OS & kernel   Verify server identity
  `hostname`      Current hostname             Confirm host name
  `uname -a`      Kernel details               Compatibility checks
  `uptime`        Uptime & load average        Check server health
  `date`          Current date/time            Verify system clock
  `timedatectl`   Time & NTP settings          Time synchronization
  `whoami`        Current user                 Verify account
  `id`            UID/GID                      Permission checks
  `lscpu`         CPU information              Hardware inspection
  `free -h`       Memory usage                 RAM availability

> \[!TIP\] Start every troubleshooting session with `hostnamectl`,
> `uptime`, and `free -h`.

# 📂 File & Directory Operations

  Command        Description          Common Use
  -------------- -------------------- ---------------------
  `pwd`          Current directory    Navigation
  `ls -lah`      Detailed listing     Inspect files
  `cd`           Change directory     Navigation
  `mkdir dir`    Create directory     Organize files
  `cp src dst`   Copy files           Backup configs
  `mv src dst`   Move/Rename          Rename files
  `rm -rf dir`   Delete recursively   Cleanup ⚠️
  `touch file`   Create file          New configs
  `tree`         Directory tree       Visualize structure

> \[!WARNING\] `rm -rf` permanently deletes data.

# 👤 User Management

  Command         Description       Common Use
  --------------- ----------------- -------------------
  `who`           Logged-in users   Audit sessions
  `w`             User activity     Active users
  `last`          Login history     Security review
  `useradd`       Create user       New accounts
  `passwd user`   Change password   Reset credentials
  `groups user`   User groups       Access review

# ⚙️ Process Management

  Command         Description           Common Use
  --------------- --------------------- --------------------
  `ps aux`        Running processes     Process inspection
  `htop`          Interactive monitor   CPU/RAM analysis
  `top`           Built-in monitor      Live usage
  `pgrep nginx`   Find PID              Service lookup
  `kill PID`      Stop process          Graceful stop
  `kill -9 PID`   Force stop            Hung process

### 📌 Example

``` bash
htop
```

> \[!NOTE\] Press **F6** inside `htop` to sort by CPU or Memory.

# 🧠 CPU & Memory Monitoring

  Command      Description      Common Use
  ------------ ---------------- ---------------------
  `free -h`    RAM usage        Memory check
  `vmstat 1`   CPU/Memory/I/O   Performance issues
  `mpstat`     CPU stats        CPU bottlenecks
  `iostat`     Disk I/O         Storage performance

# 💾 Disk & Storage

  Command      Description           Common Use
  ------------ --------------------- --------------------
  `df -h`      Filesystem usage      Disk space
  `du -sh *`   Directory sizes       Find large folders
  `lsblk`      Block devices         Storage inventory
  `mount`      Mounted filesystems   Verify mounts
  `fdisk -l`   Partition table       Disk inspection

# 🌐 Networking

  Command        Description       Common Use
  -------------- ----------------- ---------------------
  `ip addr`      IP addresses      Interface check
  `ip route`     Routing table     Routing issues
  `ss -tulnp`    Listening ports   Verify services
  `ping host`    Connectivity      Reachability
  `dig domain`   DNS lookup        DNS troubleshooting
  `curl URL`     HTTP requests     API testing
  `wget URL`     Download files    Retrieve packages

### 📌 Example

``` bash
ss -tulnp | grep :443
```

# 📜 Logs & Journals

  Command                 Description    Common Use
  ----------------------- -------------- -------------------------
  `journalctl`            System logs    General troubleshooting
  `journalctl -u nginx`   Service logs   Application errors
  `journalctl -f`         Follow logs    Live monitoring
  `dmesg`                 Kernel logs    Hardware issues

# 🔥 Services (systemd)

  Command                     Description       Common Use
  --------------------------- ----------------- ----------------
  `systemctl status nginx`    Service status    Verify service
  `systemctl restart nginx`   Restart service   Apply config
  `systemctl stop nginx`      Stop service      Maintenance
  `systemctl enable nginx`    Enable at boot    Persistence

# 🔐 Permissions

  Command                  Description           Common Use
  ------------------------ --------------------- --------------------
  `chmod 755 file`         Change permissions    Executable scripts
  `chown user:user file`   Change ownership      Correct ownership
  `umask`                  Default permissions   Security

# 📦 Package Management

  -----------------------------------------------------------------------
  Distribution                        Common Commands
  ----------------------------------- -----------------------------------
  Debian/Ubuntu                       `apt update`, `apt upgrade`,
                                      `apt install`, `apt remove`

  RHEL/CentOS                         `dnf update`, `dnf install`,
                                      `dnf remove`
  -----------------------------------------------------------------------

# 🔍 Search

  Command               Description            Common Use
  --------------------- ---------------------- ----------------
  `find / -name file`   Find files             Locate configs
  `grep "text" file`    Search text            Log analysis
  `locate file`         Fast filename search   Quick lookup

# 🚀 Performance

  Command         Purpose
  --------------- ---------------------
  `top`           Process monitor
  `htop`          Interactive monitor
  `vmstat 1`      CPU/Memory
  `iostat`        Disk I/O
  `sar`           Historical stats
  `lsof`          Open files
  `watch df -h`   Live disk usage

# 🛠️ Troubleshooting Workflow

``` text
Server Issue
   │
   ├── uptime
   ├── htop
   ├── systemctl status <service>
   ├── journalctl -u <service>
   ├── ss -tulnp
   ├── free -h
   ├── df -h
   └── dmesg
```

## ⭐ Daily Admin Cheat Sheet

  Task                  Command
  --------------------- --------------------
  Server Info           `hostnamectl`
  Memory                `free -h`
  Disk                  `df -h`
  Processes             `ps aux`
  Interactive Monitor   `htop`
  Open Ports            `ss -tulnp`
  Service Status        `systemctl status`
  Logs                  `journalctl -u`
  Search Text           `grep`
  Find Files            `find`
