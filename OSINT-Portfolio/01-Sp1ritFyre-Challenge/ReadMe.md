# 🕵️‍♀️ OSINT Investigation: Operation Sp1ritFyre

![Category](https://img.shields.io/badge/Category-OSINT-blue)
![Status](https://img.shields.io/badge/Status-Completed-success)
![Role](https://img.shields.io/badge/Role-Blue%20Team%20Analyst-orange)

## 📌 Project Overview
**Challenge Context:** CyberHouse Ghana Cyber Sentinels Training  
**Objective:** Conduct Open Source Intelligence (OSINT) investigation on the target `@sp1ritfyre` to uncover their digital footprint, identity, and potential ties to malicious activity.

This scenario simulates a real-world threat actor profiling exercise involving an MSP (Managed Service Provider) breach.

---

## 🛠️ Tools & Techniques Used
- **Reconnaissance:** Manual Twitter Profiling, Web Correlation  
- **Decoding:** CyberChef (Base64 De-obfuscation)  
- **Search Operations:** Google Dorking & OSINT Search Queries  
- **Attribution:** Username Enumeration, Metadata Correlation  

---

## 🔍 Investigation Walkthrough

### **Phase 1 — Initial Reconnaissance**
The provided starting point was a suspicious Twitter account.

**Target:** `@sp1ritfyre`  
**Observation:**  
![Twitter Bio](evidence/01-twitter-bio.jpeg)

---

### **Phase 2 — Decoding & Pivoting**
The profile contained an encoded string. I used **CyberChef** to investigate.

- **Technique:** Base64 Decoding  
- **Input:** `cmVkaHVudC5uZXQK`  
- **Output:** `redhunt.net` (Target’s personal website)

![CyberChef Decode](evidence/02-cyberchef-decode.jpeg)

---

### **Phase 3 — Deep Dorking**
Using the discovered domain, I pivoted via Google Dorking.

**Query used:**
```text
"redhunt.net" -site:redhunt.net
