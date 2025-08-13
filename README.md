# SecureUpload Library

This repository is an effort to make uploading files more secure in DataFlex applications. It provides a library that can be used to handle file uploads with enhanced security measures. By default it uses Windows Defender to scan files before they are uploaded, ensuring that only safe files are processed. It is required to exclude the Data/Temp directory from Windows Defender scanning to avoid race conditions and stability issues. After scanning, the file is scanned using the File (libmagic) library to determine the file type, and if it is not a valid file type, it will be rejected. After it matches the max file size and extention, the file is uploaded to the server e.g. moving it to the Data/uploads directory.

###### External Components

| Component                  | Version                                  |
| -------------------------- | ---------------------------------------- |
| File                       | https://github.com/DataFlex-dev/File.git |
| Windows Defender (default) | Windows 10 or later                      |

## General Information

| Product  | Version          |
| -------- | ---------------- |
| DataFlex | 23.0, 24.0, 25.0 |
