# Windows General Tips

# File System Explained
- [Windows Filesystem Lamen's Terms](##windows-filesystem-lamen's-terms)
- [Good Practice](##good-practice)
- [32 and 64bit identification](##32-64bit)
- [File system Types](##file-system-types)

# Sysadmin Stuff
- [Hidden Files](##hidden-files)
- [Windows Directory](##windows-directory)
- [Windows Folder](##windows-folder)

# Mac 
- [MacOs File Types](##macos-file-types)
- [MacOs Equivalent stuff](##macos-equivalent_stuff)

## Windows Filesystem Lamen's Terms
A computer has a drive, or more drives can be installed. If drives had data before, it has been formatted. Each drive can be partitioned, so that one drive can be virtually two drives. 
When you install a version of Windows on a drive/partition, Windows will create a file system and store its files there. 
Windows files and processes will constantly take up some storage and RAM. 
Your application, documents, etc., can be stored on a different drive/partition, it is a good habit.

## Good Practice
File Explorer Home for each user is just Windows User's directory (this is the default when you open File Explorer)
You don't have permissions to access other user's folders unless you're admin
- Go to `options` of File Explorer and set `Open File Explorer To This PC` instead of `Home`
- Ease of access to shares and drives when you open File Explorer (Home is just to see the current User folders)

## 32 and 64 bit identification
Check if there's a Program File and Program File (x86). If there's an (x86) folder labelled like that, it is x64

## File system Types
Windows: NTFs (new Windos File system allows permissions and groups compared t Fat32)
Linux: ext3 and ext4
Mac: APFs
Global: Fat32, exFAT (common in Usbs)

# Sysadmin Stuff

## Hidden Files
Can make files/folders hidden/read-only
Default Windows folders include:
- User Folder has a `Default` folder, which is a template folder for whenever you create a new user
- AppData settings in User/Program Files is app settings just for the user (eg. chrome bookmarks) (for sysadmin, might want to delete Google (for google chrome) in AppData, to delete User configs and settings for Google Chrome, then when launched, will create a new one (only deletes configs for this user). you can them take it out of recycling bin and replace the new one to get the old one back (useful for portable google chrome configs) (but google account authetnication is stored here?)

## Windows Folder
Windows OS folder located in Drive Letter/Windows
All the core things that Windows need to run is stored in System32, so if deleted, you're dead 
- can repair it with sfc

# Mac

## MacOs File Types
- .dmg
- .app
- .pkg, 

## MacOs Equivalent stuff
- FileVault (FDE: Full disk encryption)
- Disk utility (partitioning and managing disks)
- keychain (password and certificate manager)



