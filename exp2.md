# Experimnt 2: Recover deleted or damaged files from a storage device using Test Disk

## Aim 🎯
The aim of this experiment is to recover deleted or damaged files from a storage device using TestDisk. The process focuses on locating files that have been marked for deletion by the file system but whose underlying data still exists on the disk, making them potentially recoverable.

## Description 📝
When a file is "deleted" from a modern file system (like NTFS, FAT32, or exFAT), the data itself isn't immediately erased. Instead, the file system simply removes the file's entry from the directory table and marks the space it occupied as free. This makes the space available for new data to be written. TestDisk is a powerful, open-source data recovery tool that can scan the disk for these orphaned file entries and, if the data hasn't been overwritten, copy the files to a safe location. It's a command-line utility, so it can be intimidating at first, but its step-by-step menu-driven interface guides the user through the recovery process.

## Tools & Equipment Used 🛠️
Forensic Workstation: A computer with an operating system compatible with TestDisk (Windows, Linux, macOS).

TestDisk: The open-source data recovery software.

Source Storage Device: The device from which you want to recover files (e.g., hard drive, USB drive, SD card). It is crucial to not write any new data to this device after the files are deleted, as this could overwrite the data you are trying to recover.

Destination Storage Device: A separate, healthy storage device with enough free space to store the recovered files. This device must be different from the source device to prevent data overwriting.

## Procedure 👩‍🔬
Preparation:
![alt text](<ScreenShort2/Screenshot 2025-09-01 234650.png>)
Download and extract the TestDisk software. Since it's a portable application, no installation is needed.
![alt text](<ScreenShort2/Screenshot 2025-09-01 234706.png>)
Connect the source storage device to the workstation.
![alt text](<ScreenShort2/Screenshot 2025-09-01 234746.png>)
Connect the destination storage device for recovered files.

Launch TestDisk with administrator privileges.

Initial Scan and Log Creation:
![alt text](<ScreenShort2/Screenshot 2025-09-01 234801.png>)
Upon launching, TestDisk will ask if you want to create a log file. Choose Create to document your recovery session.
![alt text](<ScreenShort2/Screenshot 2025-09-01 234809.png>)
The program will then display a list of all connected drives. Use the arrow keys to select the source storage device and press Enter to proceed.
![alt text](<ScreenShort2/Screenshot 2025-09-01 234825.png>)
Partition Analysis:
![alt text](<ScreenShort2/Screenshot 2025-09-01 234843.png>)
TestDisk will automatically detect the partition table type (e.g., Intel/PC, EFI GPT). The default selection is usually correct. Confirm this selection and press Enter.

From the main menu, select the Advanced option. This option is used for undeleting files and recovering files from a specific partition.

Next, select the partition you want to recover from. A list of partitions on the selected drive will be shown.

At the bottom of the screen, you'll see various options. Select Undelete and press Enter.

File Recovery:
![alt text](<ScreenShort2/Screenshot 2025-09-01 234854.png>)
TestDisk will begin scanning the selected partition for deleted files and directories. Files that are recoverable will be listed, often in a different color (e.g., red) to indicate they are deleted.

Navigate the list using the arrow keys. Use the : key to select individual files or folders you wish to recover. You can also press a to select all files.

Once your selection is complete, press the C key (capital C) to copy the selected files.

A new window will appear, prompting you to choose a destination directory for the recovered files. Navigate to the destination storage device you prepared earlier.

Once you've selected the recovery folder, press C again to start the copying process.

Completion:
![alt text](<ScreenShort2/Screenshot 2025-09-01 234932.png>)
TestDisk will copy the recovered files to the specified destination.

A summary will be displayed, showing how many files were copied.

Press Quit to exit the program.

## Results 📊
File Recovery: A number of deleted files were successfully recovered from the source storage device. These files were copied to the destination device without altering the original disk.

Integrity Check: The recovered files were examined and found to be intact and readable, indicating that their data had not been overwritten since deletion.

Log Documentation: The log file created at the beginning of the process contains a record of all steps taken, providing a clear chain of custody and documentation for the recovery procedure.