# 🐧 Linux Master Cheatsheet

> A complete reference of Linux commands for **DevOps, system administration, and daily usage**

---

# 📌 1. Basic Commands

- `ls` : List directory contents
  - **Example:** `ls -l`

- `cd` : Change directory
  - **Example:** `cd /home/user`

- `pwd` : Show current directory
  - **Example:** `pwd`

- `cp` : Copy files or directories
  - **Example:** `cp file.txt backup.txt`

- `mv` : Move or rename files
  - **Example:** `mv old.txt new.txt`

- `rm` : Remove files
  - **Example:** `rm file.txt`

- `rm -rf` : Force remove directory
  - **Example:** `rm -rf mydir`

- `mkdir` : Create directory
  - **Example:** `mkdir new_folder`

- `rmdir` : Remove empty directory
  - **Example:** `rmdir empty_folder`

- `touch` : Create empty file
  - **Example:** `touch file.txt`

- `clear` : Clear terminal
  - **Example:** `clear`

---

# 📂 2. File & Directory Management

- `find` : Search files
  - **Example:** `find /home -name "*.txt"`

- `locate` : Find files quickly
  - **Example:** `locate file.txt`

- `tree` : Show directory structure
  - **Example:** `tree`

- `stat` : Show file details
  - **Example:** `stat file.txt`

- `basename` : Extract filename
  - **Example:** `basename /path/file.txt`

- `dirname` : Extract directory path
  - **Example:** `dirname /path/file.txt`

- `rsync` : Sync files/directories
  - **Example:** `rsync -avz src/ dest/`

---

# 🔐 3. File Permissions & Ownership

- `chmod` : Change file permissions
  - **Example:** `chmod 755 script.sh`

- `chown` : Change file owner
  - **Example:** `sudo chown user file.txt`

- `chgrp` : Change group ownership
  - **Example:** `sudo chgrp dev file.txt`

- `umask` : Set default permissions
  - **Example:** `umask 022`

---

# 👤 4. User Management

- `useradd` : Create user
-   - **Example:** `sudo useradd user`

- `adduser` : Create user interactively
  - **Example:** `sudo adduser user`

- `usermod` : Modify user
  - **Example:** `sudo usermod -aG sudo user`

- `passwd` : Set or change password
  - **Example:** `sudo passwd user`

- `userdel` : Delete user
  - **Example:** `sudo userdel -r user`

- `id` : Show user UID and groups
  - **Example:** `id user`

- `groups` : Show user groups
  - **Example:** `groups user`

- `whoami` : Show current user
  - **Example:** `whoami`

- `who` : Show logged-in users
  - **Example:** `who`

- `w` : Show user activity
  - **Example:** `w`

- `chage` : Manage password aging
  - **Example:** `sudo chage -l user`

- `usermod -u` : Change UID
  - **Example:** `sudo usermod -u 1001 user`

- `usermod -g` : Change primary group
  - **Example:** `sudo usermod -g dev user`

- `usermod -aG` : Add user to group
  - **Example:** `sudo usermod -aG dev user`

- `usermod -l` : Rename user
  - **Example:** `sudo usermod -l new old`

- `usermod -d` : Change home directory
  - **Example:** `sudo usermod -d /home/new user`

- `usermod -U` : Unlock user account
  - **Example:** `sudo usermod -U user`

- `vipw` : Safely edit /etc/passwd
  - **Example:** `sudo vipw`

- `vigr` : Safely edit /etc/group
  - **Example:** `sudo vigr`

- `visudo` : Safely edit sudoers
  - **Example:** `sudo visudo`

- `awk -F':' '{print $1}' /etc/passwd` : List all users
  - **Example:** `awk -F':' '{print $1}' /etc/passwd`

---

# 👥 5. Group Management

- `groupadd` : Create group
  - **Example:** `sudo groupadd dev`

- `groupdel` : Delete group
  - **Example:** `sudo groupdel dev`

- `groupmod` : Modify group
  - **Example:** `sudo groupmod -n new old`

- `gpasswd` : Manage group password/users
  - **Example:** `sudo gpasswd group`

- `gpasswd -a` : Add user to group
  - **Example:** `sudo gpasswd -a user dev`

- `gpasswd -d` : Remove user from group
  - **Example:** `sudo gpasswd -d user dev`

