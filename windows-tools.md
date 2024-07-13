# Windows IT Notes

- [system Information](##system-information)
- [Registry Editor](##registry-editor)
- [Resource Monitor](##resource-monitor)
- [system Configuration](##system-configuration)
- [Disk Management](##disk-management)
- [Disk Cleanup](##disk-cleanup)
- [Disk Defragmentation](##disk-defragmentation)
- [Task scheduler](##task-scheduler)
- [Computer Management](##computer-management)
- [Management Console](##management-console)
- [safe Mode](##safe-mode)

## system Information
Can be run w/ `msinfo32.exe`
- Provides computer information:
    - hardware resources: Os, how much memory installed etc
    - components: display settings, network configs
    - software environment: hardware drivers, pending print jobs, current running jobs

## Registry Editor
Can be run w/ `regedit.exe`
- Registry contains application, Os, and hardware configuration 
- Creates a central "organised" registry for configuration files etc, instead of individual .ini files or other config files
- For stuff like how something should operate, user preferences, settings, device driver configs etc
- Quite scattered
- NOTE: Doesn't delete data from uninstalled applications

## Resource Monitor
Can be run w/ `resmon.exe`
- Detailed real-time view on performance (CPU, Disk, Network, Memory)
- More detailed than Task Manager Performance's tab

## system Configuration
Can be run w/ `msconfig.exe`
- Managing boot processes (eg. safe boot), startup of services/applications (has been moved to Task Manager instead), services

## Disk Management
Can be run w/ `diskmgmt.msc`
- see all disks and partitions
- Used to format and partition disks
- TIP: disks partition also has Recovery Partition. If you have 2 partitions for storage on 1 disk, depending on where they are located, it may not be possible to give partition space to each other w/out reformatting the drive

## Disk Cleanup
Can be run w/ `cleanmgr.exe`
- Find unused/unneeded files on disk and cleans them

## Disk Defragmentation
Can be run w/ `dfrgui.exe` or drive properties
CLI version (requires elevation): defrag 'volume'  (defrag C:)
- For HDD (not ssd, as HDD is spinning)
- Takes scattered pieces of files all over drive and puts them into one single area of drive (hence why drives need file system) -> increases speed
- NOTE: HDD defragmenting is automatic in Windows 10 and up and done on regular basis (unless disabled, not recommended), so if HDD is slow, it probably isn't this issue

## Task scheduler
Can be run w/ `taskschd.mc`
- Tell Windows to do something at specified time (run backup script every night at certain time, or launch specific program at specific time)
- A lot of the times when you install an application, if it has inbuilt updater, it’ll automatically come into windows task schedular as a task (e.g. Norton auto updater in image below)

## Computer Management 
Can be run w/ `compmgmt.msc`
- Administrative tool allows management of local and remote computers and shares

## Management Console
Can be run w/ `mmc`
- snap in to manage local and connected devices (Allows customisation)
- Lot of options for snap-ins, computer management is an instance of management console

## safe Mode
How to access:
- Access via settings>update & security>recovery
- Hold shift while restarting, then select Troubleshoot>Advanced options>startup settings>Restart (May require Bitlocker key), then select startup setting desired
- Can exit safe mode by restarting PC/clear safe boot checkbox from msconfig
\nPurpose:
- Boot windows in simple state (only basic drivers)
- Most bootup software is not in memory
    - so if no problems, problem might not be windows but loaded w/ windows itself
- If in standard windows, deleting windows file may not work cause windows is using it, safe mode can delete/rename file that wasn’t possible in normal Windows most of the time (also good if can't get into Windows normal environment due to problems/malware)

