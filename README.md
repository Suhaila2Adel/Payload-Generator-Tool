# Payload-Generator-Tool
A modular Python-based payload generator for offensive security testing — supporting XSS, SQL Injection, and Command Injection payloads with encoding, obfuscation, and output customization.

## Project Structure
payload-generator/
├── main.py
├── cli.py
├── payload_encoder.py
├── modules/
│   ├── xss.py
│   ├── sqli.py
│   └── cmd_injection.py
├── payloads/
│   ├── xss_payload.txt
│   ├── sql_payloads.txt
│   └── cmd_payloads.txt
└── README.md

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


