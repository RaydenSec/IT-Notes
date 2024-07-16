# Useful Windows CLI Commands 

- [Windows Path](##windows-path)
- [System Info](##system-info)
- [dir](##dir)
- [del](##del)
- [ping](##ping)
- [tracert](##tracert)
- [pathping](##pathping)
- [netstat](##netstat)
- [nslookup](##nslookup)
- [net](##net)
- [explorer.exe](##explorer.exe)
- [Unix Parallels](##Unix-parallels)

## Windows Path
- Each partition is assigned a drive letter (eg. `C:`)
- drive letters can be assigned to partitions and seperate drives
- Can reference drive  using `D:`, when copying into it, listing it, full path etc
- Example of Windows path: `C:\Users\Mickey`

## System Info
`systeminfo`
- An alternative to `msinfo32.exe`, gives extensive details on windows system
- Difference: `msinfo32.exe` is a GUI version, while `systeminfo` is for CLI. So the latter is for speed, whilst the prior is for readability

## dir
`dir`
- lists contents of current directory (displays if directory or file and shows file extension)
- Works the same as Unix `ls` -> eg. can `dir Downloads`

## del
`del`
- Same as `rm`
- (How to del non-empty directory?)

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

## Unix Parallels
- `mkdir`, `rmdir`, `cd`
