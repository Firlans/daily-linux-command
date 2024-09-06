# 🐧 Linux Commands Cheatsheet

## 📁 File and Directory Operations

### Change Directory
```bash
cd <directory>
```
**Tip:** Use `cd ..` to go up one level, `cd ~` to go to home directory.

### Copy File
```bash
cp <source> <destination>
```
**Tip:** Use `-r` flag for copying directories: `cp -r <source_dir> <destination_dir>`

### Create Folder
```bash
mkdir <folder name>
```
**Tip:** Use `-p` flag to create parent directories: `mkdir -p path/to/new/folder`

### Remove Folder
```bash
rmdir <folder name>
```
**Warning:** Use `rm -r <folder name>` to remove non-empty directories (use with caution!)

### Show Items in Directory
```bash
ls
```
**Useful flags:**
- `-l`: Long format
- `-a`: Show hidden files
- `-h`: Human-readable file sizes

### Show Current Working Directory
```bash
pwd
```

### Move or Rename File
```bash
mv <source> <destination>
```

## 📝 File Content Operations

### View File Content
```bash
cat <filename>
```

### Edit File
```bash
nano <filename>
```
or
```bash
vim <filename>
```

### Search File Content
```bash
grep <pattern> <filename>
```

## 👤 User and Permissions

### Change File Permissions
```bash
chmod <permissions> <filename>
```

#### Understanding Permissions

Permissions in Linux are represented by three sets of characters:
- Owner permissions
- Group permissions
- Others permissions

Each set can have read (r), write (w), and execute (x) permissions.

#### Numeric Representation

Permissions can be set using numbers:
- 4: Read permission
- 2: Write permission
- 1: Execute permission

Common permission combinations:
- 7 (4+2+1): Full permissions (read, write, execute)
- 6 (4+2): Read and write
- 5 (4+1): Read and execute
- 4: Read only
- 0: No permissions

Example:
```bash
chmod 755 file.txt
```
This sets read, write, execute (7) for the owner, and read and execute (5) for group and others.

#### Symbolic Representation

You can also use symbolic notation:
- u: Owner
- g: Group
- o: Others
- a: All (owner, group, others)

Operations:
- +: Add permission
- -: Remove permission
- =: Set exact permission

Example:
```bash
chmod u+x,go-w file.txt
```
This adds execute permission for the owner and removes write permission for group and others.

### Change File Owner
```bash
chown <user>:<group> <filename>
```

Example:
```bash
chown john:developers file.txt
```
This changes the owner of file.txt to 'john' and the group to 'developers'.

### View File Permissions
```bash
ls -l <filename>
```
This shows detailed information including permissions, owner, and group.```

## 🖥️ System Information

### Display System Information
```bash
uname -a
```

### Check Disk Usage
```bash
df -h
```

### Check Memory Usage
```bash
free -h
```

## 🌐 Network

### Check IP Address
```bash
ip addr show
```

### Test Network Connectivity
```bash
ping <hostname or IP>
```

## 📦 Package Management (for Debian-based systems)

### Update Package List
```bash
sudo apt update
```

### Upgrade Packages
```bash
sudo apt upgrade
```

### Install a Package
```bash
sudo apt install <package name>
```

Remember: Always be cautious when using commands that modify your system. When in doubt, read the manual (`man <command>`) or use the `--help` flag for more information.