# Penetration Test Engagement Template

This repository provides a clean, standardized directory structure to use for a single penetration testing engagement. Clone this repository to a new local directory to kickstart your project and keep your findings organized.

## 🛑 **CRITICAL SECURITY WARNING** 🛑

**This repository is intended to be used as a PRIVATE repository on GitHub or your local machine.**

If you choose to use this template as a public repository, you **MUST NOT** commit any sensitive client or engagement data. For public use, this should only serve as a template.

### **Best Practice: Clone for Each Engagement**

The recommended workflow is to clone this repository into a new, local, and secure directory for each new client engagement.

```bash
# Example for a new project for "Acme Corp"
git clone https://github.com/jf773/Penetration-Test-Engagement-Template.git
cd ./Penetration-Test-Engagement-Template
```

**From this point on, all work should be done locally. Do not push engagement data back to the remote template repository.**

## 🚀 How to Use

1.  **Clone this repository** to a new directory named for your project.
2.  **Review the Scope:** Open `01_SCOPE/rules_of_engagement.md` and document the agreed-upon scope, IP ranges, and rules of engagement.
3.  **Start Working:** As you conduct your test, place relevant files into the appropriate directories:
    -   Nmap/Nessus outputs go into `02_SCANS/`.
    -   Tool logs (Burp, Metasploit) go into `03_LOGS/`.
    -   Evidence (screenshots, exfiltrated data) goes into `04_EVIDENCE/`.
4.  **Handle Credentials Safely:** Any credentials you find should be stored in the `04_EVIDENCE/credentials/` directory. **This directory is explicitly ignored by `.gitignore` and its contents will NOT be committed to Git.**
5.  **Document Findings:** Use `06_REPORTING/findings.md` to keep a running list of vulnerabilities and observations for your final report.

## 📁 Directory Structure Explained

-   `01_SCOPE/`: Contains defining documents for the engagement, like the Rules of Engagement (RoE) and target IP lists.
-   `02_SCANS/`: Raw output from scanning tools (e.g., Nmap, Nessus, Nikto).
-   `03_LOGS/`: General-purpose logging from interactive tools (e.g., Metasploit console output, proxy logs).
-   `04_EVIDENCE/`: Where all evidence of vulnerabilities and exploitation is stored.
    -   `screenshots/`: Screenshots of successful exploits or interesting findings.
    -   `data/`: Exfiltrated data, such as configuration files, user lists, or database dumps.
    -   `credentials/`: **(GIT IGNORED)** A safe, local-only space to store captured credentials, hashes, or API keys.
-   `05_TOOLS/`: Any specific scripts, binaries, or tools used during the engagement.
-   `06_REPORTING/`: Notes, drafts, and key findings that will be used to construct the final report.
-   `.gitignore`: **(CRUCIAL)** This file prevents sensitive files and the entire `credentials` directory from being accidentally committed.

## ✍️ License

This template is provided under the [MIT License](LICENSE). Adapt it to fit your personal workflow.
