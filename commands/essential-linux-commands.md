# Essential Linux Commands for Everyday Administration

A collection of Linux commands I frequently use for system administration, troubleshooting, networking, storage management, and process monitoring.

---

# System Information

| Command | Description |
|---------|-------------|
| `hostnamectl` | Display system hostname and operating system information. |
| `uname -a` | Show kernel version and system architecture. |
| `cat /etc/os-release` | Display Linux distribution details. |
| `uptime` | Show system uptime and load averages. |
| `date` | Display the current date and time. |
| `timedatectl` | View or configure time, timezone, and NTP settings. |

---

# File & Directory Management

| Command | Description |
|---------|-------------|
| `pwd` | Show the current working directory. |
| `ls -lah` | List files with permissions, sizes, and hidden files. |
| `cd <directory>` | Change directory. |
| `mkdir <dir>` | Create a new directory. |
| `rm -rf <dir>` | Remove files or directories recursively. |
| `cp -r source destination` | Copy files or directories. |
| `mv source destination` | Move or rename files. |
| `find / -name filename` | Search for files. |
| `locate filename` | Quickly locate files (requires updated database). |

---

# File Permissions

| Command | Description |
|---------|-------------|
| `chmod 755 file` | Change file permissions. |
| `chown user:group file` | Change file ownership. |
| `umask` | Display or set default file permissions. |

---

# User Management

| Command | Description |
|---------|-------------|
| `whoami` | Display the current user. |
| `id` | Show user and group IDs. |
| `useradd username` | Create a new user. |
| `passwd username` | Set or change a user's password. |
| `usermod -aG group username` | Add a user to a group. |
| `groups username` | Display user group memberships. |

---

# Disk & Storage

| Command | Description |
|---------|-------------|
| `df -h` | Show disk usage. |
| `du -sh *` | Display directory sizes. |
| `lsblk` | List block devices. |
| `blkid` | Show filesystem UUIDs. |
| `mount` | Display mounted filesystems. |
| `mount /dev/sdb1 /mnt` | Mount a filesystem. |
| `umount /mnt` | Unmount a filesystem. |

---

# Process Management

| Command | Description |
|---------|-------------|
| `ps aux` | List running processes. |
| `top` | Display running processes in real time. |
| `htop` | Interactive process viewer. |
| `kill PID` | Terminate a process. |
| `killall process` | Kill all matching processes. |
| `nice` | Start a process with a custom priority. |
| `renice` | Change the priority of a running process. |

---

# Services (systemd)

| Command | Description |
|---------|-------------|
| `systemctl status service` | Check service status. |
| `systemctl start service` | Start a service. |
| `systemctl stop service` | Stop a service. |
| `systemctl restart service` | Restart a service. |
| `systemctl enable service` | Enable service at boot. |
| `systemctl disable service` | Disable service at boot. |

---

# Networking

| Command | Description |
|---------|-------------|
| `ip addr` | Show IP addresses. |
| `ip route` | Display routing table. |
| `ping host` | Test network connectivity. |
| `ss -tulnp` | Display listening ports. |
| `curl URL` | Send HTTP requests. |
| `wget URL` | Download files. |
| `traceroute host` | Trace packet path. |
| `dig domain.com` | Query DNS records. |
| `nslookup domain.com` | Lookup DNS information. |
| `tcpdump -i eth0` | Capture network packets. |

---

# SSH

| Command | Description |
|---------|-------------|
| `ssh user@host` | Connect to a remote server. |
| `scp file user@host:/path` | Securely copy files. |
| `ssh-keygen` | Generate SSH keys. |
| `ssh-copy-id user@host` | Copy SSH public key to a remote host. |

---

# Logs

| Command | Description |
|---------|-------------|
| `journalctl` | View system logs. |
| `journalctl -u nginx` | View logs for a specific service. |
| `tail -f /var/log/syslog` | Monitor log output in real time. |
| `dmesg` | Display kernel messages. |

---

# Package Management (Ubuntu/Debian)

| Command | Description |
|---------|-------------|
| `sudo apt update` | Refresh package index. |
| `sudo apt upgrade` | Upgrade installed packages. |
| `sudo apt install package` | Install a package. |
| `sudo apt remove package` | Remove a package. |
| `sudo apt autoremove` | Remove unused dependencies. |

---

# Compression

| Command | Description |
|---------|-------------|
| `tar -czvf backup.tar.gz folder` | Create a compressed archive. |
| `tar -xzvf backup.tar.gz` | Extract an archive. |
| `zip -r archive.zip folder` | Compress files into a ZIP archive. |
| `unzip archive.zip` | Extract a ZIP archive. |

---

# Useful Utilities

| Command | Description |
|---------|-------------|
| `history` | Show command history. |
| `clear` | Clear the terminal screen. |
| `alias ll='ls -lah'` | Create a command alias. |
| `watch command` | Execute a command repeatedly. |
| `xargs` | Build and execute commands from standard input. |

---

## Notes

This document is intended as a practical reference and will continue to grow as I explore Linux administration, automation, troubleshooting, and infrastructure management.
