# Linux Command Cheat Sheet

A practical, organized reference for daily terminal usage. Assume a Linux shell (bash/zsh).

Copy tip: Each row includes a right-side Copy column that repeats the command for quick selection. Many Markdown renderers (GitHub and VS Code) also show a copy button on code blocks.

---

## 1) Navigation and Directory Management

| Command | Purpose | Copy |
| --- | --- | --- |
| `cd` | Go to home directory | `cd` |
| `cd ..` | Go up one level | `cd ..` |
| `cd -` | Go to previous directory | `cd -` |
| `cd /path/to/dir` | Go to a specific path | `cd /path/to/dir` |
| `pwd` | Show current directory | `pwd` |
| `ls` | List files and directories | `ls` |
| `ls -l` | Long listing | `ls -l` |
| `ls -a` | Show hidden files | `ls -a` |
| `ls -lh` | Human readable sizes | `ls -lh` |
| `ls -la` | Common detailed view | `ls -la` |
| `ls -lt` | Sort by modified time | `ls -lt` |
| `tree` | Display directory structure | `tree` |
| `sudo apt install tree` | Install tree | `sudo apt install tree` |
| `mkdir folder` | Create directory | `mkdir folder` |
| `mkdir -p a/b/c` | Create nested dirs | `mkdir -p a/b/c` |
| `mkdir -p website/static/{css,js}` | Create multiple dirs | `mkdir -p website/static/{css,js}` |
| `rmdir folder` | Remove empty directory | `rmdir folder` |
| `pushd dir` | Save current dir and move | `pushd dir` |
| `popd` | Return to last dir | `popd` |

---

## 2) File Creation, Copy, Move, and Delete

| Command | Purpose | Copy |
| --- | --- | --- |
| `touch file.txt` | Create empty file or update timestamp | `touch file.txt` |
| `rm file.txt` | Delete a file | `rm file.txt` |
| `rm -r folder/` | Delete a directory recursively | `rm -r folder/` |
| `rm -rf folder/` | Force delete (dangerous) | `rm -rf folder/` |
| `cp file1 file2` | Copy file | `cp file1 file2` |
| `cp -r dir1 dir2` | Copy directory recursively | `cp -r dir1 dir2` |
| `cp -a dir1 dir2` | Preserve attributes | `cp -a dir1 dir2` |
| `mv old.txt new.txt` | Rename file | `mv old.txt new.txt` |
| `mv file.txt folder/` | Move file | `mv file.txt folder/` |
| `mv -i file.txt folder/` | Prompt before overwrite | `mv -i file.txt folder/` |
| `stat file.txt` | Detailed file info | `stat file.txt` |
| `file script.sh` | Detect file type | `file script.sh` |

---

## 3) File Viewing and Editing

| Command | Purpose | Copy |
| --- | --- | --- |
| `cat file.txt` | View a file | `cat file.txt` |
| `less file.txt` | Scrollable view | `less file.txt` |
| `more file.txt` | Basic pager | `more file.txt` |
| `head file.txt` | First lines | `head file.txt` |
| `tail file.txt` | Last lines | `tail file.txt` |
| `tail -f logfile.log` | Live log monitoring | `tail -f logfile.log` |
| `nl file.txt` | Show line numbers | `nl file.txt` |
| `nano file.txt` | Editor (beginner) | `nano file.txt` |
| `vi file.txt` | Editor (vi) | `vi file.txt` |
| `vim file.txt` | Editor (vim) | `vim file.txt` |

---

## 4) Searching and Text Processing

| Command | Purpose | Copy |
| --- | --- | --- |
| `grep word file.txt` | Search text | `grep word file.txt` |
| `grep -i word file.txt` | Case insensitive search | `grep -i word file.txt` |
| `grep -r word folder/` | Recursive search | `grep -r word folder/` |
| `find . -name "*.txt"` | Find files by name | `find . -name "*.txt"` |
| `find / -size +100M` | Find large files | `find / -size +100M` |
| `wc file.txt` | Word/line/byte count | `wc file.txt` |
| `sort file.txt` | Sort lines | `sort file.txt` |
| `uniq file.txt` | Remove duplicates | `uniq file.txt` |
| `cut -d":" -f1 /etc/passwd` | Column extract | `cut -d":" -f1 /etc/passwd` |
| `awk '{print $1}' file.txt` | Print first column | `awk '{print $1}' file.txt` |
| `sed 's/old/new/g' file.txt` | Replace text | `sed 's/old/new/g' file.txt` |
| `xargs` | Build commands from input | `xargs` |
| `tr -d '\r' file.txt` | Remove CR characters | `tr -d '\r' file.txt` |

---

## 5) System Info and Hardware

