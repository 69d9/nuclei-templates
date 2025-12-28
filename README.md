#  Custom Nuclei Templates
A curated collection of custom Nuclei templates designed for bug bounty hunters, penetration testers, and security researchers.

These templates focus on real-world vulnerabilities with practical detection logic, organized by vulnerability category for easy usage and scalability.

Auth/ → Authentication & authorization issues

IDOR/ → Insecure Direct Object Reference (IDOR)

LFI/ → Local File Inclusion

Leaks/ → Sensitive information disclosure

OpenRedirect/ → Open redirect vulnerabilities

Rate/ → Rate limiting & brute-force issues

SQLi/ → SQL Injection vulnerabilities

Takeover/ → Subdomain takeover checks

XSS/ → Reflected, stored, and DOM-based XSS


#  Goals of This Repository

High-signal templates (low false positives)

Bug bounty–oriented detection logic

Easy integration with existing Nuclei workflows

Clean and readable YAML structure

Continuously expandable


## Usage

This repository contains custom Nuclei templates and can be used directly with ProjectDiscovery Nuclei.

### Clone the repository
```bash
git clone https://github.com/69d9/nuclei-templates.git
cd nuclei-templates

nuclei -u https://example.com -t .

---

nuclei -u https://example.com -t XSS/
nuclei -u https://example.com -t SQLi/
nuclei -u https://example.com -t IDOR/
nuclei -u https://example.com -t Auth/
nuclei -u https://example.com -t LFI/
nuclei -u https://example.com -t OpenRedirect/
nuclei -u https://example.com -t Rate/
nuclei -u https://example.com -t Takeover/
nuclei -u https://example.com -t Leaks/

---

nuclei -l targets.txt -t .

---

nuclei -u https://example.com -t . -o results.txt
