# Windows General Tips

# File System Explained
- [Windows Filesystem Lamen's Terms](##windows-filesystem-lamen's-terms)
- [Windows Fileystem History](##windows-filesystem-history)
- [Good Practice](##good-practice)
- [Public Users Folder](##public-users-folder)
- [32 and 64bit identification](##32-64bit)
- [File system Types](##file-system-types)

# Sysadmin Stuff
- [Permissions](##permissions)
- [Hidden Files](##hidden-files)
- [Different Application Data Store Locations](##different-application-data-store-locations)
- [Windows Directory](##windows-directory)
- [Windows Folder](##windows-folder)

# Mac 
- [MacOs File Types](##macos-file-types)
- [MacOs Equivalent stuff](##macos-equivalent_stuff)

## Windows Filesystem Lamen's Terms
Every device has a filesyste -> phone, laptop, storage drives etc.
A computer has a drive, or more drives can be installed. If drives had data before, it has been formatted. Each drive can be partitioned, so that one drive can be virtually two drives. 
When you install a version of Windows on a drive/partition, Windows will create a file system and store its files there. 
Windows files and processes will constantly take up some storage and RAM. 
Your application, documents, etc., can be stored on a different drive/partition, it is a good habit.

## Windows Fileystem History
`FAT` (gone) -> `FAT32` (single file max 4GB) -> `NTFS` (Single file large size, recoverable (logs of file changes), has permissions, windows only) 
`exFAT` came to fix `FAT32` problems (Can be used for every OS, and good for USB as very large size for one file)
You can format your drive (in CLI/file explorer) etc. into `FAT32`, `exFAT`, `NTFS`, for `Windows`

## Good Practice
File Explorer Home for each user is just Windows User's directory (this is the default when you open File Explorer)
You don't have permissions to access other user's folders unless you're admin
- Go to `options` of File Explorer and set `Open File Explorer To This PC` instead of `Home`
- Ease of access to shares and drives when you open File Explorer (Home is just to see the current User folders)

## Public Users Folder
There is a `Public` folder in Users, so users can put files and folder in there that every user on system can access. 

## 32 and 64 bit identification
Check if there's a Program File and Program File (x86). If there's an (x86) folder labelled like that, it is x64

## File system Types
Windows: `NTFS` (new Windos File System allows permissions and groups compared to `Fat32`)
Linux: `ext3` and `ext4`
Mac: `APFS`
Global: `Fat32`, `exFAT` (common in Usbs)

# Sysadmin Stuff

## Permissions
Permissions of folder/file in `Properties->Security`
`Full Control` -> Full permissions for everything below (and can give other people permissions to file)
If you add a new user to the Permissions, default permissions -> `Read` and `Execute`
`Modify` -> Gives all the following permissions, except `Full Control` (can't edit permissions for others)
Can also give permissions view the contents of a folder
- When changing permissions for a folder, files inside will inherit permissions, but if you move a file to the folder, that file will not change to the folder's permissions
- Remember: Deny takes precedence over Allow (Folder has allow, files inside has deny, so the file denies access)

## Hidden Files
Can make files/folders hidden/read-only
Default Windows folders include:
- `User Folder` has a `Default` folder, which is a template folder for whenever you create a new user
- `AppData` Hidden Folder in User/Program Files is app settings just for the user (eg. chrome bookmarks) (for sysadmin, might want to delete Google (for google chrome) in `AppData`. This deletes User configs and settings for Google Chrome, then when launched, Google Chrome will create a new one (only deletes configs for this user). you can them take it out of recycling bin and replace the new one to get the old one back (useful for portable google chrome configs)

## Different Application Data Store Locations
Program != Application (Python vs MS Word)
- `AppData` -> where user application/program data is stored
- `Registry` -> Where application configuration is stored
- `ProgramData` -> Application specific data is stored
- `Program Files` -> Where read-only application binaries and code is stored

## Windows Folder
Windows OS folder located in `Drive Letter/Windows`
All the core things that Windows need to run is stored in `System32`, so if deleted, you're dead 
- can repair it with `sfc`

# Mac

## MacOs File Types
- .dmg
- .app
- .pkg, 

## MacOs Equivalent stuff
- FileVault (FDE: Full disk encryption)
- Disk utility (partitioning and managing disks)
- keychain (password and certificate manager)



