# 🐧 Linux Commands Handbook

A practical beginner-to-intermediate guide to Linux commands, file management, permissions, processes, networking, system administration, and cybersecurity usage.

---

# 📚 Table of Contents

* [Linux Basics](#linux-basics)
* [Command Structure](#command-structure)
* [Navigation Commands](#navigation-commands)
* [File and Directory Management](#file-and-directory-management)
* [Viewing File Contents](#viewing-file-contents)
* [Searching Files and Directories](#searching-files-and-directories)
* [Text Processing](#text-processing)
* [Pipes and Redirection](#pipes-and-redirection)
* [File Permissions](#file-permissions)
* [Users and Groups](#users-and-groups)
* [Process Management](#process-management)
* [System Information](#system-information)
* [Disk and Storage](#disk-and-storage)
* [Networking Commands](#networking-commands)
* [Package Management](#package-management)
* [Archives and Compression](#archives-and-compression)
* [Environment Variables](#environment-variables)
* [SSH](#ssh)
* [Command History](#command-history)
* [Help and Documentation](#help-and-documentation)
* [Command Chaining](#command-chaining)
* [Useful Security Commands](#useful-security-commands)
* [Important Directories](#important-directories)
* [Practical Examples](#practical-examples)
* [Quick Reference](#quick-reference)

---

# Linux Basics

## What is Linux?

Linux is an open-source operating system kernel.

Linux distributions combine the Linux kernel with other software to create a complete operating system.

Examples:

* Kali Linux
* Ubuntu
* Debian
* Fedora
* Arch Linux
* Linux Mint
* Rocky Linux

For example, Kali Linux is commonly used for:

* Penetration testing
* Vulnerability assessment
* Digital forensics
* Security research
* Network analysis
* CTFs

---

# Command Structure

Most Linux commands follow this structure:

```bash
command [options] [arguments]
```

Example:

```bash
ls -l /home
```

Here:

* `ls` → command
* `-l` → option
* `/home` → argument

Another example:

```bash
mkdir -p projects/tools
```

Here:

* `mkdir` → command
* `-p` → option
* `projects/tools` → argument

---

# Navigation Commands

## `pwd`

`pwd` means **Print Working Directory**.

It displays the directory you are currently inside.

```bash
pwd
```

Example output:

```text
/home/kali
```

This is useful when you are unsure about your current location.

---

## `ls`

`ls` lists files and directories.

```bash
ls
```

### Common Options

```bash
ls -l
```

Shows detailed information.

```bash
ls -a
```

Shows hidden files.

```bash
ls -la
```

Shows hidden files in detailed format.

```bash
ls -lh
```

Shows file sizes in human-readable format.

```bash
ls -R
```

Lists directories recursively.

### Example

```bash
ls -lah /var/log
```

Useful when inspecting log files.

---

## `cd`

`cd` means **Change Directory**.

```bash
cd /home
```

Moves to `/home`.

### Go to Home Directory

```bash
cd ~
```

or simply:

```bash
cd
```

### Go to Parent Directory

```bash
cd ..
```

### Go to Previous Directory

```bash
cd -
```

### Example

```bash
cd /var/log
pwd
```

Output:

```text
/var/log
```

---

## `clear`

Clears the terminal screen.

```bash
clear
```

Keyboard shortcut:

```text
Ctrl + L
```

---

## `whoami`

Displays the currently logged-in username.

```bash
whoami
```

Example:

```text
kali
```

This is particularly useful when working with different users or privilege levels.

---

# File and Directory Management

## `mkdir`

Creates a directory.

```bash
mkdir notes
```

Creates:

```text
notes/
```

### Create Nested Directories

```bash
mkdir -p projects/cybersecurity/linux
```

The `-p` option creates parent directories when necessary.

---

## `touch`

Creates an empty file.

```bash
touch notes.txt
```

It can also update the modification timestamp of an existing file.

```bash
touch existing.txt
```

---

## `cp`

Copies files or directories.

### Copy a File

```bash
cp file.txt backup.txt
```

### Copy File to Directory

```bash
cp file.txt /home/kali/Documents/
```

### Copy a Directory

```bash
cp -r project/ backup/
```

The `-r` option means recursive.

---

## `mv`

Moves or renames files and directories.

### Rename a File

```bash
mv old.txt new.txt
```

### Move a File

```bash
mv report.txt /home/kali/Documents/
```

### Rename a Directory

```bash
mv old_folder new_folder
```

---

## `rm`

Removes files.

```bash
rm file.txt
```

### Remove Multiple Files

```bash
rm file1.txt file2.txt
```

### Remove a Directory

```bash
rm -r folder/
```

### Force Removal

```bash
rm -f file.txt
```

### Recursive + Force

```bash
rm -rf folder/
```

**Warning:** `rm -rf` can permanently delete large amounts of data. Always verify the path before using it.

---

## `rmdir`

Removes an empty directory.

```bash
rmdir empty_folder
```

It will not normally remove a directory containing files.

---

# Viewing File Contents

## `cat`

Displays the complete contents of a file.

```bash
cat file.txt
```

### Multiple Files

```bash
cat file1.txt file2.txt
```

### Create a File Using `cat`

```bash
cat > notes.txt
```

Type the content and press:

```text
Ctrl + D
```

to finish.

---

## `less`

Displays large files one screen at a time.

```bash
less largefile.txt
```

Useful for reading:

* Log files
* Configuration files
* Long command output

Useful keys:

| Key     | Action        |
| ------- | ------------- |
| `Space` | Next page     |
| `b`     | Previous page |
| `/word` | Search        |
| `q`     | Quit          |

---

## `more`

Another command for viewing files page by page.

```bash
more file.txt
```

`less` is generally more flexible.

---

## `head`

Displays the beginning of a file.

```bash
head file.txt
```

### First 20 Lines

```bash
head -n 20 file.txt
```

---

## `tail`

Displays the end of a file.

```bash
tail file.txt
```

### Last 20 Lines

```bash
tail -n 20 file.txt
```

### Follow a Log File

```bash
tail -f /var/log/auth.log
```

`-f` continuously displays new lines as they are added.

This is useful for monitoring logs.

---

# Searching Files and Directories

## `find`

Searches for files and directories.

### Search by Name

```bash
find /home/kali -name "notes.txt"
```

### Find All `.log` Files

```bash
find /var/log -name "*.log"
```

### Find Directories

```bash
find /home/kali -type d
```

### Find Files

```bash
find /home/kali -type f
```

### Find Files Larger Than 100 MB

```bash
find / -type f -size +100M 2>/dev/null
```

The `2>/dev/null` hides permission-denied messages.

---

## `locate`

Searches for files using a prebuilt database.

```bash
locate passwd
```

It is usually faster than `find`, but the database may not contain the newest files.

Update the database when supported:

```bash
sudo updatedb
```

---

## `which`

Shows the location of an executable.

```bash
which python
```

Example:

```text
/usr/bin/python
```

Useful for determining which executable will be used.

---

## `whereis`

Searches for binary, source, and manual-page locations.

```bash
whereis python
```

---

# Text Processing

## `grep`

Searches for matching text.

```bash
grep "error" logfile.txt
```

### Case-Insensitive Search

```bash
grep -i "error" logfile.txt
```

### Show Line Numbers

```bash
grep -n "error" logfile.txt
```

### Recursive Search

```bash
grep -r "password" /home/kali/projects/
```

### Invert Match

```bash
grep -v "error" logfile.txt
```

Shows lines that do **not** contain `error`.

### Regular Expressions

```bash
grep -E "admin|root|user" users.txt
```

Searches for any of the three terms.

### Cybersecurity Example

```bash
grep "Failed password" /var/log/auth.log
```

Can help identify failed SSH authentication attempts.

---

## `sort`

Sorts lines of text.

```bash
sort users.txt
```

### Reverse Order

```bash
sort -r users.txt
```

---

## `uniq`

Removes adjacent duplicate lines.

```bash
uniq users.txt
```

For accurate duplicate removal, sort first:

```bash
sort users.txt | uniq
```

### Count Occurrences

```bash
sort users.txt | uniq -c
```

---

## `wc`

Counts lines, words, and bytes.

```bash
wc file.txt
```

### Count Lines

```bash
wc -l file.txt
```

### Count Words

```bash
wc -w file.txt
```

### Count Characters/Bytes

```bash
wc -c file.txt
```

Example:

```bash
cat users.txt | wc -l
```

Counts the number of lines.

---

## `cut`

Extracts sections from each line.

Example file:

```text
admin:1000:/home/admin
user:1001:/home/user
```

Command:

```bash
cut -d ":" -f 1 users.txt
```

Output:

```text
admin
user
```

Here:

* `-d ":"` → delimiter is `:`
* `-f 1` → select field 1

---

## `awk`

A powerful text-processing language.

Example:

```bash
awk '{print $1}' file.txt
```

Prints the first whitespace-separated field.

Example:

```bash
awk -F ":" '{print $1}' /etc/passwd
```

Displays usernames from `/etc/passwd`.

---

## `sed`

Used to search, replace, insert, or delete text.

### Replace Text

```bash
sed 's/old/new/' file.txt
```

Replace all occurrences on each line:

```bash
sed 's/old/new/g' file.txt
```

Example:

```bash
sed 's/http:/https:/g' urls.txt
```

---

# Pipes and Redirection

Linux commands can be combined to create powerful workflows.

## Pipe `|`

A pipe sends the output of one command to another command.

```bash
ls | grep ".txt"
```

Process:

```text
ls
 ↓
grep
 ↓
.txt files
```

---

## Example

```bash
ps aux | grep firefox
```

First:

```bash
ps aux
```

lists processes.

Then:

```bash
grep firefox
```

filters the output.

---

## Output Redirection `>`

Writes output to a file.

```bash
ls > files.txt
```

If the file exists, its contents are overwritten.

---

## Append `>>`

Adds output to the end of a file.

```bash
echo "New entry" >> log.txt
```

Existing content is preserved.

---

## Input Redirection `<`

Uses a file as input.

```bash
sort < users.txt
```

---

## Error Redirection `2>`

Redirects standard error.

```bash
command 2> errors.txt
```

---

## Redirect Output and Errors

```bash
command > output.txt 2> errors.txt
```

---

## Redirect Everything

```bash
command > output.txt 2>&1
```

This sends standard output and standard error to the same file.

---

## `/dev/null`

`/dev/null` discards data.

```bash
command > /dev/null
```

Discard errors:

```bash
command 2>/dev/null
```

Discard both:

```bash
command > /dev/null 2>&1
```

---

# File Permissions

Linux uses permissions to control access to files and directories.

Example:

```bash
ls -l file.txt
```

Output:

```text
-rw-r--r-- 1 kali kali 120 Sep 13 18:00 file.txt
```

The permission section is:

```text
-rw-r--r--
```

Breakdown:

```text
- rw- r-- r--
  │   │   │
  │   │   └── Others
  │   └────── Group
  └────────── Owner
```

---

## Permission Types

| Symbol | Meaning                |
| ------ | ---------------------- |
| `r`    | Read                   |
| `w`    | Write                  |
| `x`    | Execute                |
| `-`    | Permission not granted |

Numeric values:

| Permission | Value |
| ---------- | ----: |
| `r`        |     4 |
| `w`        |     2 |
| `x`        |     1 |

Therefore:

```text
rwx = 4 + 2 + 1 = 7
rw- = 4 + 2 = 6
r-x = 4 + 1 = 5
r-- = 4
```

---

## `chmod`

Changes file permissions.

### Give Owner Execute Permission

```bash
chmod u+x script.sh
```

### Remove Write Permission from Group

```bash
chmod g-w file.txt
```

### Numeric Permissions

```bash
chmod 755 script.sh
```

Meaning:

```text
Owner  = rwx = 7
Group  = r-x = 5
Others = r-x = 5
```

So:

```text
755 = rwxr-xr-x
```

Another common permission:

```bash
chmod 644 file.txt
```

Meaning:

```text
Owner  = rw-
Group  = r--
Others = r--
```

---

# Ownership

## `chown`

Changes file ownership.

```bash
sudo chown user file.txt
```

Change owner and group:

```bash
sudo chown user:group file.txt
```

Example:

```bash
sudo chown kali:kali report.txt
```

---

## `chgrp`

Changes the group ownership.

```bash
sudo chgrp developers project.txt
```

---

# Users and Groups

## `id`

Displays user and group information.

```bash
id
```

Example:

```text
uid=1000(kali) gid=1000(kali) groups=1000(kali),27(sudo)
```

---

## `who`

Shows users currently logged in.

```bash
who
```

---

## `w`

Shows logged-in users and what they are doing.

```bash
w
```

---

## `users`

Displays currently logged-in usernames.

```bash
users
```

---

## `sudo`

Runs a command with elevated privileges.

```bash
sudo command
```

Example:

```bash
sudo apt update
```

`sudo` does not automatically mean "become root permanently." It executes the specified command with elevated privileges if the user is authorized.

---

## `su`

Switches to another user.

```bash
su username
```

Switch to root where permitted:

```bash
su -
```

---

## `passwd`

Changes a user's password.

```bash
passwd
```

Change another user's password with appropriate privileges:

```bash
sudo passwd username
```

---

## `useradd`

Creates a user.

```bash
sudo useradd username
```

Create a user with a home directory:

```bash
sudo useradd -m username
```

---

## `userdel`

Deletes a user.

```bash
sudo userdel username
```

Delete user and home directory:

```bash
sudo userdel -r username
```

---

## `groupadd`

Creates a group.

```bash
sudo groupadd developers
```

---

## `usermod`

Modifies a user account.

Add a user to a group:

```bash
sudo usermod -aG developers username
```

The `-aG` combination means:

* `-a` → append
* `-G` → supplementary group

---

# Process Management

A process is a running instance of a program.

## `ps`

Displays running processes.

```bash
ps
```

### All Processes

```bash
ps aux
```

### Search for a Process

```bash
ps aux | grep ssh
```

---

## `top`

Displays processes and system resource usage in real time.

```bash
top
```

Press:

```text
q
```

to exit.

---

## `htop`

An interactive alternative to `top`.

```bash
htop
```

It may need to be installed first.

---

## `pgrep`

Searches for processes by name.

```bash
pgrep ssh
```

---

## `kill`

Terminates a process using its PID.

```bash
kill PID
```

Example:

```bash
kill 1234
```

---

## `kill -9`

Forcefully terminates a process.

```bash
kill -9 1234
```

Use this when normal termination does not work.

---

## `pkill`

Kills processes based on their name.

```bash
pkill firefox
```

Use carefully because multiple matching processes may be affected.

---

## Background Processes

Run a command in the background:

```bash
command &
```

Example:

```bash
python server.py &
```

---

## `jobs`

Shows jobs running in the current shell.

```bash
jobs
```

---

## `fg`

Brings a background job to the foreground.

```bash
fg
```

---

## `bg`

Continues a stopped job in the background.

```bash
bg
```

---

# System Information

## `uname`

Displays system information.

```bash
uname
```

### Kernel Information

```bash
uname -a
```

---

## `hostname`

Displays the system hostname.

```bash
hostname
```

Set hostname where supported and authorized:

```bash
sudo hostname new-name
```

---

## `hostnamectl`

Displays and manages hostname/system information on systems using systemd.

```bash
hostnamectl
```

---

## `date`

Displays the current date and time.

```bash
date
```

---

## `uptime`

Shows how long the system has been running.

```bash
uptime
```

---

## `free`

Displays memory usage.

```bash
free
```

Human-readable:

```bash
free -h
```

---

## `lscpu`

Displays CPU information.

```bash
lscpu
```

---

## `lsusb`

Displays connected USB devices.

```bash
lsusb
```

---

## `lspci`

Displays PCI devices.

```bash
lspci
```

---

## `dmesg`

Displays kernel messages.

```bash
dmesg
```

Some systems require privileges:

```bash
sudo dmesg
```

Useful for troubleshooting hardware and kernel events.

---

# Disk and Storage

## `df`

Shows filesystem disk usage.

```bash
df
```

Human-readable:

```bash
df -h
```

Example:

```text
Filesystem      Size  Used Avail Use%
/dev/sda1        50G   20G   28G  42%
```

---

## `du`

Shows directory/file space usage.

```bash
du -sh folder/
```

Here:

* `-s` → summary
* `-h` → human-readable

Find large directories:

```bash
du -sh * | sort -h
```

---

## `lsblk`

Displays block devices.

```bash
lsblk
```

Useful for identifying:

* Hard drives
* SSDs
* USB drives
* Partitions

---

## `mount`

Mounts a filesystem.

```bash
sudo mount /dev/sdb1 /mnt
```

---

## `umount`

Unmounts a filesystem.

```bash
sudo umount /mnt
```

---

# Networking Commands

Networking commands are particularly important for cybersecurity.

## `ip`

The modern command for inspecting and configuring network interfaces.

### Show Interfaces

```bash
ip addr
```

Short form:

```bash
ip a
```

### Show Routes

```bash
ip route
```

### Show Link Information

```bash
ip link
```

### Show Neighbor/ARP Information

```bash
ip neigh
```

---

## `ping`

Tests network connectivity.

```bash
ping 8.8.8.8
```

Test a hostname:

```bash
ping google.com
```

Stop with:

```text
Ctrl + C
```

---

## `ss`

Displays network sockets.

```bash
ss
```

### Listening Ports

```bash
ss -l
```

### TCP Listening Ports

```bash
ss -ltn
```

### UDP Listening Ports

```bash
ss -lun
```

### Show Processes

```bash
sudo ss -lntup
```

This is useful for identifying services listening on the system.

---

## `netstat`

Older networking command.

```bash
netstat -tuln
```

`ss` is generally preferred on modern Linux systems.

---

## `traceroute`

Shows the path packets take to a destination.

```bash
traceroute example.com
```

It may need to be installed.

---

## `tracepath`

Another tool for discovering the network path.

```bash
tracepath example.com
```

---

## `nslookup`

Performs DNS queries.

```bash
nslookup example.com
```

---

## `dig`

A powerful DNS query tool.

```bash
dig example.com
```

### Query A Record

```bash
dig example.com A
```

### Query MX Record

```bash
dig example.com MX
```

### Query TXT Record

```bash
dig example.com TXT
```

### Short Output

```bash
dig +short example.com
```

Useful during reconnaissance and DNS troubleshooting.

---

## `host`

Simple DNS lookup utility.

```bash
host example.com
```

---

## `curl`

Transfers data using URLs.

```bash
curl https://example.com
```

### Save Output

```bash
curl -o page.html https://example.com
```

### Show HTTP Headers

```bash
curl -I https://example.com
```

### Follow Redirects

```bash
curl -L https://example.com
```

### Send a Custom Header

```bash
curl -H "User-Agent: test" https://example.com
```

`curl` is widely used for API testing, HTTP troubleshooting, and security testing.

---

## `wget`

Downloads files from the network.

```bash
wget https://example.com/file.zip
```

### Save with Custom Name

```bash
wget -O file.zip https://example.com/file.zip
```

---

## `nc`

`nc` stands for **netcat**.

It can create TCP/UDP connections and is useful for network troubleshooting and testing.

Example:

```bash
nc -vz 192.168.1.10 22
```

This checks whether TCP port 22 is reachable.

---

## `nmap`

Nmap is a network discovery and security auditing tool.

### Basic Scan

```bash
nmap 192.168.1.10
```

### Service Detection

```bash
nmap -sV 192.168.1.10
```

### OS Detection

```bash
sudo nmap -O 192.168.1.10
```

### Specific Ports

```bash
nmap -p 22,80,443 192.168.1.10
```

### Scan a Network

```bash
nmap 192.168.1.0/24
```

Only scan systems you own or are explicitly authorized to test.

---

# Package Management

Package management depends on the Linux distribution.

For Debian-based distributions such as Kali Linux and Ubuntu, `apt` is commonly used.

## `apt update`

Updates package repository information.

```bash
sudo apt update
```

---

## `apt upgrade`

Upgrades installed packages.

```bash
sudo apt upgrade
```

---

## `apt install`

Installs a package.

```bash
sudo apt install nmap
```

---

## `apt remove`

Removes a package.

```bash
sudo apt remove package-name
```

---

## `apt search`

Searches available packages.

```bash
apt search nmap
```

---

## `apt show`

Displays package information.

```bash
apt show nmap
```

---

## `dpkg`

Low-level Debian package manager.

Install a `.deb` package:

```bash
sudo dpkg -i package.deb
```

List installed packages:

```bash
dpkg -l
```

---

# Archives and Compression

## `tar`

Creates and extracts archives.

### Create Archive

```bash
tar -cf archive.tar folder/
```

### Extract Archive

```bash
tar -xf archive.tar
```

### Create Gzip Archive

```bash
tar -czf archive.tar.gz folder/
```

### Extract Gzip Archive

```bash
tar -xzf archive.tar.gz
```

### List Contents

```bash
tar -tf archive.tar
```

Common options:

| Option | Meaning |
| ------ | ------- |
| `c`    | Create  |
| `x`    | Extract |
| `t`    | List    |
| `f`    | File    |
| `z`    | gzip    |

---

## `gzip`

Compresses files.

```bash
gzip file.txt
```

Decompress:

```bash
gunzip file.txt.gz
```

---

## `zip`

Creates ZIP archives.

```bash
zip archive.zip file.txt
```

Directory:

```bash
zip -r archive.zip folder/
```

---

## `unzip`

Extracts ZIP files.

```bash
unzip archive.zip
```

---

# Environment Variables

Environment variables store configuration information used by processes and shells.

## `env`

Displays environment variables.

```bash
env
```

---

## `printenv`

Displays environment variables.

```bash
printenv
```

Specific variable:

```bash
printenv HOME
```

---

## `$HOME`

Stores the user's home directory.

```bash
echo $HOME
```

Example:

```text
/home/kali
```

---

## `$PATH`

Contains directories searched for executable commands.

```bash
echo $PATH
```

Example:

```text
/usr/local/bin:/usr/bin:/bin
```

When you type:

```bash
python
```

the shell searches directories in `$PATH` to find the executable.

---

## `export`

Creates an environment variable for the current shell and its child processes.

```bash
export NAME="Bhavya"
```

Check:

```bash
echo $NAME
```

---

# SSH

SSH stands for **Secure Shell**.

It allows secure remote access to another system.

## Connect to a Remote System

```bash
ssh username@192.168.1.10
```

Example:

```bash
ssh kali@192.168.1.10
```

---

## Specify a Port

```bash
ssh -p 2222 username@192.168.1.10
```

---

## SSH Keys

Generate an SSH key pair:

```bash
ssh-keygen
```

Typical files:

```text
~/.ssh/id_ed25519
~/.ssh/id_ed25519.pub
```

The private key should be protected and should not be shared.

---

## `ssh-keygen`

Generate an Ed25519 key:

```bash
ssh-keygen -t ed25519
```

---

## `scp`

Securely copies files over SSH.

### Upload

```bash
scp file.txt username@192.168.1.10:/home/username/
```

### Download

```bash
scp username@192.168.1.10:/home/username/file.txt .
```

---

# Command History

## `history`

Displays previously executed commands.

```bash
history
```

Search history:

```bash
history | grep nmap
```

---

## Run Previous Command

```bash
!!
```

Example:

```bash
sudo !!
```

This reruns the previous command with `sudo`.

---

## History Expansion

Run a specific command:

```bash
!50
```

Runs command number 50 from history.

Use carefully, especially when previous commands contain sensitive information.

---

# Help and Documentation

## `man`

Displays the manual page for a command.

```bash
man ls
```

Example:

```bash
man chmod
```

Search within a manual:

```text
/keyword
```

Exit:

```text
q
```

---

## `--help`

Most commands provide a quick help screen.

```bash
ls --help
```

or:

```bash
nmap --help
```

---

## `info`

Displays GNU Info documentation where available.

```bash
info coreutils
```

---

## `apropos`

Searches manual-page descriptions.

```bash
apropos password
```

---

## `type`

Shows how the shell interprets a command.

```bash
type cd
```

Example:

```text
cd is a shell builtin
```

---

# Command Chaining

Commands can be combined using operators.

## `;`

Runs commands sequentially regardless of whether the previous command succeeds.

```bash
mkdir test; cd test
```

---

## `&&`

Runs the second command only if the first succeeds.

```bash
mkdir test && cd test
```

This is safer when the second command depends on the first.

---

## `||`

Runs the second command only if the first fails.

```bash
ping -c 1 192.168.1.10 || echo "Host unreachable"
```

---

## `&`

Runs a command in the background.

```bash
python server.py &
```

---

# Useful Security Commands

Linux commands are heavily used during security assessments, incident response, and system administration.

---

## Check Current User

```bash
whoami
```

---

## Check User Privileges

```bash
id
```

Look for groups such as:

```text
sudo
adm
docker
```

Membership in privileged groups can affect what a user can access or execute.

---

## Check Listening Services

```bash
sudo ss -lntup
```

This can reveal:

* Listening ports
* TCP services
* UDP services
* Associated processes

---

## Check Running Processes

```bash
ps aux
```

Filter:

```bash
ps aux | grep ssh
```

---

## Search Logs

Example:

```bash
grep "Failed password" /var/log/auth.log
```

This can help identify failed SSH login attempts on systems where that log file is used.

---

## Check File Permissions

```bash
ls -la
```

Look for unusual or overly permissive permissions.

---

## Find World-Writable Files

```bash
find / -type f -perm -002 2>/dev/null
```

This searches for files writable by others.

Use carefully because scanning the entire filesystem can be resource-intensive.

---

## Find SUID Files

SUID programs can execute with the privileges of their file owner.

Find SUID files:

```bash
find / -perm -4000 -type f 2>/dev/null
```

This is commonly used during authorized Linux privilege-assessment work.

---

## Check Scheduled Tasks

View the current user's cron jobs:

```bash
crontab -l
```

System-wide cron configuration may exist under:

```text
/etc/crontab
/etc/cron.d/
/etc/cron.daily/
/etc/cron.hourly/
/etc/cron.weekly/
/etc/cron.monthly/
```

---

## Check Open Files

`lsof` means **List Open Files**.

```bash
lsof
```

Find network connections:

```bash
sudo lsof -i
```

Specific port:

```bash
sudo lsof -i :80
```

---

## Check File Hashes

### MD5

```bash
md5sum file.txt
```

### SHA-256

```bash
sha256sum file.txt
```

Hashes can be used to verify file integrity.

For security-sensitive integrity checks, SHA-256 is generally preferred over MD5.

---

## Search for Sensitive Files

Example:

```bash
find /home -type f -name "*.conf" 2>/dev/null
```

Search text:

```bash
grep -rni "password" /home/kali/projects/ 2>/dev/null
```

Only perform searches on systems and data you are authorized to inspect.

---

## Check Authentication Logs

Depending on the distribution and logging configuration:

```bash
sudo less /var/log/auth.log
```

Some systems use other logging mechanisms, such as `journalctl`.

---

## `journalctl`

Reads systemd journal logs.

```bash
sudo journalctl
```

### Recent Logs

```bash
sudo journalctl -n 50
```

### Follow Logs

```bash
sudo journalctl -f
```

### SSH Service Logs

```bash
sudo journalctl -u ssh
```

---

# Important Linux Directories

Understanding the Linux filesystem is essential for administration and cybersecurity.

## `/`

The root of the filesystem.

Everything starts from `/`.

---

## `/home`

Contains normal users' home directories.

Example:

```text
/home/kali
```

---

## `/root`

Home directory of the root user.

```text
/root
```

Normal users usually cannot access it without sufficient privileges.

---

## `/etc`

Contains system configuration files.

Examples:

```text
/etc/passwd
/etc/shadow
/etc/hosts
/etc/ssh/
/etc/crontab
```

---

## `/var`

Contains variable data.

Examples:

```text
/var/log
/var/cache
/var/lib
```

Logs are commonly stored under:

```text
/var/log/
```

---

## `/tmp`

Temporary files.

```text
/tmp
```

---

## `/usr`

Contains many user-space programs, libraries, and shared data.

Common directories:

```text
/usr/bin
/usr/sbin
/usr/lib
```

---

## `/bin`

Essential user command binaries.

On modern distributions using merged `/usr`, `/bin` may be a symbolic link to `/usr/bin`.

---

## `/sbin`

System administration binaries.

On modern merged-/usr systems, this may also be a symbolic link into `/usr`.

---

## `/dev`

Contains device files.

Examples:

```text
/dev/null
/dev/sda
/dev/tty
```

---

## `/proc`

A virtual filesystem exposing information about processes and the kernel.

Example:

```bash
cat /proc/cpuinfo
```

---

## `/sys`

Provides information about devices, drivers, and the kernel.

---

## `/opt`

Often used for optional or third-party software.

---

## `/mnt`

Commonly used as a temporary mount point.

---

## `/media`

Commonly used for automatically mounted removable media.

---

# Practical Examples

## Example 1: Find Your Current Location

```bash
pwd
```

Then list everything:

```bash
ls -la
```

---

## Example 2: Create a Cybersecurity Project Structure

```bash
mkdir -p cybersecurity/{recon,scans,reports,notes}
```

Check:

```bash
tree cybersecurity
```

If `tree` is not installed:

```bash
find cybersecurity
```

---

## Example 3: Find Large Files

```bash
find /home -type f -size +100M 2>/dev/null
```

This can help identify files consuming significant disk space.

---

## Example 4: Monitor Authentication Logs

```bash
sudo tail -f /var/log/auth.log
```

Then, from another terminal, perform an authorized SSH login attempt.

The log can help demonstrate how authentication events are recorded.

---

## Example 5: Find Failed Login Attempts

```bash
sudo grep "Failed password" /var/log/auth.log
```

Count them:

```bash
sudo grep "Failed password" /var/log/auth.log | wc -l
```

---

## Example 6: Find Listening Ports

```bash
sudo ss -lntup
```

This can help answer:

> Which services are currently listening for network connections?

---

## Example 7: Check a Web Server

```bash
curl -I https://example.com
```

This displays HTTP response headers.

For example:

```text
HTTP/2 200
content-type: text/html
server: ...
```

Headers can provide useful information during authorized web security testing.

---

## Example 8: Search Configuration Files

```bash
find /etc -type f -name "*.conf" 2>/dev/null
```

Search for a specific configuration value:

```bash
grep -Rni "Listen" /etc/apache2/ 2>/dev/null
```

---

## Example 9: Calculate a File Hash

```bash
sha256sum suspicious_file
```

You can compare the resulting hash with a known trusted hash to determine whether the file contents have changed.

---

## Example 10: Inspect a Running Process

Find a process:

```bash
ps aux | grep nginx
```

Find its PID:

```bash
pgrep nginx
```

Inspect open files:

```bash
sudo lsof -p PID
```

---

# Linux Command Concepts to Remember

## Absolute Path

An absolute path starts from `/`.

Example:

```text
/home/kali/notes/file.txt
```

It identifies the location independently of the current directory.

---

## Relative Path

A relative path starts from the current directory.

Example:

```text
notes/file.txt
```

If the current directory is:

```text
/home/kali
```

then:

```text
notes/file.txt
```

refers to:

```text
/home/kali/notes/file.txt
```

---

## `.`

Represents the current directory.

```bash
./script.sh
```

---

## `..`

Represents the parent directory.

```bash
cd ..
```

---

## `~`

Represents the current user's home directory.

```bash
cd ~
```

---

## Wildcards

### `*`

Matches zero or more characters.

```bash
ls *.txt
```

Lists `.txt` files.

### `?`

Matches one character.

```bash
ls file?.txt
```

Could match:

```text
file1.txt
file2.txt
```

but not:

```text
file10.txt
```

### `[]`

Matches characters from a set.

```bash
ls file[123].txt
```

Could match:

```text
file1.txt
file2.txt
file3.txt
```

---

# Command Output and Exit Status

Linux commands return an exit status.

Usually:

```text
0 = success
non-zero = error/failure
```

Check the previous command's exit status:

```bash
echo $?
```

Example:

```bash
ls
echo $?
```

If `ls` succeeds:

```text
0
```

This concept is particularly important when writing Bash scripts.

---

# Standard Streams

Linux programs commonly use three standard streams.

| Stream   | Number | Purpose         |
| -------- | -----: | --------------- |
| `stdin`  |      0 | Standard input  |
| `stdout` |      1 | Standard output |
| `stderr` |      2 | Standard error  |

Example:

```bash
command > output.txt
```

is equivalent to:

```bash
command 1> output.txt
```

Error output:

```bash
command 2> error.txt
```

This concept is important for understanding pipes, redirection, and Bash scripting.

---

# Common Command Combinations

## List and Filter

```bash
ls -la | grep ".txt"
```

---

## Search and Count

```bash
grep "error" logfile.txt | wc -l
```

---

## Sort and Remove Duplicates

```bash
sort users.txt | uniq
```

---

## Sort by Frequency

```bash
sort users.txt | uniq -c | sort -nr
```

This is useful when analyzing repeated values.

---

## Find and Process

```bash
find . -type f -name "*.log" | wc -l
```

Counts `.log` files.

---

# Quick Reference

## Navigation

| Command  | Purpose                |
| -------- | ---------------------- |
| `pwd`    | Show current directory |
| `ls`     | List files             |
| `cd`     | Change directory       |
| `clear`  | Clear terminal         |
| `whoami` | Show current user      |

---

## File Management

| Command | Purpose                |
| ------- | ---------------------- |
| `touch` | Create file            |
| `mkdir` | Create directory       |
| `cp`    | Copy                   |
| `mv`    | Move/rename            |
| `rm`    | Remove                 |
| `rmdir` | Remove empty directory |

---

## File Viewing

| Command   | Purpose                |
| --------- | ---------------------- |
| `cat`     | Display file           |
| `less`    | Read large file        |
| `more`    | Read file page by page |
| `head`    | Show beginning         |
| `tail`    | Show end               |
| `tail -f` | Follow file changes    |

---

## Searching

| Command   | Purpose                     |
| --------- | --------------------------- |
| `find`    | Search filesystem           |
| `locate`  | Search file database        |
| `which`   | Locate executable           |
| `whereis` | Locate binary/source/manual |
| `grep`    | Search text                 |

---

## Text Processing

| Command | Purpose                 |
| ------- | ----------------------- |
| `grep`  | Search text             |
| `sort`  | Sort lines              |
| `uniq`  | Remove/count duplicates |
| `wc`    | Count lines/words/bytes |
| `cut`   | Extract fields          |
| `awk`   | Process structured text |
| `sed`   | Transform text          |

---

## Permissions

| Command | Purpose            |
| ------- | ------------------ |
| `chmod` | Change permissions |
| `chown` | Change owner       |
| `chgrp` | Change group       |
| `ls -l` | View permissions   |

---

## Users

| Command    | Purpose                      |
| ---------- | ---------------------------- |
| `whoami`   | Current user                 |
| `id`       | User/group information       |
| `who`      | Logged-in users              |
| `w`        | Logged-in users + activity   |
| `passwd`   | Change password              |
| `useradd`  | Create user                  |
| `userdel`  | Delete user                  |
| `usermod`  | Modify user                  |
| `groupadd` | Create group                 |
| `sudo`     | Run with elevated privileges |
| `su`       | Switch user                  |

---

## Processes

| Command | Purpose                     |
| ------- | --------------------------- |
| `ps`    | View processes              |
| `top`   | Monitor processes           |
| `htop`  | Interactive process monitor |
| `pgrep` | Find process                |
| `kill`  | Terminate process           |
| `pkill` | Terminate by name           |
| `jobs`  | View shell jobs             |
| `fg`    | Foreground job              |
| `bg`    | Background job              |

---

## System

| Command       | Purpose                     |
| ------------- | --------------------------- |
| `uname`       | Kernel/system information   |
| `hostname`    | Hostname                    |
| `hostnamectl` | System/hostname information |
| `date`        | Date/time                   |
| `uptime`      | System uptime               |
| `free`        | Memory usage                |
| `lscpu`       | CPU information             |
| `lsusb`       | USB devices                 |
| `lspci`       | PCI devices                 |
| `dmesg`       | Kernel messages             |

---

## Storage

| Command  | Purpose               |
| -------- | --------------------- |
| `df`     | Filesystem disk usage |
| `du`     | File/directory usage  |
| `lsblk`  | Block devices         |
| `mount`  | Mount filesystem      |
| `umount` | Unmount filesystem    |

---

## Networking

| Command      | Purpose                             |
| ------------ | ----------------------------------- |
| `ip`         | Network configuration               |
| `ping`       | Connectivity test                   |
| `ss`         | Network sockets                     |
| `netstat`    | Network connections                 |
| `traceroute` | Trace network path                  |
| `tracepath`  | Trace network path                  |
| `nslookup`   | DNS lookup                          |
| `dig`        | DNS queries                         |
| `host`       | DNS lookup                          |
| `curl`       | Transfer/test URLs                  |
| `wget`       | Download files                      |
| `nc`         | Network connections                 |
| `nmap`       | Network discovery/security auditing |

---

## Packages

| Command       | Purpose                    |
| ------------- | -------------------------- |
| `apt update`  | Update package information |
| `apt upgrade` | Upgrade packages           |
| `apt install` | Install package            |
| `apt remove`  | Remove package             |
| `apt search`  | Search packages            |
| `apt show`    | Show package information   |
| `dpkg`        | Manage Debian packages     |

---

## Archives

| Command  | Purpose                 |
| -------- | ----------------------- |
| `tar`    | Create/extract archives |
| `gzip`   | Compress                |
| `gunzip` | Decompress gzip         |
| `zip`    | Create ZIP archive      |
| `unzip`  | Extract ZIP archive     |

---

## Remote Access

| Command      | Purpose              |
| ------------ | -------------------- |
| `ssh`        | Remote secure shell  |
| `ssh-keygen` | Generate SSH keys    |
| `scp`        | Secure file transfer |

---

## Logs and Security

| Command      | Purpose                    |
| ------------ | -------------------------- |
| `journalctl` | View systemd logs          |
| `tail -f`    | Monitor changing logs      |
| `lsof`       | List open files            |
| `sha256sum`  | Calculate SHA-256 hash     |
| `md5sum`     | Calculate MD5 hash         |
| `find`       | Search files               |
| `grep`       | Search log contents        |
| `ss`         | Inspect listening services |
| `ps`         | Inspect processes          |

---

# Essential Commands to Learn First

If you are completely new to Linux, learn these commands in this order:

```text
pwd
ls
cd
mkdir
touch
cp
mv
rm
cat
less
head
tail
find
grep
chmod
chown
whoami
id
sudo
ps
top
df
du
ip
ping
ss
curl
apt
tar
ssh
```

Once these are comfortable, move on to:

```text
awk
sed
cut
sort
uniq
xargs
lsof
journalctl
dig
nc
nmap
```

These commands form a strong foundation for Linux administration, Bash scripting, SOC work, VAPT, penetration testing, and cybersecurity labs.

---

# Final Concept

Linux command-line skills are not about memorizing hundreds of commands.

The important skill is understanding how commands can be combined.

For example:

```bash
grep "Failed password" /var/log/auth.log | sort | uniq -c | sort -nr
```

This combines:

```text
grep
  ↓
sort
  ↓
uniq
  ↓
sort
```

Each command performs one task, and the output becomes the input for the next command.

This is one of the fundamental ideas behind Linux command-line workflows and is also the foundation for effective Bash scripting.
