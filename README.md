# Secure Host Hardening and Certificate Authority (CA) Setup

This project demonstrates automated host hardening using Bash scripting and the creation of a Root Certificate Authority using OpenSSL. It was completed as part of a cybersecurity milestone project, emphasizing secure configurations, cryptographic standards, and adherence to the CIA triad.

---

## 🔐 Project Goals

- Automate key hardening tasks (timezone, hostname, idle lockout, log exports)
- Display directory and certificate structures
- Build a Root CA with OpenSSL
- Generate and sign certificate requests
- Reinforce confidentiality, integrity, and availability through PKI

---

## 🧰 Tasks Performed

| Task                      | Description                                                                                              | Screenshot |
|---------------------------|----------------------------------------------------------------------------------------------------------|------------|
| Rename Hostname           | Set to `mmayobaker` using `sudo hostnamectl set-hostname mmayobaker`                                     | ![image](https://github.com/user-attachments/assets/e141fce6-45a0-4b0f-a4a0-9e6a98b10ad1) |
| Set Time Zone             | Configured system timezone to `America/Denver`                                                           | ![image](https://github.com/user-attachments/assets/1be4ceaa-dc86-49f8-a02f-a1a5f3748dcb) |
| Log Running Processes     | Used `ps aux >> process.txt` to log all active processes                                                 | ![image](https://github.com/user-attachments/assets/81dafa8d-a310-4c71-a5c3-66d8f532c828)<br>![image](https://github.com/user-attachments/assets/7967354d-a027-4746-b2a7-14109283b588) |
| Enforce Idle Lockout      | Used `gsettings` to enforce session lockout after 3 minutes of inactivity                               | ![image](https://github.com/user-attachments/assets/a85178de-1e15-4504-84d6-3c6ee6db8630) |
| Export Security Log       | Extracted last 50 lines from `/var/log/syslog` into `security_log_may_baker.txt`                         | ![image](https://github.com/user-attachments/assets/3f5553e1-8525-4372-8f54-dc8b11bef847) |
| Final Script              | Created and executed `finalScript.sh` to automate above steps                                            | ![image](https://github.com/user-attachments/assets/a46c39a0-0d21-400f-9d6d-b5eace0f278b) |
| Directory Tree Display    | Used `ls -R` to view directory structure of RootCA                                                       | ![image](https://github.com/user-attachments/assets/90645fd5-0f10-4c32-8e16-35742a20ee83) |
| DB Subfolder Listing      | Listed subfolders in `db/` from RootCA directory                                                         | ![image](https://github.com/user-attachments/assets/e90d1929-c1b0-4552-80f6-4ba1b5a4bfeb) |
| CA Config + Cert Request  | Edited `root-ca.conf`, then created CSR and private key using OpenSSL                                    | ![image](https://github.com/user-attachments/assets/dea7bd4a-aba9-4e97-bb31-9916692daf0f) |
| Self-Signed Certificate   | Signed the CSR with CA private key using `openssl ca -selfsign` command                                  | ![image](https://github.com/user-attachments/assets/2f759229-7272-40a7-ac3f-851d9771c895) |
| File Verification         | Verified `private/`, `issued/`, and `.csr` files using `ls -l`                                           | ![image](https://github.com/user-attachments/assets/f97a3557-e7d8-4b04-bf37-514326746e22) |

---

## 📂 Repository Structure
secure-host-hardening-and-pki/
├── finalScript.sh
├── process.txt
├── security_log_may_baker.txt
├── RootCA/
│   ├── conf/
│   │   └── root-ca.conf
│   ├── private/
│   │   └── root-ca.key
│   ├── issued/
│   │   └── root-ca.crt
│   ├── db/
│   └── root-ca.csr
├── screenshots/                # (Optional: all screenshots used in README)
├── README.md

---

## 📚 References

- [How to Create a CSR – DigiCert](https://knowledge.digicert.com/general-information/how-to-create-a-csr)  
- [Scripting Explained – Isecjobs.com (2025)](https://isecjobs.com/insights/scripting-explained/)  
- [PKI with OpenSSL – ThinkBox](https://blog.thinkbox.dev/posts/0011-pki-with-openssl)

---

## 💬 Final Thoughts

This project demonstrated the value of scripting, encryption, and layered security through real-world tools and hands-on implementation. From locking down a host to issuing digital certificates, every task reinforced the foundational importance of consistency, automation, and trust in cybersecurity operations.


