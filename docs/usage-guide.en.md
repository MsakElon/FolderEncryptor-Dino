[简体中文](./usage-guide.md) | English | [日本語](./usage-guide.ja.md) | [한국어](./usage-guide.ko.md)

# Usage Guide

## Who This Is For

This guide is intended for first-time users of `Folder Encryptor V5`.

If you only want a quick overview, start with the README. If you plan to use the software more seriously, reading this full page is recommended.

## Available Editions

The project currently provides two editions:

- Installer edition: `dist/FolderEncryptor_Dino_SmartSetup.exe`
- Portable edition: `dist/FolderEncryptor_V5_Dino.exe`

In general, the installer edition is recommended. If you only want to try it quickly or prefer not to install anything, you can use the portable edition directly.

## Interface Overview

The main interface includes:

- `Target Folder / 目标文件夹`: choose the folder you want to encrypt or decrypt
- `Browse`: open the folder picker
- `Master Password / 安全密码`: enter your own password
- `随机生成`: automatically generate a strong password
- `隐形加密 (Encrypt)`: run encryption
- `一键还原 (Decrypt)`: run decryption

## What Stealth Encryption Means

One of the key ideas behind `Folder Encryptor V5` is stealth encryption.

Here, "stealth" mainly means:

- File names and folder structure usually stay unchanged after encryption
- From the outside, the folder still looks like the original one
- But the file content has already been turned into ciphertext
- Without the correct password, files will usually fail to open or appear garbled, corrupted, or unreadable

This makes it suitable for quietly protecting file contents instead of turning them into an obviously separate encrypted archive.

## Technical Overview

Technically, this is not simple text replacement or scrambling. It encrypts the full content of each file.

High-level flow:

1. Recursively scan files in the target folder
2. Read each file as full binary data
3. Use the password and a random `salt` to derive a key with `PBKDF2-HMAC-SHA256`
4. Use `cryptography.fernet.Fernet` to encrypt the file content and protect integrity
5. Write the encrypted data back to the original file path

So what is protected is the actual file content, not just text inside text files.

## Random Password Generation

If you do not want to set a password manually, click `随机生成`.

The program will automatically generate a strong password and also save it to a backup text file on the desktop to help prevent password loss.

This backup file works like this:

- A txt backup file is created on the desktop
- Every time you click `随机生成`, a new password record is appended
- Old records are not overwritten

Example format:

```text
【V5 专属加密密码备份】
密码: euZi^oahxuKq2Zm6

【V5 专属加密密码备份】
密码: JSE7CWTg54#CSH!Q
```

After the operation is complete, it is recommended to move that backup file to a safer place instead of leaving it on the desktop for a long time.

## Before You Start

Before first use, prepare a small test folder with a few unimportant files and run through the full encryption and decryption process once.

Benefits:

- You get familiar with the interface and workflow
- You can confirm the app runs correctly on your computer
- You avoid using important data for your very first test

## Encrypting a Folder

Recommended steps:

1. Launch the program
2. Choose the target folder in `Target Folder / 目标文件夹`
3. Enter a password in `Master Password / 安全密码`, or click `随机生成`
4. Check that the selected path is correct
5. Click `隐形加密 (Encrypt)`
6. Wait for the process to finish
7. Open the result folder and verify it manually

## Decrypting a Folder

Recommended steps:

1. Launch the program
2. Select a folder previously processed by this tool
3. Enter the original encryption password
4. Click `一键还原 (Decrypt)`
5. Verify that the restored files open correctly

## Important Notes

### 1. Password Management

- The password is the key to restoring your files
- Make sure you store it safely
- If you use a random password, also keep the desktop backup file

### 2. Backup Before You Operate

- Create an extra backup before encrypting important files
- Especially during your first real use, avoid operating on the only original copy

### 3. Test On a Small Scale First

- Start with one or two small folders
- After confirming the workflow is stable, move on to more important data

### 4. Environment Notes

- The current public version is intended for Windows desktop environments
- If system security settings are strict, you may need to confirm the first launch manually

## FAQ

### What is the difference between the installer and portable editions?

- The installer edition is better for long-term regular use
- The portable edition is better for quick testing and single-file distribution

### Can I use it without creating my own password?

Yes. Click `随机生成` and the program will create a strong password for you and automatically save a txt backup on the desktop.

### Will multiple random generations overwrite previous passwords?

No. New passwords are appended to the same backup text file, and old records remain there.

### What if I forget the password?

The password is essential for restoring encrypted data. Decide on a password management method before using the tool. If you use random passwords, save the desktop backup file promptly.

### Should I use important data for my first test?

No. It is better to validate the workflow with a test folder first, then use it for real data later.

## Recommended Use Cases

- Organizing private personal files
- Archiving course materials and study documents
- Adding extra protection to local project documents
- Temporarily protecting a group of folders
