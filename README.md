# Secure Host Hardening & PKI Setup


This project demonstrates a full implementation of remote system hardening and a custom Public Key Infrastructure (PKI) using OpenSSL. It was built to support secure asset relocation in high-risk environments.

---

## 🔐 Key Components

- 🛡️ **System Hardening Script**
    - Applies baseline security configurations to newly deployed Linux machines
    - Disables unnecessary services
    - Configures automatic updates, auditing, and SSH hardening
    - Can be deployed remotely via SSH

- 🔏 **Certificate Authority (PKI)**
    - Sets up both **Root CA** and **Intermediate CA**
    - Uses secure OpenSSL configurations (`openssl.cnf`)
    - Supports certificate signing requests (CSRs) and certificate revocation lists (CRLs)
    - Logs and organizes certs in a modular folder structure

---

## 🧠 Project Objectives

- Create a hardened, cert-backed endpoint deployment process  
- Automate encryption standards using a custom OpenSSL configuration  
- Apply cryptographic best practices (RSA 4096, SHA256, serial tracking)  
- Simulate a CA environment for organizational internal use

---

## 🛠️ Tech Stack

- **Bash**  
- **OpenSSL**  
- **Linux (Debian-based)**  
- **Manual + Automated CLI interaction**  

---

## 📁 File Structure Overview
![Screenshot 2025-06-28 111026](https://github.com/user-attachments/assets/0e322170-ca02-4f6c-ba80-7ef9c026dc59)

---

## 🚧 Status

✅ **Hardening script complete**  
✅ **CA directory structure implemented**  
🧠 **Additional automation in progress** (CSR generation + remote deployment)

---

## 📸 Screenshots (To Be Added)
Add screenshots of:
- Hardened system checklist
- Terminal logs showing successful cert creation
- `openssl.cnf` config logic
- Directory structure in action

---

## 💡 Use Cases

- Secure system provisioning for enterprise or hybrid environments  
- Labs and demonstrations for PKI training  
- Resume/portfolio showcase for security ops interviews

---

## 👩🏽‍💻 Author

**Marjean Mayo-Baker**  
Cybersecurity Engineer | Automation Enthusiast | AI Security Researcher  
[LinkedIn](https://linkedin.com/in/marjean-mayo-baker)