- `cut -d: -f1 /etc/group` : List group names
  - **Example:** `cut -d: -f1 /etc/group`

---

# ⚙️ 6. Process Management

- `ps` : Show processes
  - **Example:** `ps aux`

- `top` : Real-time process monitoring
  - **Example:** `top`

- `htop` : Interactive monitoring
  - **Example:** `htop`

- `kill` : Kill process by PID
  - **Example:** `kill -9 1234`

- `killall` : Kill process by name
  - **Example:** `killall nginx`

- `jobs` : List background jobs
  - **Example:** `jobs`

- `bg` : Resume background job
  - **Example:** `bg %1`

- `fg` : Bring job to foreground
  - **Example:** `fg %1`

- `shutdown` : Shutdown system
  - **Example:** `shutdown -h now`

- `reboot` : Restart system
  - **Example:** `sudo reboot`

- `poweroff` : Power off system
  - **Example:** `poweroff`

- `init` : Change runlevel
  - **Example:** `init 6`

---

# 🛠 7. Service Management

- `systemctl status` : Check service status
  - **Example:** `systemctl status ssh`

- `systemctl start` : Start service
  - **Example:** `systemctl start ssh`

- `systemctl stop` : Stop service
  - **Example:** `systemctl stop ssh`

- `systemctl restart` : Restart service
  - **Example:** `systemctl restart ssh`

- `systemctl enable` : Enable at boot
  - **Example:** `systemctl enable ssh`

- `journalctl` : View logs
  - **Example:** `journalctl -xe`

- `journalctl -u` : Service logs
  - **Example:** `journalctl -u nginx`

---

# 🌐 8. Networking

- `ping` : Check connectivity
  - **Example:** `ping google.com`

- `ip` : Show network info
  - **Example:** `ip a`

- `ifconfig` : Network config (legacy)
  - **Example:** `ifconfig`

- `netstat` : Network connections
  - **Example:** `netstat -tuln`

- `ss` : Socket stats
  - **Example:** `ss -tuln`

- `traceroute` : Trace route
  - **Example:** `traceroute google.com`

- `nslookup` : DNS query
  - **Example:** `nslookup google.com`

- `dig` : DNS lookup
  - **Example:** `dig google.com`

- `curl` : Fetch URL
  - **Example:** `curl example.com`

- `wget` : Download file
  - **Example:** `wget file.zip`

- `scp` : Secure copy
  - **Example:** `scp file user@host:/tmp`

- `ssh` : Remote login
  - **Example:** `ssh user@ip`

- `nc` : Network tool
  - **Example:** `nc -l -p 8080`

---

# 💽 9. Disk Management

- `df` : Disk usage
  - **Example:** `df -h`

- `du` : Directory size
  - **Example:** `du -sh /home`

- `lsblk` : Block devices
  - **Example:** `lsblk`

- `blkid` : Device info
  - **Example:** `blkid`

- `fdisk` : Partition disk
  - **Example:** `sudo fdisk /dev/sda`

- `parted` : Manage partitions
  - **Example:** `sudo parted /dev/sda`

- `mkfs` : Create filesystem
  - **Example:** `mkfs.ext4 /dev/sdb1`

- `fsck` : Check filesystem
  - **Example:** `fsck /dev/sdb1`

- `mount` : Mount filesystem
  - **Example:** `mount /dev/sdb1 /mnt`

- `umount` : Unmount filesystem
  - **Example:** `umount /mnt`

- `fstab` : File system mount configuration file
  - **Example:** /etc/fstab

---

# 📊 10. System Monitoring

- `uptime` : Show uptime
  - **Example:** `uptime`

- `free` : Memory usage
  - **Example:** `free -h`

- `vmstat` : Memory stats
  - **Example:** `vmstat 1`

- `iostat` : CPU/IO stats
  - **Example:** `iostat`

- `time` : Measure execution time
  - **Example:** `time ls`

- `uname` : System info
  - **Example:** `uname -a`

- `hostname` : Show hostname
  - **Example:** `hostname`

- `dmesg` : Kernel logs
  - **Example:** `dmesg`

- `lscpu` : CPU info
  - **Example:** `lscpu`

- `lsusb` : USB devices
  - **Example:** `lsusb`

- `lspci` : PCI devices
  - **Example:** `lspci`

