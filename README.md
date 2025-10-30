# Metadata-Extraction-using-ExifTool-log2timeline-and-Hidden-Data-Search-using-Steganography-Tools

## AIM:
To extract metadata, perform timeline analysis, and search for hidden data using forensic tools like ExifTool, log2timeline, and steganography detection tools.

## DESIGN STEPS:
### Step 1:
Use exiftool to extract metadata from files such as images, documents, and videos.

### Step 2:
Use log2timeline and plaso to create and analyze event timelines from system logs and file metadata.

### Step 3:
Apply steganography detection tools like steghide, zsteg, or binwalk to uncover hidden data in media files.

## PROGRAM:
Metadata and Timeline Forensics, Steganography Analysis Steps

## OUTPUT:
# A. Using ExifTool – for file metadata

 Install:
```
sudo apt update
sudo apt install exiftool -y
```
 Extract metadata from a file:
```
exiftool image.jpg
```
 Batch process a folder:
```
exiftool -r /path/to/folder
```
 # Useful flags:

-G: Show metadata group

-time:all: Show only timestamps

-GPSLatitude -GPSLongitude: Extract GPS data
<img width="956" height="572" alt="Screenshot 2025-09-27 144208" src="https://github.com/user-attachments/assets/29340968-b1f1-4c6c-89c6-ebda18375aa3" />


# install log2timeline
```
sudo apt install plaso -y
```
```
sudo apt install steghide -y
```
# Embed data
```
steghide embed -cf /home/kali/Downloads/wallpaper.jpg -ef /home/kali/Downloads/secret.txt
```
<img width="960" height="62" alt="Screenshot 2025-09-27 144620" src="https://github.com/user-attachments/assets/e1e47d0c-1f37-482e-8a42-47007d9733e6" />


Extract hidden data:
```
steghide extract -sf hidden.jpg
```
<img width="960" height="62" alt="Screenshot 2025-09-27 144620" src="https://github.com/user-attachments/assets/ea4a61f4-6b8b-4dd3-8965-a2541f371b1f" />


# Using binwalk – for file analysis

```
sudo apt install binwalk -y
binwalk suspicious.jpg
```
<img width="962" height="145" alt="Screenshot 2025-09-27 144607" src="https://github.com/user-attachments/assets/c19c0f89-f96d-4abd-998b-9e51b1f26d76" />



## RESULT:
Metadata was successfully extracted, timeline analysis was completed, and hidden data was identified using steganography tools.

