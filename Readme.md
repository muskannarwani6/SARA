
# SARA - Simple Access Remote Attack (Ransomware)

> ⚠️ **DISCLAIMER**: This project is intended for **educational and ethical research purposes only**. Unauthorized use of this tool on systems without explicit permission is **strictly illegal** and punishable by law. Use responsibly in controlled environments for learning, red teaming, or cybersecurity awareness.

---

## 💡 About

**SARA** is a Python-based educational ransomware and remote access simulation tool. It provides a real-world scenario of how ransomware operates — encrypting files on a target system, establishing a reverse shell connection, and displaying a ransom note. It is ideal for penetration testers, researchers, or cybersecurity students looking to understand ransomware mechanisms.

---

## ⚙️ Features

- 🔐 Encrypts files using a simple XOR encryption (for educational purposes)
- 💻 Opens a reverse shell from victim to attacker
- 📁 Targets specified folders for encryption
- 📜 Drops and displays a custom ransom note
- 📦 Supports creating standalone `.exe` payloads using `pyinstaller`
- 🖥️ Compatible with Linux & Windows
- 📡 Can be paired with Ngrok or port forwarding for WAN-based reverse shells

---

## 📂 Project Structure

```
SARA/
├── sara.py              # Ransomware payload (client side)
├── requirements.txt     # Python dependencies
├── LICENSE
└── README.md            # Project documentation
```

---

## 🛠️ Installation

> **Tested on Python 3.x**

### 1. Clone the repository

```bash
git clone https://github.com/muskannarwani6/SARA
cd SARA
```

### 2. Install required packages

```bash
pip install -r requirements.txt
```

---

## 🔧 Configuration

Edit the following variables in `sara.py` or `utils.py`:

```python
IP = 'attacker_ip'     # Your listening server IP
PORT = 4444            # Port to listen on
DIRECTORY = 'target_folder'  # Path to target victim files
```

### ➤ Run or send the payload (victim side)

```bash
python sara.py
```

---

## 🛠️ Build Standalone Executable (Optional)

Use `pyinstaller` to compile `sara.py` into a `.exe`:

```bash
pip install pyinstaller
pyinstaller --onefile sara.py
```

You can disguise or bind this payload using your preferred tools for ethical testing purposes.

---

## 📜 Example Ransom Note

SARA drops a ransom note in the target folder which can be customized in the code:

```
Your files have been encrypted by SARA.
To decrypt your files, contact us with your unique key.
```

---

## 🧠 Educational Purpose

SARA is **not a real-world ransomware** — it uses simple XOR encryption and is designed to help:

- Learn file encryption/decryption mechanisms
- Understand reverse shells and remote access
- Train for ransomware incident response
- Conduct red team cybersecurity simulations

