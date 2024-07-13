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


## Task scheduler
Can be run w/ `taskschd.mc`
-	Tell Windows to do something at specified time (run backup script every night at certain time, or launch specific program at specific time)
-	A lot of the times when you install an application, if it has inbuilt updater, it’ll automatically come into windows task schedular as a task (e.g. Norton auto updater in image below)



test [here](#Task-scheduler)
