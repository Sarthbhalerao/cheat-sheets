# 🐧 Linux Commands Handbook

> A structured, Notion-style reference of essential Linux commands for DevOps, system administration, and daily usage.

---

## 📌 1. Basic Commands

| Command  | Usage                   | Example                  |
| -------- | ----------------------- | ------------------------ |
| `ls`     | List directory contents | `ls -l`                  |
| `cd`     | Change directory        | `cd /home/user`          |
| `pwd`    | Show current directory  | `pwd`                    |
| `cp`     | Copy files/directories  | `cp file.txt backup.txt` |
| `mv`     | Move/rename files       | `mv old.txt new.txt`     |
| `rm`     | Remove files            | `rm file.txt`            |
| `rm -rf` | Force remove directory  | `rm -rf mydir`           |
| `mkdir`  | Create directory        | `mkdir new_folder`       |
| `rmdir`  | Remove empty directory  | `rmdir empty_folder`     |
| `touch`  | Create empty file       | `touch newfile.txt`      |
| `clear`  | Clear terminal          | `clear`                  |

---

## 📂 2. File & Directory Management

| Command    | Usage                  | Example                    |
| ---------- | ---------------------- | -------------------------- |
| `find`     | Search files           | `find /home -name "*.txt"` |
| `locate`   | Find files quickly     | `locate notes.txt`         |
| `tree`     | Show directory tree    | `tree mydir`               |
| `stat`     | File details           | `stat file.txt`            |
| `basename` | Extract filename       | `basename /path/file.txt`  |
| `dirname`  | Extract directory path | `dirname /path/file.txt`   |
| `rsync`    | Sync files             | `rsync -avz src/ dest/`    |

---

## 🔐 3. File Permissions & Ownership

| Command | Usage               | Example                    |
| ------- | ------------------- | -------------------------- |
| `chmod` | Change permissions  | `chmod 755 script.sh`      |
| `chown` | Change owner        | `sudo chown user file.txt` |
| `chgrp` | Change group        | `sudo chgrp dev file.txt`  |
| `umask` | Default permissions | `umask 022`                |

---

## 👤 4. User & Permission Management

| Command    | Usage            | Example                         |
| ---------- | ---------------- | ------------------------------- |
| `useradd`  | Add user         | `sudo useradd testusr`          |
| `adduser`  | Interactive add  | `sudo adduser testusr`          |
| `usermod`  | Modify user      | `sudo usermod -aG sudo testusr` |
| `passwd`   | Change password  | `passwd testusr`                |
| `userdel`  | Delete user      | `sudo userdel testusr`          |
| `groupadd` | Add group        | `sudo groupadd testgrp`         |
| `groupdel` | Delete group     | `sudo groupdel testgrp`         |
| `groups`   | Show user groups | `groups testusr`                |
| `id`       | Show UID/GID     | `id testusr`                    |
| `whoami`   | Current user     | `whoami`                        |
| `who`      | Logged-in users  | `who`                           |
| `w`        | User activity    | `w`                             |
| `chage`    | Password aging   | `sudo chage -l testusr`         |

---

## ⚙️ 5. Process Management

| Command    | Usage               | Example           |
| ---------- | ------------------- | ----------------- |
| `ps`       | Show processes      | `ps aux`          |
| `top`      | Real-time monitor   | `top`             |
| `htop`     | Interactive monitor | `htop`            |
| `kill`     | Kill by PID         | `kill -9 1234`    |
| `killall`  | Kill by name        | `killall firefox` |
| `jobs`     | List jobs           | `jobs`            |
| `bg`       | Resume background   | `bg %1`           |
| `fg`       | Foreground job      | `fg %1`           |
| `shutdown` | Shutdown system     | `shutdown -h now` |
| `reboot`   | Restart system      | `sudo reboot`     |
| `poweroff` | Power off           | `poweroff`        |
| `init`     | Change runlevel     | `init 6`          |

---

## 🛠 6. Service Management (systemd)

