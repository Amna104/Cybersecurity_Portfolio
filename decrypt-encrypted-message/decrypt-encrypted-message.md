# Decrypt an Encrypted Message

## Overview
This project demonstrates practical skills in cryptography and Linux command-line usage. The activity focuses on decrypting a Caesar cipher and an AES-256-CBC encrypted file to reveal hidden messages.

This activity shows my ability to:
- Work with Linux Bash commands
- Identify and read hidden files
- Apply decryption techniques using the Caesar cipher
- Use OpenSSL to decrypt AES-encrypted files
- Document steps clearly for reproducibility

---

## Scenario
All files in the analyst's home directory have been encrypted. The goal is to:
1. Explore the home directory
2. Find a hidden file
3. Decrypt a Caesar cipher
4. Use the revealed command to decrypt the encrypted file
5. Recover and read the hidden message

---

## Tasks Completed

### **Task 1: Read the Contents of a File**
- Command: `ls /home/analyst`
- Command: `cat README.txt`
- Learned the next steps were in the `caesar` subdirectory.

### **Task 2: Find a Hidden File**
- Command: `cd caesar`
- Command: `ls -a` to list hidden files
- Hidden file found: `.leftShift3`
- Decrypt Caesar cipher:
```bash
cat .leftShift3 | tr "d-za-cD-ZA-C" "a-zA-Z"
