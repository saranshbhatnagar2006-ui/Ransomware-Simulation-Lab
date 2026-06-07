
# Ransomware Attack & Defense Cryptographic Simulator

An educational malware simulation tool designed to demonstrate how symmetric encryption is utilized by modern ransomware strains to lock files, alongside the corresponding incident response recovery mechanisms.

## 📌 Disclaimer
This repository is strictly for **educational purposes, academic evaluation, and defensive security research**. It handles file encryption within an isolated sandbox environment (`target_folder`) and must never be executed on production systems.

## 🛠️ Architecture & Mechanism
This project utilizes **AES-128 bit symmetric encryption in CBC mode** via Python's `cryptography` library (Fernet specs). 

* **The Attacker Vector (`encryptor.py`):** Generates a unique secure key, drops it locally to disk (`secret.key`), loops dynamically through an isolated directory, and overwrites existing data blocks into cipher text.
* **The Defender Vector (`decryptor.py`):** Acts as an Incident Response utility. It safely reads the cryptographic key structure and cleanly reverses the cipher strings back into plain text.

## 🚀 How to Run the Lab

1. Clone the project and navigate inside:
   ```bash
   git clone [https://github.com/YOUR_USERNAME/Ransomware-Simulation-Lab.git](https://github.com/YOUR_USERNAME/Ransomware-Simulation-Lab.git)
   cd Ransomware-Simulation-Lab