| Command             | Usage           | Example                 |
| ------------------- | --------------- | ----------------------- |
| `systemctl status`  | Check service   | `systemctl status ssh`  |
| `systemctl start`   | Start service   | `systemctl start ssh`   |
| `systemctl stop`    | Stop service    | `systemctl stop ssh`    |
| `systemctl restart` | Restart service | `systemctl restart ssh` |
| `systemctl enable`  | Enable at boot  | `systemctl enable ssh`  |
| `journalctl`        | System logs     | `journalctl -xe`        |
| `journalctl -u`     | Service logs    | `journalctl -u ssh`     |

---

## 🌐 7. Networking Commands

| Command      | Usage                | Example                   |
| ------------ | -------------------- | ------------------------- |
| `ping`       | Connectivity test    | `ping google.com`         |
| `ip`         | Network info         | `ip a`                    |
| `ifconfig`   | Network config (old) | `ifconfig eth0`           |
| `netstat`    | Network connections  | `netstat -tuln`           |
| `ss`         | Socket stats         | `ss -tuln`                |
| `traceroute` | Trace route          | `traceroute google.com`   |
| `nslookup`   | DNS query            | `nslookup example.com`    |
| `dig`        | DNS lookup           | `dig example.com`         |
| `curl`       | Fetch URL data       | `curl http://example.com` |
| `wget`       | Download file        | `wget http://file.zip`    |
| `scp`        | Secure copy          | `scp file user@host:/tmp` |
| `ssh`        | Remote login         | `ssh user@192.168.1.10`   |
| `nc`         | Network utility      | `nc -l -p 844`            |

---

## 💽 8. Disk Management

| Command  | Usage             | Example                    |
| -------- | ----------------- | -------------------------- |
| `df`     | Disk usage        | `df -h`                    |
| `du`     | Directory size    | `du -sh /home/user`        |
| `lsblk`  | Block devices     | `lsblk`                    |
| `blkid`  | Block attributes  | `blkid`                    |
| `fdisk`  | Partition disk    | `sudo fdisk /dev/sda`      |
| `parted` | Disk partitions   | `sudo parted /dev/sda`     |
| `mkfs`   | Create filesystem | `sudo mkfs.ext4 /dev/sdb1` |
| `fsck`   | Check filesystem  | `sudo fsck /dev/sdb1`      |
| `mount`  | Mount FS          | `mount /dev/sdb1 /mnt`     |
| `umount` | Unmount FS        | `umount /mnt`              |
| `fstab`  | FS config file    | `/etc/fstab`               |

---

## 📊 9. System Monitoring & Performance

| Command    | Usage           | Example           |
| ---------- | --------------- | ----------------- |
| `uptime`   | System run time | `uptime`          |
| `free`     | Memory usage    | `free -h`         |
| `vmstat`   | Memory stats    | `vmstat 1`        |
| `iostat`   | CPU/IO stats    | `iostat`          |
| `time`     | Execution time  | `time ls`         |
| `uname`    | System info     | `uname -a`        |
| `hostname` | Hostname        | `hostname`        |
| `dmesg`    | Boot logs       | `dmesg`           |
| `lscpu`    | CPU info        | `lscpu`           |
| `lsusb`    | USB devices     | `lsusb`           |
| `lspci`    | PCI devices     | `lspci`           |
| `lshw`     | Hardware info   | `sudo lshw`       |
| `watch`    | Run repeatedly  | `watch -n 1 free` |

---

## 📦 10. Compression & Archiving

| Command  | Usage          | Example                 |
| -------- | -------------- | ----------------------- |
| `tar`    | Create/extract | `tar -xvzf file.tar.gz` |
| `gzip`   | Compress       | `gzip file.txt`         |
| `gunzip` | Decompress     | `gunzip file.gz`        |
| `bzip2`  | Compress       | `bzip2 file.txt`        |
| `zip`    | Zip files      | `zip a.zip file.txt`    |
| `unzip`  | Extract zip    | `unzip a.zip`           |

