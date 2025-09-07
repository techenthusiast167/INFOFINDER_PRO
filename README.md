# INFOFINDER_PRO

A comprehensive Python-based OSINT (Open Source Intelligence) tool for email and phone number verification with breach detection, social media lookup, and digital footprint analysis capabilities.


---

# Table of Contents

- Overview

- Features

- Importance in OSINT & Cybersecurity

- Installation

- Dependencies

- Usage

- Examples

- API Keys Configuration

- Output Examples

- Contributing

- Disclaimer


---

# Overview

Cyber Intel OSINT Tool is a powerful Python application designed for cybersecurity professionals, digital investigators, and ethical hackers. It provides comprehensive analysis of email addresses and phone numbers, helping to identify potential security risks, data breaches, and digital footprints across multiple platforms.


---

# Features

**Email Analysis**

- Syntax Validation: Validates email format and structure

- MX Record Check: Verifies domain mail exchange records

- Disposable Email Detection: Identifies temporary email services

- Breach Database Check: Searches HaveIBeenPwned for data breaches

- Gravatar Profile Lookup: Checks for Gravatar profiles

- GitHub Account Search: Finds GitHub users associated with email

- Social Media Search: Generates search URLs across multiple platforms

- Email Verification: Uses Hunter.io API for email validation

- Pastebin Scanning: Checks for email exposure in public pastes

- Name Extraction: Intelligently extracts names from email addresses

- Social Deep Dive: Comprehensive social media analysis


---

**Phone Number Analysis**

- Number Validation: Validates phone number format and existence

- Carrier Identification: Identifies mobile network carriers

- Geolocation: Determines approximate geographical location

- Timezone Detection: Identifies relevant timezones

- Google Dorking: Generates search queries for OSINT investigations

---

**Reporting**

- CSV Reports: Exports findings to CSV format

- PDF Reports: Generates detailed PDF reports

- Color-coded Output: Terminal output with intuitive color coding

---

# Importance in OSINT & Cybersecurity

**For Digital Investigators**


- **Threat Intelligence**: Identify potential threats through digital footprint analysis

- **Identity Verification**: Confirm subject identities through multiple data points

- **Connection Mapping**: Establish relationships between different data elements

---

**For Cybersecurity Professionals**


- **Breach Assessment**: Determine if credentials have been compromised

- **Attack Surface Analysis**: Identify exposed information that could be leveraged in attacks

- **Social Engineering Defense**: Understand what information is publicly available

---

**For Organizations**


- **Employee Security**: Check if corporate emails appear in data breaches

- **Third-party Risk Assessment**: Evaluate security posture of partners and vendors

- **Incident Response**: Quickly assess compromised accounts during security incidents

---

# Prerequisites

- Python 3.6 or higher

- pip (Python package manager)

---

**Manual Installation**

- Create your virtual environment

- Follow the link below, copy and install the tool script manually using nano: **https://gist.github.com/techenthusiast167/75e44a3f5e4abc268c9c86b098a85268**

**Example**:

- **nano infofinder_pro.py**
- Press **Ctrl + O, Enter, Ctrl + X** to save and exit

**Install Dependencies**

    pip install requests
    pip install dnspython
    pip install phonenumbers
    pip install pandas
    pip install reportlab

**OR**

    pip install requests dnspython phonenumbers pandas reportlab

---

**Set Up API Keys (Optional but recommended)**

- Edit the script and add your **API keys** for enhanced functionality

---

# Usage

**Basic Command**


    python infofinder_pro.py

---

# Interactive Mode

**The tool launches in interactive mode, prompting you to**:


- Choose between email or phone number analysis

- Enter the target email or phone number

- View comprehensive results in the terminal

- Save reports in CSV and PDF formats

---

# Examples

**Email Analysis Example**


- python3 infofinder_pro.py

- **Select analysis type**:
  
  1. Email Analysis
  2. Phone Number Analysis

**Enter your choice (1 or 2):** 1
**Enter email address:** example@domain.com

---

**Phone Analysis Example**


- python3 infofinder_pro.py
  
- **Select analysis type:**

  1. Email Analysis
  2. Phone Number Analysis

**Enter your choice (1 or 2):** 2
**Enter phone number (with country code):** +1234567890

---

**Sample Output for Email Analysis**


**---[ EMAIL BREACH & SOURCE ANALYSIS ]---**

[OK] Email appears non-disposable.

**Checking breach databases...**

[FOUND] 3 breaches detected:

  - Adobe (2013-10-04)
  - LinkedIn (2012-05-05)
  - MySpace (2008-01-01)
  
**Extracted Name:** John Doe

**Social Media Searches:**

  Twitter: https://twitter.com/search?q=John+Doe
  Facebook: https://www.facebook.com/search/top/?q=John+Doe
  LinkedIn: https://www.linkedin.com/search/results/people/?keywords=John+Doe

---

**Sample Output for Phone Number Analysis**

**---[ PHONE NUMBER ANALYSIS ]---**

**Valid Number:** True
**International Format:** +234 810 477 2324
**National Format:** 0810 477 2324
**Location:** Nigeria
**Carrier:** MTN
**Timezone:** Africa/Lagos

**---[ OSINT RESULTS FOR +2348104772324 ]---**

**PHONE VALIDATION:**

  **Valid:** True
  **International Format:** +234 810 477 2324
  **National Format:** 0810 477 2324
  **Location:** Nigeria
  **Carrier:** MTN
  **Timezone:** Africa/Lagos

**GOOGLE DORKING SUGGESTIONS:**

  **Exact Phone Number:** https://www.google.com/search?q="+2348104772324"
  **Phone without Formatting:** https://www.google.com/search?q="2348104772324"
  **Phone in Text:** https://www.google.com/search?q=intext:"+2348104772324"
  **Phone on Social Sites:** https://www.google.com/search?q=site:facebook.com OR site:twitter.com "+2348104772324"

**REPORTS SAVED:**

**CSV:** cyber_intel_report_phone_2348104772324.csv
**PDF:** cyber_intel_report_phone_2348104772324.pdf

---

# API Keys Configuration

- For full functionality, obtain and configure these API keys:

**HaveIBeenPwned API**

- Visit **https://haveibeenpwned.com/API/Key**

- Sign up for an API key

- Add to script: **HIBP_API_KEY = "your_api_key_here"**

**Hunter.io API**

- Visit **https://hunter.io/api-keys**

- Create account and generate API key

- Add to script: **HUNTER_IO_API_KEY = "your_api_key_here"**


---

# Report Files

**The tool generates two types of reports:**

- **CSV Report:** Structured data for further analysis

- **PDF Report:** Formatted document for sharing and documentation

**Sample CSV output:**

**csv**

- Email,Disposable,Gravatar Found,Data Breaches,Email Reputation
- example@domain.com,No,Yes,3,Clean

---

# Contributing

**I welcome contributions to enhance INFOFINDER_PRO Tool:**

- Fork the repository

- Create a feature branch (git checkout -b feature/amazing-feature)

- Commit your changes (git commit -m 'Add amazing feature')

- Push to the branch (git push origin feature/amazing-feature)

- Open a Pull Request

---

# Disclaimer

**This tool is intended for:**

- Educational purposes

- Security research

- Authorized penetration testing

- Personal security assessment

**Use Responsibly:** Always ensure you have proper authorization before investigating email addresses or phone numbers. Unauthorized use may violate privacy laws and terms of service.



