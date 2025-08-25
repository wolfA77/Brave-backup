# Brave-backup
Backup and restore brave browser withot synch function.


ℹ️ YourFolder is the path to your Brave browser's backup profile folder, and it should be an absolute path.

Step 1 - Turn off Brave before performing backup and restore.
Step 2 - Change "YourFolder" to your Brave backup directory before run commands.
Setp 3 - Copy and run commands.
-------------------------------------
🪟 WINDOWS

BACKUP

$Backup_Folder = "C:\Users\VanMarkus\Desktop\My_Brave"; Remove-Item $Backup_Folder"\*" -Recurse -Force -Confirm:$false; Copy-Item "~\AppData\Local\BraveSoftware\Brave-Browser\" -Destination $Backup_Folder -Recurse -Force;

RESTORE

$Backup_Folder = "C:\Users\VanMarkus\Desktop\My_Brave"; Remove-Item "~\AppData\Local\BraveSoftware\*" -Recurse -Force -Confirm:$false; Copy-Item $Backup_Folder"\*" -Destination "~\AppData\Local\BraveSoftware\" -Recurse -Force;
