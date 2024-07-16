# Useful Windows CLI Commands 

# System
- [Windows Path](##windows-path)
- [Windows Version](##windows-version)
- [System Info](##system-info)
- [hostname](##hostname)
- [dir](##dir)
- [del](##del)
- [format](##format)
- [Disk Partition](##disk-partition)
- [Copy Single File](##copy-single-file)
- [Check File System](##check-file-system)
- [Scan All Protected System Files](##scan-all-protected-system-files)

# Network
- [ping](##ping)
- [tracert](##tracert)
- [pathping](##pathping)
- [netstat](##netstat)
- [nslookup](##nslookup)
- [net](##net)
- [explorer.exe](##explorer.exe)
- [shutdown](##shutdown)
- [Unix Parallels](##unix-parallels)
- [Misc Notes](##misc-notes)

# System

## Windows Path
- Each partition is assigned a drive letter (eg. `C:`)
- drive letters can be assigned to partitions and seperate drives
- Can reference drive  using `D:`, when copying into it, listing it, full path etc
- Example of Windows path: `C:\Users\Mickey`

## Windows Version
`winver`
- Find information on windows version (great for troubleshooting to check if latest patches or updates are installed)

## System Info
`systeminfo`
- An alternative to `msinfo32.exe`, gives extensive details on windows system
- Difference: `msinfo32.exe` is a GUI version, while `systeminfo` is for CLI. So the latter is for speed, whilst the prior is for readability

## hostname
`hostname`
- Displays Windows device name
- When you have multiple CLIs on screen for different devices, useful to check which CLI is for which Windows Device

## dir
`dir`
- lists contents of current directory (displays if directory or file and shows file extension)
- Works the same as Unix `ls` -> eg. can `dir Downloads`

## del
`del`
- Same as `rm`
- (How to del non-empty directory?)

## format
`format` [Drive] 
- Formats a drive (Wipes disk -> low level or high level? Recoverability?)
- eg. `format G:`
- Can specify file system type (eg. Fat32)

## Disk Partition
`diskpart`
- Creates partition from an avaiable disk
- Can be used to format (can use instead of `format`),list, modify, delete volumes etc.
- Of course, will requrie elevation

## Copy Single File

## Check File System
`chkdsk`

## Scan All Protected System Files
`sfc`

# Network

## ping

## tracert

## pathping

## netstat
`netstsat`
- shows active network connections (IPv4/6 on system (w/out tags -> TCP connections)
Tags:
- -a -> Shows all active connections
- -b -> Shows what application is used to send and receive data (requires admin) (Can run this before and after opening an application)
- -n -> Do not resolve names, only IP

## nslookup
`nslookup` [domain name]
- Lookup info from DNS servers, and displays info on IP addresses, cache timers etc.
- Multiple IP addresses -> because multiple DNS servers for redundancy

## net

## explorer.exe
`explorer.exe [path]` 
- Opens directory in file explorer of specificied path (eg. `explorer.exe .` opens pwd)

## shutdown
`shutdown`
- Shutdown/restart computer
Tags:
- `shutdown /s` -> Shutdown
- `shutdown /r` -> Restart
- `shutdown /s /t 90` -> Shutdown in 90 seconds
- `shutdown /a` -> Abort Shutdown/Restart timer

## Unix Parallels
- `mkdir`, `rmdir`, `cd`

## Misc Notes
- Opening CLI w/out running as admin, opens you in user home directory
- As admin, can go to other user's directories and do stuff to their files, but not as normal user
