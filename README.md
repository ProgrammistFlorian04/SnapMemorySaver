# SnapMemorySaver

## Download

Get the latest version here:  
https://ko-fi.com/s/eeeb47f0f7

---

## Short Overview

SnapMemorySaver is a local desktop tool for macOS and Windows, available in English and German, that allows Snapchat Memories to be downloaded and stored locally using the official Snapchat export JSON.

The tool reads the JSON file provided by Snapchat, downloads each media file individually, automatically extracts ZIP files, renames files in a readable format, and stores everything locally in a clear folder structure.

It runs as:
- macOS `.app`
- Windows `.exe`

No Python installation, browser extensions, or additional software are required.

---
<img width="1470" height="956" alt="Bildschirmfoto 2025-12-25 um 16 46 50" src="https://github.com/user-attachments/assets/0d60915a-5d82-4d23-b2db-b3ed9bb8426c" />

---

## What the Tool Actually Does

SnapMemorySaver performs the following steps:

### 1. Read Snapchat Export JSON
- Uses the `Saved Media` section
- Reads all included media download URLs
- Filters entries by selected years

### 2. Individual Download of All Media
- Each file is downloaded individually using the official Snapchat URL
- Downloads run sequentially (no parallel downloads)
- The user interface remains responsive during downloads

### 3. Automatic ZIP Processing
When a `.zip` file is downloaded:
- the ZIP archive is opened
- contained media files are extracted
- extracted files are renamed
- timestamps are applied (optional)
- the original ZIP file is deleted afterward

### 4. Meaningful File Naming
- File names are based on the original Snapchat creation date
- Format:  
  `YYYY-MM-DD_HH-MM-SS_Index.extension`

### 5. Timestamp Handling (Optional)
- If enabled, the file timestamp is applied
- Uses the date from the Snapchat JSON
- Implemented in a UTC-safe way

### 6. Folder Structure (Optional)
Either:
- all files in a single folder  
or:
- structured storage by year / month

### 7. Progress and Remaining Time
- Progress is based on the number of files
- Remaining time (ETA) is calculated using a sliding average
- Fluctuations caused by mixed file sizes are reduced

### 8. Logging
- A log file is created in the target directory
- Logged information includes:
  - successful downloads
  - ZIP extractions
  - errors (timeouts, server errors, connection drops)
  - user-initiated aborts

---

## Supported File Types

Based on the detected content type, the following formats are supported:

### Videos
- `.mp4`

### Images
- `.jpg`
- `.jpeg`
- `.png`
- `.webp`
- `.gif`

### Archives
- `.zip` (automatically extracted)

Unknown types are stored using a fallback extension.

---

## What the Tool Does Not Do

- no Snapchat login
- no scraping
- no bypassing of access restrictions
- no data uploads
- no cloud services
- no modification of Snapchat data

Only the official Snapchat-provided download URLs are used.

---

## Languages and Platforms

### Languages
- English
- German

### Platforms
- macOS
- Windows

---

## Execution Model

- Runs completely locally
- Network access only to Snapchat media URLs
- Downloads run in a separate thread
- Errors do not crash the application

---

## Screenshots

<img width="1470" height="956" alt="Bildschirmfoto 2025-12-25 um 16 46 50" src="https://github.com/user-attachments/assets/eb277f91-3c6c-4d08-8d26-6423d6df7db4" />
<img width="1470" height="956" alt="Bildschirmfoto 2025-12-25 um 16 49 25" src="https://github.com/user-attachments/assets/b0604eb5-fef2-4270-9f4a-eed1b819add1" />
<img width="1333" height="568" alt="Bildschirmfoto 2025-12-25 um 16 51 41" src="https://github.com/user-attachments/assets/fc010763-b39e-4660-8284-0fdbfc4ecfb8" />
<img width="254" height="254" alt="snapsaver" src="https://github.com/user-attachments/assets/1d18d6d8-5dd8-41e7-89e3-aec6e6bbedda" />


---

## Download

Get the latest version here:  
https://ko-fi.com/s/eeeb47f0f7
