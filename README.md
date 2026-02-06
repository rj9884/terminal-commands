# Linux Command Cheat Sheet

A practical, organized reference for daily terminal usage. Assume a Linux shell (bash/zsh).

## 1) Navigation and Directory Management

- `cd` change directory
  - `cd`                      # home directory
  - `cd ..`                   # up one level
  - `cd -`                    # previous directory
  - `cd /path/to/dir`
- `ls` list files and directories
  - `ls`
  - `ls -l`                   # long listing
  - `ls -a`                   # include hidden files
  - `ls -lh`                  # human-readable sizes
- `pwd` print working directory
  - `pwd`
- `tree` display directory structure
  - `tree`
  - `sudo apt install tree`
- `mkdir` create directories
  - `mkdir folder`
  - `mkdir -p a/b/c`
  - `mkdir -p website/static/{css,js}`
- `rmdir` remove empty directory
  - `rmdir folder`
- `pushd` and `popd` directory stack
  - `pushd dir`               # save current dir and move
  - `popd`                    # return to last dir
- Useful additions
  - `ls -la`                  # common detailed view
  - `ls -lt`                  # sort by modified time

## 2) File Creation, Copy, Move, and Delete

- `touch` create empty file or update timestamp
  - `touch file.txt`
- `rm` delete files/directories (dangerous)
  - `rm file.txt`
  - `rm -r folder/`
  - `rm -rf folder/`          # force delete (dangerous)
- `cp` copy files/directories
  - `cp file1 file2`
  - `cp -r dir1 dir2`
  - `cp -a dir1 dir2`          # preserve attributes
- `mv` move or rename
  - `mv old.txt new.txt`
  - `mv file.txt folder/`
  - `mv -i file.txt folder/`   # prompt before overwrite
- `stat` detailed file info
  - `stat file.txt`
- `file` detect file type
  - `file script.sh`

## 3) File Viewing and Editing

- View files
  - `cat file.txt`
  - `less file.txt`
  - `more file.txt`
- Partial viewing
  - `head file.txt`
  - `tail file.txt`
  - `tail -f logfile.log`      # live log monitoring
- Editors
  - `nano file.txt`            # beginner-friendly
  - `vi file.txt`
  - `vim file.txt`             # advanced editor
- Quick file preview
  - `nl file.txt`              # show line numbers

## 4) Searching and Text Processing

- `grep` search text
  - `grep word file.txt`
  - `grep -i word file.txt`    # case-insensitive
  - `grep -r word folder/`     # recursive
- `find` search files
  - `find . -name "*.txt"`
  - `find / -size +100M`
- Text utilities
  - `wc file.txt`              # word/line/byte count
  - `sort file.txt`
  - `uniq file.txt`
  - `cut -d":" -f1 /etc/passwd`
- Powerful tools
  - `awk '{print $1}' file.txt`
  - `sed 's/old/new/g' file.txt`
- Useful additions
  - `xargs`                    # build commands from input
  - `tr -d '\r' file.txt`      # remove CR characters

## 5) System Info and Hardware

- `uname -a`                   # kernel and system info
- `hostname`                   # system hostname
- Disk and memory
  - `df -h`                    # disk usage
  - `du -sh folder/`           # folder size
  - `free -h`                  # memory usage
- Storage devices
  - `lsblk`
  - `mount`
- CPU info
  - `lscpu`

## 6) Process and Resource Management

- Process listing
  - `ps aux`
  - `top`
  - `htop`                     # better top (install separately)
- Kill processes
  - `kill PID`
  - `killall process_name`
- Monitoring
  - `uptime`
  - `watch df -h`
- Background jobs
  - `jobs`
  - `bg`
  - `fg`

## 7) Permissions and Users

- Permissions
  - `chmod 755 file.sh`
  - `chmod u+x file.sh`        # add execute bit
- Ownership
  - `chown user:group file.txt`
- User info
  - `whoami`
  - `who`
  - `id`
- Switch user
  - `su`
  - `sudo command`

## 8) Networking

- Interfaces and routes
  - `ip a`
  - `ip r`
- Connectivity
  - `ping google.com`
  - `traceroute google.com`
- Networking tools
  - `ss -tuln`
  - `netstat -tuln`
- Web requests
  - `curl https://example.com`
  - `wget https://example.com/file.zip`

## 9) Package Management (APT)

- `sudo apt update`
- `sudo apt upgrade`
- `sudo apt install package-name`
- `sudo apt remove package-name`
- Cleanup
  - `sudo apt autoremove`
  - `sudo apt clean`

## 10) Archives and Compression

- TAR
  - `tar -cvf archive.tar folder/`
  - `tar -xvf archive.tar`
- GZIP
  - `gzip file.txt`
  - `gunzip file.txt.gz`
- ZIP
  - `zip archive.zip file.txt`
  - `unzip archive.zip`

## 11) Environment and Shell

- Basics
  - `echo "Hello World"`
  - `env`
  - `export VAR=value`
  - `history`
  - `clear`
- Aliases
  - `alias ll='ls -la'`
- Shell config
  - `source ~/.bashrc`
- Useful additions
  - `which python`             # locate executable
  - `whereis bash`             # find binary, source, and man page

## 12) Documentation and Help

- `man ls`
- `ls --help`
- `info ls`
- Quick command lookup
  - `tldr ls`                  # install tldr

## Pro Tips

- Use Tab for auto-completion
- Use `Ctrl + R` to search command history
- Use `&&` to chain commands
- Avoid `rm -rf /`

---

Tip: Bookmark this repo and revisit often. Mastery comes from daily terminal usage, not memorization.
