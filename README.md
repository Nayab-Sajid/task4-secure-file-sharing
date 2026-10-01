# Task 4 – Secure File Sharing System

Internee.pk Cybersecurity Internship

## Objective
Ensure secure file exchanges between Internee.pk and external parties, by building a secure file-sharing portal with end-to-end encryption, cloud storage with signed-URL-style access, and encryption during both upload and download.

## What's in this repo
- **Task4_Secure_File_Sharing_Report.docx** – Full write-up covering the encryption tool, sample data, and the signed-URL sharing demonstration

## What was done
1. **Built a secure file-sharing tool** – Developed "Simple Secure File Share," a working tool using the browser's native Web Crypto API to perform genuine client-side AES-256-GCM encryption, with the key never leaving the browser alongside the file.
2. **Sample data** – Used a real dataset ("Sample Sales Data") from Kaggle as the test file, since Internee.pk's staging data wasn't accessible.
3. **Cloud storage with a signed-URL equivalent** – Uploaded the encrypted file to Filebin, a free service that issues a unique, time-limited shareable link, functioning like an AWS S3 / GCP / Azure signed URL.
4. **End-to-end verification** – Confirmed the full pipeline: encrypt → upload → share link → download → decrypt, with the final decrypted file matching the original exactly.

## Tools used
- [Kaggle](https://www.kaggle.com/) – sample dataset
- [CodePen](https://codepen.io/) – hosting the encryption tool
- Web Crypto API (built into the browser) – AES-256-GCM encryption/decryption
- [Filebin](https://filebin.net/) – temporary shareable link (signed-URL equivalent)