| Command | Purpose | Copy |
| --- | --- | --- |
| `uname -a` | Kernel and system info | `uname -a` |
| `hostname` | System hostname | `hostname` |
| `df -h` | Disk usage | `df -h` |
| `du -sh folder/` | Folder size | `du -sh folder/` |
| `free -h` | Memory usage | `free -h` |
| `lsblk` | Storage devices | `lsblk` |
| `mount` | Mounted filesystems | `mount` |
| `lscpu` | CPU info | `lscpu` |

---

## 6) Process and Resource Management

| Command | Purpose | Copy |
| --- | --- | --- |
| `ps aux` | List processes | `ps aux` |
| `top` | Live process view | `top` |
| `htop` | Better top (install separately) | `htop` |
| `kill PID` | Kill a process | `kill PID` |
| `killall process_name` | Kill by name | `killall process_name` |
| `uptime` | System uptime | `uptime` |
| `watch df -h` | Watch disk usage | `watch df -h` |
| `jobs` | List background jobs | `jobs` |
| `bg` | Resume job in background | `bg` |
| `fg` | Bring job to foreground | `fg` |

---

## 7) Permissions and Users

| Command | Purpose | Copy |
| --- | --- | --- |
| `chmod 755 file.sh` | Set permissions | `chmod 755 file.sh` |
| `chmod u+x file.sh` | Add execute bit | `chmod u+x file.sh` |
| `chown user:group file.txt` | Change ownership | `chown user:group file.txt` |
| `whoami` | Current user | `whoami` |
| `who` | Logged in users | `who` |
| `id` | User and groups | `id` |
| `su` | Switch user | `su` |
| `sudo command` | Run as root | `sudo command` |

---

## 8) Networking

| Command | Purpose | Copy |
| --- | --- | --- |
| `ip a` | Show interfaces | `ip a` |
| `ip r` | Show routes | `ip r` |
| `ping google.com` | Connectivity test | `ping google.com` |
| `traceroute google.com` | Route trace | `traceroute google.com` |
| `ss -tuln` | Listening sockets | `ss -tuln` |
| `netstat -tuln` | Legacy sockets view | `netstat -tuln` |
| `curl https://example.com` | HTTP request | `curl https://example.com` |
| `wget https://example.com/file.zip` | Download a file | `wget https://example.com/file.zip` |

---

## 9) Package Management (APT)

| Command | Purpose | Copy |
| --- | --- | --- |
| `sudo apt update` | Refresh package lists | `sudo apt update` |
| `sudo apt upgrade` | Upgrade packages | `sudo apt upgrade` |
| `sudo apt install package-name` | Install package | `sudo apt install package-name` |
| `sudo apt remove package-name` | Remove package | `sudo apt remove package-name` |
| `sudo apt autoremove` | Remove unused deps | `sudo apt autoremove` |
| `sudo apt clean` | Clear cache | `sudo apt clean` |

---

## 10) Archives and Compression

| Command | Purpose | Copy |
| --- | --- | --- |
| `tar -cvf archive.tar folder/` | Create tar | `tar -cvf archive.tar folder/` |
| `tar -xvf archive.tar` | Extract tar | `tar -xvf archive.tar` |
| `gzip file.txt` | Compress gzip | `gzip file.txt` |
| `gunzip file.txt.gz` | Decompress gzip | `gunzip file.txt.gz` |
| `zip archive.zip file.txt` | Create zip | `zip archive.zip file.txt` |
| `unzip archive.zip` | Extract zip | `unzip archive.zip` |

---

## 11) Environment and Shell

| Command | Purpose | Copy |
| --- | --- | --- |
| `echo "Hello World"` | Print text | `echo "Hello World"` |
| `env` | Show environment | `env` |
| `export VAR=value` | Set env var | `export VAR=value` |
| `history` | Command history | `history` |
| `clear` | Clear screen | `clear` |
| `alias ll='ls -la'` | Create alias | `alias ll='ls -la'` |
| `source ~/.bashrc` | Reload shell config | `source ~/.bashrc` |
| `which python` | Locate executable | `which python` |
| `whereis bash` | Find binary and man page | `whereis bash` |

---

## 12) Documentation and Help

| Command | Purpose | Copy |
| --- | --- | --- |
| `man ls` | Manual page | `man ls` |
| `ls --help` | Built in help | `ls --help` |
| `info ls` | Info docs | `info ls` |
| `tldr ls` | Quick help (install tldr) | `tldr ls` |

---

## Pro Tips

| Tip | Why it helps | Copy |
| --- | --- | --- |
| Use Tab for auto completion | Faster commands | `Tab` |
| Use `Ctrl + R` to search history | Find previous commands | `Ctrl + R` |
| Use `&&` to chain commands | Run next only if previous succeeds | `&&` |
| Avoid `rm -rf /` | Prevent catastrophic delete | `rm -rf /` |

---

Tip: Bookmark this repo and revisit often. Mastery comes from daily terminal usage, not memorization.
