#### How to format USB flash drive with PowerShell
#### This awesome information was taken from [this awesome webpage.]( https://www.windowscentral.com/how-format-usb-flash-drive-windows-10){:target="_blank"}
You can even use PowerShell commands to format a USB flash drive to erase its content. Or the command-line tool can also be used to clean and format the storage to resolve corruption and other problems.
Format flash drive using PowerShell

To format a USB flash drive using PowerShell commands, use these steps:

    Open Start.
    Search for PowerShell, right-click the top result, and select the Run as administrator option.

    Type the following command to perform a quick format on the flash drive and press Enter:

    Format-Volume -DriveLetter DRIVE-LETTER -FileSystem FILE-SYSTEM -NewFileSystemLabel DRIVE-NAME

    In the command, replace DRIVE-LETTER with the correct letter reflecting the drive you want to format, FILE-SYSTEM for FAT32, exFAT, or NTFS, and DRIVE-NAME with the name you want the device to appear in File Explorer.

    This example performs a quick format of the "F" drive with the NTFS file system:

    Format-Volume -DriveLetter F -FileSystem NTFS -NewFileSystemLabel workFlash

    PowerShell format USB flash drive
    Source: Windows Central

    (Optional) Type the following command to perform a full format of the USB flash drive and press Enter:

    Format-Volume -DriveLetter DRIVE-LETTER -FileSystem FILE-SYSTEM -Full -Force

    In the command, replace DRIVE-LETTER with the correct letter reflecting the drive you want to format, and FILE-SYSTEM for FAT32, exFAT, or NTFS, depending on the file system you want to use. If you do not know, and you are using Windows 10, then you could use NTFS. The Full option tells the command to perform a full format, and the -Force option specifies the override switch.

    This example performs a full format of the "F" drive:

    Format-Volume -DriveLetter F -FileSystem NTFS -Full -Force

After you complete the steps, PowerShell will format the removable storage with the settings you specified.
Clean and format flash drive using PowerShell

To clean and format a removable drive with PowerShell commands, use these steps:

    Open Start.
    Search for PowerShell, right-click the top result, and select the Run as administrator option.

    Type the following command to view the flash drive you want to fix and press Enter:

    Get-Disk

    Type the following command to delete the volume and press Enter:

    Get-Disk DISK-NUMBER | Clear-Disk -RemoveData

    In the command, change DISK-NUMBER for the correct number representing the flash drive you are formatting.

    This example selects and cleans the disk number 2:

    Get-Disk 2 | Clear-Disk -RemoveData

    Type Y to confirm the action and press Enter.

    Type the following command to create a new partition and press Enter:

    New-Partition -DiskNumber DISK-NUMBER -UseMaximumSize

    In the command, change DISK-NUMBER to the correct number representing the storage you are formatting.

    This example creates a new partition using the entire space available on drive number 2:

    New-Partition -DiskNumber 2 -UseMaximumSize

    Type the following command to perform a quick format and assign a drive label, and press Enter:

    Get-Partition -DiskNumber DISK-NUMBER | Format-Volume -FileSystem FILE-SYSTEM -NewFileSystemLabel DRIVE-NAME

    In the command, change DISK-NUMBER for the number that identifies the storage in the system, FILE-SYSTEM for "NTFS," "FAT32," or "exFAT," and DRIVE-NAME with the name you want the device to appear in File Explorer.

    This example selects and formats drive number 2 using the NTFS file system:

    Get-Partition -DiskNumber 2 | Format-Volume -FileSystem NTFS -NewFileSystemLabel workFlash

    PowerShell clean and format USB flash drive
    Source: Windows Central

    Type the following command to assign a new letter to the drive and press Enter:

    Get-Partition -DiskNumber DISK-NUMBER | Set-Partition -NewDriveLetter DRIVE-LETTER

    In the command, replace DISK-NUMBER for the number that identifies the storage in the system, and DRIVE-LETTER with the letter you want the device to appear in File Explorer.

    This example sets "E" as the drive letter for disk number 2:

    Get-Partition -DiskNumber 2 | Set-Partition -NewDriveLetter E

After you complete the steps, PowerShell will remove any information on the removable USB storage to fix problems, including data corruption, write protection, and unrecognized drives. Then it will proceed to create a new partition and configure a file system to store files.

How to format USB flash drive with Command Prompt

Alternatively, you can also format a USB flash drive using commands. Or you can use the Command Prompt to clean the drive and start fresh with a new partition and file system table.
Format flash drive using command-line

To perform a quick or full format on a USB flash drive with Command Prompt, use these steps:

    Open Start.
    Search for Command Prompt, right-click the top result, and select the Run as administrator option.

    Type the following command to perform a quick format of the USB flash drive and press Enter:

    format VOLUME: /v:FLASHDRIVE-LABEL /fs:FILE-SYSTEM /q

    In the command, make sure to replace the VOLUME with the correct drive letter of the storage, FLASHDRIVE-LABEL with the name you want the drive to appear in File Explorer, FILE-SYSTEM with one of the available file systems, including "FAT32," "exFAT," or "NTFS."

    This example performs a quick format of the E drive:

    format G: /v:workFlash /fs:NTFS /q

    Command Prompt quick format for USB flash drive
    Source: Windows Central
    Press Enter again to continue.

    (Optional) Type the following command to perform a full format of the USB flash drive and press Enter:

    format VOLUME: /v:FLASHDRIVE-LABEL /fs:FILE-SYSTEM

    This example performs a full format of the E drive:

    format E: /v:"workFlash" /fs:NTFS
    Press Enter again to continue.

After you complete the steps, the thumb drive will be formatted with the settings you specified.
Clean and format flash drive using command-line

To clean and format a flash drive with command-line, use these steps:

    Open Start.
    Search for Command Prompt, right-click the top result, and select the Run as administrator option.

    Type the following command to launch the diskpart tool and press Enter:

    diskpart

    Type the following command to view a list of the available drives and press Enter:

    list disk

    Type the following command to select the flash drive you want to delete and press Enter:

    select disk DISK-NUMBER

    In the command, make sure to replace DISK-NUMBER for the number representing the drive you are trying to format.

    This example selects the flash drive listed as disk number 2:

    select disk 2

    Type the following command to delete all the partitions on the storage and press Enter:

    clean

    Type the following command to create a primary partition and press Enter:

    create partition primary

    Type the following command to perform a quick format and press Enter:

    format fs=FILE-SYSTEM label=DRIVE-NAME quick

    In the command, make sure to replace FILE-SYSTEM for your preferred file system, including "FAT32," "exFAT," or "NTFS." Also, replace DRIVE-NAME with the name you want to give the device, and if you do not specify the "quick" option, then a full format will be performed.

    This example quickly formats the removable storage using the NTFS file system and applies the "workFlash" name:

    format fs=NTFS label=workFlash quick

    Diskpart format USB flash drive
    Source: Windows Central

    Type the following command to assign a drive letter and press Enter:

    assign

    Quick note: You can append "letter=E" in the command to assign (in this case) "E" as the drive letter. Otherwise, the system will assign a letter automatically.

    Type the following command to close diskpart and press Enter:

    exit

Once you complete the steps, the diskpart command-line tool will remove any information from the USB flash drive. It will create a new partition and configure a compatible file system to store files from your Windows 10, macOS, or Linux machine (depending on your configuration).
