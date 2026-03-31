# Ransomware Simulation & Detection Project (Red Team + Blue Team)

## 📌 Project Overview
This project is a controlled ransomware simulation designed to demonstrate how ransomware attacks operate, how they impact systems, and how they can be detected and mitigated.

The project combines both offensive (red team) and defensive (blue team) perspectives to provide a complete understanding of ransomware behavior.

---

## 👨‍💻 Role & Objective

In this project, I acted as a cybersecurity analyst simulating:

- Ransomware attack behavior (encryption, persistence, user impact)
- Detection strategies used by security teams
- Defensive measures to mitigate ransomware threats

The goal is to bridge the gap between understanding attacks and defending against them.

## Technologies Used

- Python 3

- ```cryptography``` library

## Project Structure
```bash

The project is modular and structured to simulate real-world ransomware components:

Ransomware Simulation & Detection Project (Red Teamn + Blue Team)/
│
├── encryptor.py            # Main script to encrypt files and write ransom notes
├── decryptor.py            # Main script to decrypt files and restore original filenames
├── ransomware_gui.py       # GUI for the ransomware attack notifications (e.g., countdown, warnings)
├── decryption_gui.py       # GUI for showing decryption success and displaying decrypted files
├── persistence.py          # Persistence setup for simulating autostart on system boot
├── decryption_log.txt      # Log of decrypted files (generated after decryption)
├── key.key                 # Encryption key file used during encryption and decryption
├── ransom_note.txt         # Template ransom message (used in script)
├── ransomware_detector.py  # Detects suspicious activity 
├── demo_files/             # Directory containing demo files for encryption/decryption
└── README.md               # Project README file (this file)
```
## 🔐 Ransomware Simulation (Red Team Perspective)

### Attack Flow:

1. Traverse target directory (`demo_files`)
2. Identify files for encryption
3. Generate encryption key
4. Encrypt files using symmetric encryption (Fernet)
5. Rename files to simulate user confusion
6. Display ransom message via GUI
7. Simulate persistence (autostart behavior)

### Encryption Method:
- Uses Python `cryptography` library (Fernet)
- Demonstrates secure symmetric encryption principles

⚠️ Note:
In real-world ransomware, encryption keys are not stored locally but are securely exfiltrated or protected using asymmetric encryption.

## 🛡️ Detection & Defense (Blue Team Perspective)

This project also includes a ransomware detection module to simulate how security teams identify malicious activity.

### Detection Indicators:
- Rapid file modifications (mass encryption behavior)
- Suspicious file extensions or renamed files
- Unusual process activity
- Unexpected file access patterns

### Defensive Strategies:
- Monitor file system activity for anomalies  
- Use Endpoint Detection & Response (EDR) tools  
- Maintain regular backups  
- Restrict unauthorized script execution  
- Implement least privilege access controls  

## ⚠️ Risk & Impact Analysis

Ransomware attacks can result in:
- Data loss or inaccessibility  
- Operational downtime  
- Financial loss  
- Reputational damage  

This simulation highlights how quickly systems can be impacted if proper defenses are not in place.

## 📊 SOC Relevance

This project demonstrates skills relevant to Security Operations Center (SOC) roles:

- Understanding ransomware attack lifecycle  
- Threat detection awareness  
- Incident response thinking  
- Log and behavior analysis  
- Defensive security strategies  

## 🧪 Safe Testing Environment

All operations are limited to the `demo_files` directory to ensure safe execution.

## ⚠️ Disclaimer

This project is strictly for educational purposes.

Do NOT run on:
- Production systems  
- Personal devices with important data  

Always use controlled environments when testing.

## 🧠 Key Takeaway

Understanding how ransomware works is essential for building effective detection and response strategies. This project demonstrates both the attack mechanics and the defensive mindset required to mitigate such threats.

## Educational Use Cases

- Demonstrating the risk and behavior of ransomware.

- Teaching about cybersecurity and ethical hacking.

- Practicing threat detection and incident response in a lab environment.

## Authors

Uchendu, Favour Eni & Oladimeji, Richard
