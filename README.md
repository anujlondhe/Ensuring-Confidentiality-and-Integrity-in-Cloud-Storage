Perfect! Here’s a **complete, updated README.md** for your project that includes both **terminal commands** and **GUI instructions**. You can copy-paste this into your repository.

---

````markdown
# Ensuring Confidentiality and Integrity in Cloud Storage Using AES-256 Encryption and SHA-256 Hashing

This project implements a **hybrid cryptographic framework** that combines **AES-256 encryption** and **SHA-256 hashing** to secure files before uploading them to **cloud storage (AWS S3)**.  
It ensures **data confidentiality** and **integrity**, providing a dual-layer protection mechanism for sensitive files.

---

## 🧰 Prerequisites
Make sure you have the following installed:

- **Python 3.8+**  
- **pip** (Python package manager)  
- **Virtual environment (venv)** module  

---

## ⚙️ Setup Instructions

### 1. Clone the Repository
```bash
git clone https://github.com/anujlondhe/Ensuring-Confidentiality-and-Integrity-in-Cloud-Storage
cd Ensuring-Confidentiality-and-Integrity-in-Cloud-Storage
````

### 2. Create and Activate a Virtual Environment

```bash
python3 -m venv venv
source venv/bin/activate     # For macOS/Linux
venv\Scripts\activate        # For Windows
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 🚀 Running the Project

### 4. Run the GUI Application

From the project root:

```bash
python -m src.gui.app
```

> This will launch the **secure backup GUI** where you can encrypt, upload, verify, and decrypt files.

### 5. Run Terminal Commands (Optional)

You can also run operations via the terminal:

* **Encrypt a file**

```bash
python -m src.cli.app encrypt <file_path>
```

* **Verify file integrity**

```bash
python -m src.cli.app verify <file_path>
```

* **Decrypt a file**

```bash
python -m src.cli.app decrypt <encrypted_file>
```

---

## 📦 Example Usage

```bash
python -m src.cli.app encrypt sample.txt
python -m src.cli.app verify sample.txt
python -m src.cli.app decrypt sample.txt.enc
```

Or launch the GUI:

```bash
python -m src.gui.app
```

---

## 🧪 Features

* AES-256 encryption for **confidentiality**
* SHA-256 hashing for **integrity verification**
* AWS S3 integration for **secure cloud storage**
* GUI and CLI support
* Performance metrics: encryption/decryption time, CPU/memory usage

---

## 🛡️ Notes

* Store your AWS credentials securely (e.g., in a `.env` file).
* Ensure IAM permissions allow S3 access for your user.
* Test with various file types (text, images, multimedia) to evaluate performance.

---

## 👨‍💻 Author

**Anuj Londhe (@anujlondhe)**
Hybrid Cryptographic Framework for Secure Cloud Storage – Research Implementation

```

---

If you want, I can **also add a small diagram or flowchart** section in the README to visually show **AES + SHA workflow**, which makes your repo look very professional.  

Do you want me to do that?
```