- `lshw` : Hardware info
  - **Example:** `sudo lshw`

- `watch` : Run repeatedly
  - **Example:** `watch -n 1 free`

---

# 📦 11. Compression

- `tar` : Archive files
  - **Example:** `tar -xvzf file.tar.gz`

- `gzip` : Compress file
  - **Example:** `gzip file.txt`

- `gunzip` : Decompress
  - **Example:** `gunzip file.gz`

- `bzip2` : Compress
  - **Example:** `bzip2 file.txt`

- `zip` : Zip files
  - **Example:** `zip file.zip file.txt`

- `unzip` : Extract zip
  - **Example:** `unzip file.zip`

---

# ⏰ 12. Scheduling

- `cron` : Background scheduler
  - **Example:** Runs automatically

- `crontab` : Manage cron jobs
  - **Example:** `crontab -e`

- `at` : One-time job
  - **Example:** `at now + 1 min`

- `batch` : Run when system load is low
  - **Example:** `batch`

- `sleep` : Delay execution
  - **Example:** `sleep 10`

---

# 📚 13. Help

- `man` : Manual pages
  - **Example:** `man ls`

- `info` : Detailed help
  - **Example:** `info ls`

- `--help` : Quick help
  - **Example:** `ls --help`

- `whatis` : Short description
  - **Example:** `whatis ls`

- `apropos` : Search commands
  - **Example:** `apropos copy`

---

# 🔎 14. Text Processing

- `cat` : Display file
  - **Example:** `cat file.txt`

- `less` : Scroll file
  - **Example:** `less file.txt`

- `more` : Basic viewer
  - **Example:** `more file.txt`

- `head` : First lines
  - **Example:** `head file.txt`

- `tail` : Last lines
  - **Example:** `tail file.txt`

- `grep` : Search text
  - **Example:** `grep error file.txt`

- `sed` : Edit text stream
  - **Example:** `sed 's/a/b/g' file.txt`

- `awk` : Pattern processing
  - **Example:** `awk '{print $1}' file.txt`

- `cut` : Extract fields
  - **Example:** `cut -d: -f1 file`

- `sort` : Sort lines
  - **Example:** `sort file.txt`

- `uniq` : Remove duplicates
  - **Example:** `uniq file.txt`

- `tr` : Translate characters
  - **Example:** `tr a-z A-Z`

- `wc` : Count words/lines
  - **Example:** `wc file.txt`

- `vim` : Text editor
  - **Example:** `vim file.txt`

---

# 📦 15. Package Management

- `apt` : Package manager
  - **Example:** `apt update`

- `apt-get` : Advanced package tool
  - **Example:** `apt-get install nginx`

- `yum` : RHEL package manager
  - **Example:** `yum install httpd`

- `dnf` : Modern RHEL manager
  - **Example:** `dnf install nginx`

- `apt update && apt upgrade` : Update system packages
  - **Example:** `sudo apt update && sudo apt upgrade`

---

# 🔒 16. Security

- `sudo` : Run as root
  - **Example:** `sudo command`

- `su` : Switch user
  - **Example:** `su - user`

- `visudo` : Edit sudoers
  - **Example:** `sudo visudo`

- `ufw` : Firewall tool
  - **Example:** `sudo ufw enable`

- `iptables` : Firewall rules
  - **Example:** `sudo iptables -L`

---

## 🐚 17. Shell & Scripting

- `bash` : Run bash script  
  - **Example:** `bash script.sh`

- `sh` : Run shell script  
  - **Example:** `sh script.sh`

- `./script.sh` : Execute script directly  
  - **Example:** `./deploy.sh`

- `source` : Run script in current shell  
  - **Example:** `source ~/.bashrc`

- `export` : Set environment variable  
  - **Example:** `export PATH=$PATH:/bin`

- `alias` : Create command shortcut  
  - **Example:** `alias ll='ls -la'`

- `unalias` : Remove alias  
  - **Example:** `unalias ll`

- `read` : Take user input  
  - **Example:** `read name`

- `echo` : Print output  
  - **Example:** `echo "Hello"`

`env` : Show environment variables  
  - **Example:** `env`

- `set` : Show shell variables  
  - **Example:** `set`

- `history` : Show command history  
  - **Example:** `history`

- `chmod +x` : Make script executable  
  - **Example:** `chmod +x script.sh`

---
