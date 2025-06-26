# Payload-Generator-Tool
A modular Python-based payload generator for offensive security testing — supporting XSS, SQL Injection, and Command Injection payloads with encoding, obfuscation, and output customization.

## Project Structure
payload-generator/
├── main.py # Entry point of the tool
├── cli.py # Argument parser logic
├── payload_encoder.py # Encoding functions (base64, URL, hex, unicode)
├── modules/ # Payload generation modules
│ ├── xss.py # XSS payloads + obfuscation
│ ├── sqli.py # SQLi payloads + obfuscation
│ └── cmd_injection.py # Command injection payloads + obfuscation
├── payloads/ # Payload list files
│ ├── xss_payload.txt
│ ├── sql_payloads.txt
│ └── cmd_payloads.txt
├── requirements.txt # Python dependencies
└── README.md # Project documentation

## Features

- **Payload Types**:
  - XSS 
  - SQL Injection 
  - Command Injection
  
- **Obfuscation Techniques**:
  - XSS: Unicode transformation
  - SQLi: SQL comment injection (`/**/`)
  - CMD: Bash tricks (`${IFS}`)

- **Encoding Options**:
  - Base64
  - URL
  - Hex (`\xXX`)
  - Unicode (`\uXXXX`)

- **Output Options**:
  - CLI (terminal)
  - JSON
  - Clipboard copy

---

## Usage

```bash
python3 main.py --xss
python3 main.py --sqli --obfuscate
python3 main.py --cmd --encode url --output json
python3 main.py --xss --encode base64 --clipboard


