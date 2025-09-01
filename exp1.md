# Experiment 1: Create a forensic image of a storage device's using FTK Imager

## Aim 
The aim of this experiment is to create a forensically sound image of a storage device. This process involves making a bit-for-bit copy of the original media without altering any data, thus preserving its integrity for a digital forensics investigation. The resulting image will be used for further analysis, allowing the original evidence to be stored securely.

## Description 
Forensic imaging is the foundational step in digital forensics. A forensic image, also known as a bitstream or a bit-for-bit copy, is an exact duplicate of the data on a storage device, including not only active files but also deleted files, unallocated space, and file system metadata. This process is crucial to ensure that the original evidence is not modified during the examination. FTK Imager, a free and widely used tool, facilitates this by creating various image formats and verifying data integrity with cryptographic hash functions like MD5 and SHA-1. The hash value acts as a unique digital fingerprint, proving that the imaged data is an exact replica of the original.

## Tools & Equipment Used 
Forensic Workstation: A dedicated computer with a clean operating system and sufficient storage space for the forensic image.

FTK Imager: A digital forensics software tool used to create the forensic image.

Evidence Storage Device: The source device to be imaged (e.g., hard drive, USB flash drive, SD card).

Write-Blocker: A hardware or software device that prevents any data from being written to the evidence device. This is a critical component to maintain the integrity of the original evidence.

Destination Storage Device: A separate, empty storage medium (e.g., external hard drive) with sufficient capacity to hold the forensic image. This device should never be the same as the evidence device.

## Procedure 👩‍🔬
Preparation:

Connect the evidence storage device to the forensic workstation via a write-blocker.

Connect the destination storage device to the workstation. Ensure it has enough free space for the image.

Launch FTK Imager.
![alt text](<Screenshort1/Screenshot 2025-09-01 215714.png>)
Creating the Image:



From the FTK Imager menu, go to File and select Create Disk Image.

In the Select Source window, choose Physical Drive and click Next.
![alt text](<Screenshort1/Screenshot 2025-09-01 215810.png>)
From the dropdown list, select the evidence device you connected. Use the size and model number to confirm it's the correct one, then click Finish.

A new window will appear. Click the Add... button to add an image destination.
![alt text](<Screenshort1/Screenshot 2025-09-01 215827.png>)
Choose the desired image type (e.g., Raw (dd), E01 (EnCase Format)) and click Next.

Fill out the Evidence Item Information form with details such as the case number, evidence number, unique description, and examiner's name. This metadata is essential for the chain of custody.
![alt text](<Screenshort1/Screenshot 2025-09-01 215840.png>)
Specify the Image Destination Folder on your destination storage device and provide a file name for the image. You can also configure fragmentation and compression settings here.

Select the Verify images after they are created checkbox. This ensures FTK Imager will calculate and compare hash values after the imaging process is complete.
![alt text](<Screenshort1/Screenshot 2025-09-01 215850.png>)
Click Start to begin the imaging process.
![alt text](<Screenshort1/Screenshot 2025-09-01 215904.png>)
Verification:
![alt text](<Screenshort1/Screenshot 2025-09-01 215912.png>)
FTK Imager will perform a bit-by-bit copy of the evidence device.

Once the imaging is complete, the tool will automatically calculate the hash values (MD5 and SHA-1) of both the original source drive and the newly created image file.
![alt text](<Screenshort1/Screenshot 2025-09-01 220112.png>)
It will then compare these two sets of hash values.
![alt text](<Screenshort1/Screenshot 2025-09-01 220419.png>)
## Results 📊
Forensic Image Created: A complete forensic image file was successfully created on the destination storage device.

Hash Value Match: The MD5 and SHA-1 hash values calculated from the source device were a perfect match with the hash values of the newly created forensic image. This result verifies the integrity of the image, proving that the data was copied exactly without any changes.

Log File: FTK Imager generated a log file detailing the entire process, including the start and end times, the examiner's information, and the matching hash values. This log serves as critical documentation for the chain of custody.
