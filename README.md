# Linux-Basic-Commands && Windows

## Commands in Ubuntu

### Package Management and System
- `apt policy <package name>`: Searches for a package in Ubuntu's repository.
- `lsb_release -a`: Displays information about the operating system.
- `uname -a`: Displays system information.
- `uname -r`: Displays kernel information.
- `getent passwd`: Lists system users.
- `journalctl -b`: Displays logs from the last system boot.
- `systemctl restart`: Restarts a service.
- `systemctl poweroff`: Shuts down the system.
- `reboot` or `shutdown -r now`: Restarts the system.
- `shutdown`: Shuts down the system safely.
- `poweroff`: Turns off the computer immediately.

### Hardware Information
- `lscpu`: Displays processor information.
- `free -h`: Displays memory usage in a readable format.
- `tty`: Shows the terminal in use.

### Networking
- `ip a`: Displays assigned IP addresses.
- `ip r`: Displays the routing table.
- `resolvectl status`: Displays information about name resolution.
- `dhclient -r`: Releases the assigned IP.
- `dhclient -v -s <network name>`: Obtains a new IP.

### File and Directory Management
- `pwd`: Displays the current directory.
- `ls -l`: Lists files with details.
- `ls -a`: Shows hidden files.
- `ls -h`: Displays file sizes in a readable format.
- `ls -R`: Recursively lists all contents of a directory.
- `mv <file> <new_name>`: Renames a file.
- `cp <source> <destination>`: Copies a file or directory.
- `cp -R <source> <destination>`: Recursively copies a directory.
- `rm -r <directory/*>`: Deletes all files in a directory without deleting the directory itself.
- `nano <file>`: Opens or creates a file using the Nano editor.
- `cat <file>`: Displays the contents of a file.
- `head <file>`: Displays the first lines of a file.
- `tail <file>`: Displays the last lines of a file.
- `diff <file1> <file2>`: Shows differences between two files.

### Users and Permissions
- `whoami`: Displays the current user.
- `id`: Displays user and group information.
- `chmod <permissions> <file>`: Modifies file permissions.
- `chown <user>:<group> <file>`: Changes the owner of a file or directory.
- `addgroup <group>`: Creates a new group.
- `sticky bit`: Restricts file deletion to the file owner.

### Aliases and Shell Customization
- `alias <alias_name>=’<command>`: Creates an alias.
- `unalias <alias_name>`: Removes an alias.
- `exec bash`: Reloads the shell.
- `apropos <word>`: Shows commands related to a keyword.
- `whatis <command>`: Displays a brief description of a command.

### Redirections and Filters
- `>`: Redirects standard output to a file (overwrites if it exists).
- `>>`: Redirects standard output to a file (appends to the existing content).
- `<`: Redirects standard input from a file.
- `<<`: Allows multiple-line input into a command until a delimiter is found.
- `cat /dev/null`: Empties a file.
- `tail -f /var/log/syslog`: Displays real-time logs.
- `grep <pattern> <file>`: Searches for a pattern in a file.
- `sort -t: -k2 -n`: Sorts by numbers in the second column.
- `sort -u`: Removes duplicate lines.
- `dmesg`: Displays direct system processes.
- `join <file1> <file2>`: Merges files with common fields.

### Compressed File Management
- `tar -cvf <file.tar> <directory>`: Creates a compressed file.
- `tar -xvf <file.tar>`: Extracts a compressed file.
- `tar -zxvf <file.tar.gz>`: Extracts a gzip compressed file.

## Task Scheduling and Automation

### Scheduled Tasks in Linux (Cron and At)
- `at <hour/minute> <month/day/year>`: Schedules a task at a specific time.
- `cron`: Schedules periodic tasks.
- `mesg yes`: Enables system messages.
- `wall <message>`: Sends a message to all logged-in users.
- `notify-send <message>`: Sends a graphical notification.

## Linux File Structure

- `/bin`: Contains essential commands.
- `/boot`: Contains boot files.
- `/dev`: Contains device files.
- `/etc`: Configuration files.
- `/home`: User directories.
- `/var`: Variable data, such as logs.
- `/lib`: Shared libraries.
- `/media`: Mount point for external devices.
- `/mnt`: Mount point for additional disks.
- `/opt`: Third-party applications.
- `/proc`: System process information.
- `/sbin`: Essential commands for administrators.
- `/srv`: Service-related data.
- `/sys`: System information.
- `/usr`: Non-essential applications and utilities.

## File Download in Linux
- `wget <URL>`: Downloads a file from a URL.
- `curl <URL>`: Fetches content from a URL.

## Disk Space Management
- `df -h`: Displays disk usage in a human-readable format (GB, MB).
- `df -i`: Shows inode usage on the disk.
- `du -sh <path>`: Displays the total size of a specific directory.
- `du -h --max-depth=1 <path>`: Lists the sizes of subdirectories.

## Disk and Partition Status
- `lsblk`: Shows disks and partitions in a tree format.
- `fdisk -l`: Lists available disk partitions.
- `blkid`: Displays UUID and filesystem type of disks.
- `mount | column -t`: Shows currently mounted filesystems.
- `cat /etc/fstab`: Lists partitions mounted at boot.

## Disk Health and Performance
- `smartctl -a /dev/sdX`: Displays S.M.A.R.T. information (requires `smartmontools`).
- `iostat -dx 1`: Monitors disk activity (requires `sysstat`).
- `hdparm -I /dev/sdX`: Shows detailed disk information.

## Finding Large Files
- `find / -type f -size +1G`: Searches for files larger than 1GB.
- `du -ah / | sort -rh | head -n 10`: Displays the 10 largest files/directories.

## File System Maintenance
- `fsck /dev/sdX`: Checks and repairs a filesystem.
- `tune2fs -l /dev/sdX`: Displays information about an ext4 filesystem.
- `mkfs.ext4 /dev/sdX`: Formats a partition as ext4 (**Warning!** This erases all data).

## Linux File Structure
- `/bin`: Contains essential commands.
- `/boot`: Contains boot files.
- `/dev`: Contains device files.
- `/etc`: Configuration files.
- `/home`: User directories.
- `/var`: Variable data, such as logs.
- `/lib`: Shared libraries.
- `/media`: Mount point for external devices.
- `/mnt`: Mount point for additional disks.
- `/opt`: Third-party applications.
- `/proc`: System process information.
- `/sbin`: Essential commands for administrators.
- `/srv`: Service-related data.
- `/sys`: System information.
- `cat /etc/fstab`: Lists partitions mounted at boot.

Example /etc/fstab entry: 
```bash
UUID=xxxx-xxxx  /mnt/data  ext4  defaults  0  2
```
## Commands in Windows

### Networking
- `ipconfig /all`: Displays network information.
- `ping 8.8.8.8`: Tests connectivity to Google.
- `ping google.com`: Tests DNS resolution.
- `nslookup <domain>`: Looks up the IP of a domain.
- `route print`: Displays the routing table.
- `ipconfig /release`: Releases the IP.
- `ipconfig /renew`: Renews the IP.

### System Information
- `winver`: Displays the Windows version.

This document contains a compilation of useful commands for both Linux (Ubuntu) and Windows, including package management, networking, file operations, and task automation.
