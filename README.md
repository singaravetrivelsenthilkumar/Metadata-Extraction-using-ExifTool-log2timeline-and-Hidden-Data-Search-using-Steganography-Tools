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
### ✅ A. Using ExifTool – for file metadata
- **📦 Install:**
```bash
sudo apt update
sudo apt install exiftool -y
```
- **📂 Extract metadata from a file:**
```bash
exiftool image.jpg
```
- **📁 Batch process a folder:**
```bash
exiftool -r /path/to/folder
```
- **📌 Useful flags:**
  
- ```-G: Show metadata group```

- ```-time:all: Show only timestamps```

- ```-GPSLatitude -GPSLongitude: Extract GPS data```

  ![image](https://github.com/user-attachments/assets/861dc1d1-4932-460d-9261-2e3295ee9f42)

### install log2timeline
```
sudo apt install plaso -y
```

```
sudo apt install steghide -y
```
- **Embed data**
```
steghide embed -cf /home/kali/Downloads/wallpaper.jpg -ef /home/kali/Downloads/secret.txt
```
![image](https://github.com/user-attachments/assets/d34970ca-ee2c-4a7f-9980-518b74962f02)

- **Extract hidden data:**
```
steghide extract -sf hidden.jpg

```
![image](https://github.com/user-attachments/assets/85520110-9150-417a-b6a9-28e559100cf7)

### Using binwalk – for file analysis
```bash
sudo apt install binwalk -y
binwalk suspicious.jpg
```
```bash
binwalk /home/kali/Downloads/wallpaper.jpg
```
![image](https://github.com/user-attachments/assets/b26be271-0680-491f-8868-1216de6fd7eb)

## RESULT:
Metadata was successfully extracted, timeline analysis was completed, and hidden data was identified using steganography tools.
