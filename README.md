# Ensuring Confidentiality and Integrity in Cloud Storage

## Overview
This project is a client-side hybrid cryptographic framework designed to secure cloud data. It utilizes AES-256 (GCM mode) for confidentiality and SHA-256 for automated integrity verification. The system integrates seamlessly with AWS S3 for scalable storage and uses AWS IAM policies to enforce strict user authorization.

## Features
- **Local Encryption:** Encrypts diverse file types locally before uploading to the cloud.
- **Integrity Verification:** Generates manifest files with unique SHA-256 hash values to detect unauthorized data tampering upon retrieval.
- **Cloud Integration:** Automated multi-part uploads and retrievals using AWS S3.
- **Security:** AES-256 (GCM) for strong symmetric encryption and client-side key management.

## Technologies Used
- **Language:** Python
- **Libraries:** Boto3, hashlib, PyCryptodome
- **Cloud Infrastructure:** Amazon Web Services (AWS S3, IAM)

## Project Structure
- `src/` - Core application source code containing encryption and cloud logic.
- `config/` - Configuration settings for the framework.
- `data/` - Local datasets and test files.
- `logs/` - Execution and application logs.
- `manifests/` - Generated manifest files mapping original files to their SHA-256 hash values.
- `run_backup.py` - Execution script to encrypt files locally and upload them to AWS S3.
- `run_restore.py` - Execution script to download files, verify their integrity using manifests, and decrypt them.
- `requirements` - List of Python dependencies.

## Setup and Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/anujlondhe/Ensuring-Confidentiality-and-Integrity-in-Cloud-Storage-Using-AES-Encryption-and-SHA-256-Hashing.git
   cd Ensuring-Confidentiality-and-Integrity-in-Cloud-Storage-Using-AES-Encryption-and-SHA-256-Hashing
   ```

2. **Create and activate a virtual environment:**
   ```bash
   python -m venv venv
   # On Windows:
   venv\Scripts\activate
   # On macOS/Linux:
   source venv/bin/activate
   ```

3. **Install the required dependencies:**
   ```bash
   pip install -r requirements
   ```

4. **Configure AWS Credentials:**
   Ensure you have configured your AWS CLI with an IAM user that has the appropriate S3 read/write permissions.
   ```bash
   aws configure
   ```

## Usage

**To backup and encrypt data:**
```bash
python run_backup.py
```

**To restore and verify data:**
```bash
python run_restore.py
```
