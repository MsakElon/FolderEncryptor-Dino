[简体中文](./README.md) | English | [日本語](./README.ja.md) | [한국어](./README.ko.md)

# Folder Encryptor V5

`Folder Encryptor V5` is a lightweight folder encryption tool for Windows.

This repository currently provides ready-to-use release packages and documentation so people can download, try, and share the software more easily. The source code, license details, and more complete technical notes will continue to be organized over time.

## Product Overview

- A folder encryption and decryption tool for Windows desktop environments
- Available in both installer and portable editions
- Supports manual password entry and randomly generated strong passwords
- When a random password is generated, the app automatically appends a password backup record to a text file on the desktop

## Downloads

| File | Description | Size |
| --- | --- | ---: |
| [`FolderEncryptor_Dino_SmartSetup.exe`](https://github.com/MsakElon/FolderEncryptor-Dino/raw/main/dist/FolderEncryptor_Dino_SmartSetup.exe) | Installer edition for regular use | 69.7 MB |
| [`FolderEncryptor_V5_Dino.exe`](https://github.com/MsakElon/FolderEncryptor-Dino/raw/main/dist/FolderEncryptor_V5_Dino.exe) | Portable edition for direct launch | 34.9 MB |

Click a file name to download it directly.

## Core Features

- Select a target folder to encrypt or decrypt
- Enter your own master password
- Click `随机生成` to create a strong password instantly
- Automatically save random-password backups to the desktop
- Multiple generations are appended to the same backup file instead of overwriting old records

## Random Password and Backup

If you do not want to create a password manually, just click the `随机生成` button in the app.

The program will:

1. Generate a strong password automatically
2. Write the generated password to a backup text file on the desktop
3. Append new records to the same file each time instead of replacing old content

Example:

```text
【V5 专属加密密码备份】
密码: euZi^oahxuKq2Zm6

【V5 专属加密密码备份】
密码: JSE7CWTg54#CSH!Q
```

After encryption, it is recommended to store that backup file safely and avoid keeping the password backup in the same place as the encrypted files for a long time.

## Quick Start

### 1. Choose a version

- Use `FolderEncryptor_Dino_SmartSetup.exe` if you want a normal installation
- Use `FolderEncryptor_V5_Dino.exe` if you want a portable version with no installation

### 2. Encrypt a folder

Recommended flow:

1. Launch `Folder Encryptor V5`
2. Select the folder you want to protect in `Target Folder / 目标文件夹`
3. Enter a password in `Master Password / 安全密码`, or click `随机生成`
4. Click `隐形加密 (Encrypt)`
5. Wait for the process to finish and verify the result

### 3. Decrypt a folder

1. Launch `Folder Encryptor V5`
2. Select a previously encrypted folder
3. Enter the correct password
4. Click `一键还原 (Decrypt)`
5. Confirm the files are restored correctly before continuing

## SHA256 Checksums

```text
F656ABB26310F83526EEBEDC685ABDD9D79D12672882D8E38D902D30D3AE50A1  dist/FolderEncryptor_Dino_SmartSetup.exe
EB1A4C324AAE3372214E1A6C904B67472FCB626B3D071165C97533DEC33ECE52  dist/FolderEncryptor_V5_Dino.exe
```

## Recommendations

- Try the full workflow with a test folder before using important data
- Create an extra backup before operating on important files
- If you use a random password, review and store the desktop backup file carefully
- The current public release is mainly intended for Windows environments

## Repository Contents

- Usage Guide:
- [简体中文](./docs/usage-guide.md)
- [English](./docs/usage-guide.en.md)
- [日本語](./docs/usage-guide.ja.md)
- [한국어](./docs/usage-guide.ko.md)
- [Checksums](./checksums.txt)

## Current Status

This repository is currently a release-oriented public package: first provide a usable version, then continue improving the open-source materials around it.

That means:

- You can download and use the release packages right now
- The documentation is already suitable for public sharing
- The source code, license details, and more technical notes may continue to be refined later

## License

This project is licensed under the [MIT License](./LICENSE).

That means you can use, copy, modify, and distribute the project as long as the original license notice is preserved. The project is provided "as is" without warranty.
