# Payload-Generator-Tool
A modular Python-based payload generator for offensive security testing — supporting XSS, SQL Injection, and Command Injection payloads with encoding, obfuscation, and output customization.
## Features

- **Payload Types**:
  - XSS (Reflected, DOM-based)
  - SQL Injection (Error-based, Union, Blind)
  - Command Injection (Linux & Windows variants)
  
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

## Installation

```bash
git clone https://github.com/your-username/payload-generator.git
python3 main.py --xss
python3 main.py --sqli --obfuscate --clipboard
python3 main.py --cmd –encode base64
