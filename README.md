# Awesome-Email-Threat-Analysis

## Top Email Threat Analysis Platforms Ecosystem



**Curated List of SaaS Products & Open-Source GitHub Projects**

*Focused on Phishing Triage, Business Email Compromise (BEC) Detection, IOC Extraction & Email Forensics*

**Last updated: September 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **Email Threat Analysis**. These tools help SOC analysts, incident responders, and email security teams investigate suspicious emails, analyze headers, extract indicators of compromise (IOCs), and determine whether credentials were harvested or payloads delivered.



**Examples** include Abnormal Security, IRONSCALES, Proofpoint Threat Response, Mimecast Threat Center, Cofense Vision, Area 1 Security (Cloudflare), Material Security, Avanan, Barracuda Sentinel, and Darktrace Email (the category leaders).



**Open-source emphasis**: Email threat analysis has a **strong open-source ecosystem**—particularly for DFIR (Digital Forensics & Incident Response) workflows. Tools like **MXRay** and **PhishGuard v2** are specifically designed as open-source alternatives to commercial email triage platforms. Meanwhile, **Proxmox Mail Gateway** and **Rspamd** provide the gateway-level filtering foundation. This section is heavily expanded with every major active project for self-hosting, custom triage pipelines, and transparent analysis workflows.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents



- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **[Abnormal Security](https://abnormalsecurity.com/)**

  AI-native email security platform focused on detecting sophisticated BEC and social engineering attacks that bypass traditional secure email gateways. Uses behavioral AI to baseline normal communication patterns and identify anomalies .



- **[IRONSCALES](https://ironscales.com/)**

  AI-powered email security platform with automated phishing remediation. Uses community-powered threat intelligence and mailbox-level remediation to remove threats post-delivery .



- **[Proofpoint Threat Response](https://www.proofpoint.com/)**

  Automated incident response platform for email threats. Provides threat intelligence correlation, IOC extraction, and remediation workflows integrated with Proofpoint's email security suite .



- **[Mimecast Threat Center](https://www.mimecast.com/)**

  Threat intelligence and analysis module within Mimecast's email security platform. Provides real-time threat dashboards, IOC feeds, and investigation tools for security teams .



- **[Cofense Vision](https://cofense.com/)**

  Automated phishing triage and remediation platform. Focuses on human-reported phishing emails, automating analysis and removal of threats from user mailboxes .



- **[Area 1 Security (Cloudflare)](https://www.cloudflare.com/)**

  Email security platform (acquired by Cloudflare) specializing in pre-delivery phishing detection. Uses global threat intelligence to identify and block phishing campaigns before they reach inboxes.



- **[Material Security](https://material.security/)**

  Email security platform focused on BEC detection, account takeover prevention, and sensitive data protection within email. Provides automated remediation and risk scoring.



- **[Avanan (Check Point)](https://www.checkpoint.com/)**

  Cloud email security platform (acquired by Check Point) that protects Microsoft 365 and Google Workspace. API-based architecture with advanced phishing and BEC detection .



- **[Barracuda Sentinel](https://www.barracuda.com/)**

  AI-powered email security specifically designed for BEC and account takeover prevention. Focuses on impersonation detection and fraud prevention .



- **[Darktrace Email](https://darktrace.com/)**

  Self-learning AI email security platform. Uses unsupervised machine learning to detect novel phishing and BEC attacks without relying on signatures or rules .



## Open-Source GitHub Projects



- **[MXRay](https://github.com/cristianzsh/MXRay)**

  Open-source DFIR tool for parsing and analyzing email evidence (.eml, .msg, .pst, .ost, .mbox). Specifically designed as a **free alternative to commercial email analysis suites** for BEC investigations. Features header and authentication analysis (SPF/DKIM/DMARC verdicts, Received chain, spoofing detection), safe HTML rendering with no network stack, attachment triage (macros, steganography, double extensions, archives), YARA scanning with embedded rules, IOC extraction, and VirusTotal enrichment (opt-in). Python/PyQt6, ships as single self-contained executable .



- **[PhishGuard v2](https://github.com/shivamgit20/PhishGuard-v2)**

  Fully client-side, enterprise-grade phishing email analysis platform. Consolidates analyst triage workflow into a single structured pipeline. Features MIME parsing, complete header forensics (SPF/DKIM/DMARC), URL inspection, social engineering pattern detection, attachment risk profiling, IOC extraction (IPs, domains, hashes, CVEs, wallets), threat scoring (0-100), SEG Engine (rule-based classification), Sandbox Engine (YARA-driven behavioral analysis), and MITRE ATT&CK mapping. React + Vite, no external API calls .



- **[Wireshark Phishing Playbook](https://github.com/yankywilson/wireshark-phishing-playbook)**

  Practitioner-grade playbook for investigating phishing PCAPs with Wireshark/TShark. Phase-by-phase decision tree covering click confirmation, redirect chain mapping, credential POST detection, payload download identification, and C2 beacon analysis. Includes 80+ display filters, TShark one-liners, IOC extraction scripts, base64 fragment decoders, and beacon cadence analysis. Built on real Triage/ANY.RUN sandbox PCAPs .



- **[Rspamd](https://github.com/rspamd/rspamd)**

  Modern, fast open-source spam filtering system with multi-threaded architecture, Redis support, machine learning, and web UI. The de facto choice for gateway-level email filtering in 2026, increasingly replacing SpamAssassin for new deployments. Supports SPF/DKIM/DMARC verification and URL blacklist checking .



- **[Proxmox Mail Gateway](https://www.proxmox.com/en/proxmox-mail-gateway)**

  The leading open-source email security solution. Full-featured mail proxy deployed between firewall and internal mail servers. Features anti-spam (SpamAssassin), anti-virus (ClamAV), object-oriented rule system, message tracking center, spam quarantine, and REST API. Handles millions of emails per day with 100% open-source (AGPL v3) .



- **[SpamAssassin](https://github.com/apache/spamassassin)**

  The original open-source anti-spam framework. Rule-based heuristic engine combining Bayesian filtering, DNSBL checks, phrase matching, and custom rules. While Rspamd has become the default for new deployments, SpamAssassin remains a solid choice for existing deployments .



- **[MailScanner](https://github.com/MailScanner/mailscanner)**

  Open-source email security system designed for Linux-based email gateways. Used at over 30,000 sites worldwide. Can be combined with SpamAssassin and ClamAV for comprehensive protection .



- **[Scrollout F1](https://github.com/scrollout/f1)**

  Free self-hosted email gateway designed for administrators without advanced email security experience. Provides virus, spam, and phishing filtering with an intuitive setup process .



- **[ASSP](https://github.com/assp/assp)**

  Anti-Spam SMTP Proxy server implementing auto-whitelists, self-learning Hidden-Markov-Model/Bayesian filtering, Greylisting, DNSBL, URIBL, SPF, and virus scanning. Platform-independent .



- **[Odin's Eye](https://github.com/Deon-Trevor/Odin-s-Eye)**

  Sleek tool for comprehensive email analysis and insight discovery. Python-based .



- **[osprey](https://github.com/syne0/osprey)**

  PowerShell-based tool (fork of T0pCyber/hawk) for gathering information related to O365 intrusions and potential breaches. Useful for investigating BEC and account compromise .



### Additional Strong Open-Source Options



- **Email Forensics & Triage**: **MXRay** (DFIR-focused, BEC investigations), **PhishGuard v2** (client-side triage, MITRE mapping), **Wireshark Phishing Playbook** (PCAP-based post-click analysis) .

- **Gateway Filtering**: **Rspamd** (modern, ML-powered), **Proxmox Mail Gateway** (complete solution), **SpamAssassin** (legacy, still solid), **MailScanner** (multi-MTA support) .

- **IOC Extraction & Threat Intel**: **extract-iocs.sh** (from Wireshark playbook), **alphaSeclab/malware-ioc-hash** (IOC hash collection), **edoardottt/defango** (IOC defanging) .

- **O365 Investigation**: **osprey** (PowerShell, O365 intrusions), **Deon-Trevor/Odin-s-Eye** (Python, email analysis) .



**Frameworks for building custom systems**: Combine **Rspamd** or **Proxmox Mail Gateway** for gateway-level filtering, **MXRay** for DFIR-level email evidence analysis, **PhishGuard v2** for analyst triage workflows, and **Wireshark Phishing Playbook** for network-level post-click investigation. Add **ClamAV** for virus scanning and **Redis** for Rspamd statistics.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- Email threat analysis tools handle sensitive email communications; ensure compliance with data protection regulations and email retention policies.

- **Open-source reality**: Open-source email threat analysis is mature at the **gateway filtering** level (**Rspamd**, **Proxmox Mail Gateway**) and the **DFIR triage** level (**MXRay**, **PhishGuard v2**). However, AI-powered BEC detection with behavioral baselining—the core of **Abnormal Security**, **Material Security**, and **Avanan**—remains primarily commercial. Open-source alternatives rely on rules, signatures, and manual analysis rather than learned communication patterns.



---



**Made for SOC analysts, incident responders, email security engineers, and DFIR practitioners.**

Let's make email threat analysis more open, transparent, and effective.
