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
#### EXAMPLE
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


![alt text](<LAB6 IMG1.png>)

### install log2timeline
```
sudo apt install plaso -y
```

```
sudo apt install steghide -y
```
- **Embed data**
```
steghide embed -cf /home/kali/Desktop/car.jpeg -ef /home/kali/Desktop/message.txt
```
![alt text](<LAB6 IMG2.png>)

- **Extract hidden data:**

#### Example: $ steghide extract -sf hidden.jpg
```
steghide extract -sf /home/kali/Desktop/car.jpeg

```
![alt text](<LAB6 IMG3.png>)
### Using binwalk – for file analysis
```bash
sudo apt install binwalk -y
binwalk suspicious.jpg
```
```bash
binwalk /home/kali/Desktop/car.jpeg
```

![alt text](<LAB6 IMG4.png>)

## RESULT:
Metadata was successfully extracted, timeline analysis was completed, and hidden data was identified using steganography tools.