---

## ⏰ 11. Scheduling & Automation

| Command   | Usage                 | Example               |
| --------- | --------------------- | --------------------- |
| `cron`    | Scheduled jobs daemon | Runs in background    |
| `crontab` | Manage cron           | `crontab -e`          |
| `at`      | One-time job          | `echo "shutdown now"` |
| `batch`   | Low-load job          | `echo "./script.sh"`  |
| `sleep`   | Delay                 | `sleep 10s`           |

---

## 📚 12. Help & Documentation

| Command   | Usage             | Example          |
| --------- | ----------------- | ---------------- |
| `man`     | Manual pages      | `man ls`         |
| `info`    | GNU docs          | `info coreutils` |
| `--help`  | Command help      | `ls --help`      |
| `whatis`  | Short description | `whatis grep`    |
| `apropos` | Search man pages  | `apropos copy`   |

---

## 🔎 13. Text Processing

| Command  | Usage             | Example                     |
| -------- | ----------------- | --------------------------- |
| `cat`    | Display file      | `cat file.txt`              |
| `less`   | Page view         | `less file.txt`             |
| `more`   | Simple pager      | `more file.txt`             |
| `head`   | First lines       | `head file.txt`             |
| `tail`   | Last lines        | `tail file.txt`             |
| `grep`   | Search text       | `grep error file.txt`       |
| `sed`    | Edit stream       | `sed 's/a/b/g' file.txt`    |
| `awk`    | Pattern scan      | `awk '{print $1}' file.txt` |
| `cut`    | Extract fields    | `cut -d: -f1 /etc/passwd`   |
| `sort`   | Sort text         | `sort names.txt`            |
| `uniq`   | Remove duplicates | `uniq sorted.txt`           |
| `tr`     | Translate chars   | `tr a-z A-Z < file.txt`     |
| `wc`     | Count words       | `wc file.txt`               |
| `vi/vim` | Text editor       | `vim script.sh`             |

---

## 📦 14. Package Management

| Command   | Usage          | Example                 |
| --------- | -------------- | ----------------------- |
| `apt`     | Debian manager | `apt update`            |
| `apt-get` | APT utility    | `apt-get install nginx` |
| `yum`     | RHEL manager   | `yum install httpd`     |
| `dnf`     | Modern RHEL    | `dnf install nginx`     |

---

## 🔒 15. Security & Firewall

| Command    | Usage         | Example                  |
| ---------- | ------------- | ------------------------ |
| `sudo`     | Run as root   | `sudo apt install nginx` |
| `su`       | Switch user   | `su - testusr`           |
| `visudo`   | Edit sudoers  | `sudo visudo`            |
| `ufw`      | Firewall tool | `sudo ufw enable`        |
| `iptables` | Packet rules  | `sudo iptables -L`       |

---

## 🐚 16. Shell & Scripting

| Command       | Usage             | Example                  |
| ------------- | ----------------- | ------------------------ |
| `bash`        | Run bash script   | `bash script.sh`         |
| `sh`          | Run shell script  | `sh script.sh`           |
| `./script.sh` | Execute script    | `./deploy.sh`            |
| `source`      | Run in same shell | `source ~/.bashrc`       |
| `export`      | Set env variable  | `export PATH=$PATH:/bin` |
| `alias`       | Command shortcut  | `alias ll='ls -la'`      |
| `unalias`     | Remove alias      | `unalias ll`             |
| `read`        | User input        | `read name`              |
| `echo`        | Print output      | `echo "Hello"`           |
| `env`         | Env variables     | `env`                    |
| `set`         | Shell variables   | `set`                    |
| `history`     | Command history   | `history`                |
| `chmod +x`    | Make executable   | `chmod +x script.sh`     |

---

# 🎯 Summary

* Covers **all essential Linux commands**
* Structured for **quick lookup**
* Ideal for:

  * DevOps engineers
  * System admins
  * Beginners → advanced users

---
