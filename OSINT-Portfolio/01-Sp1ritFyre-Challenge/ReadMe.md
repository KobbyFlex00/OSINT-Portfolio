# 🕵️‍♀️ OSINT Investigation: Operation Sp1ritFyre

![Category](https://img.shields.io/badge/Category-OSINT-blue) ![Status](https://img.shields.io/badge/Status-Completed-success) ![Role](https://img.shields.io/badge/Role-Blue%20Team%20Analyst-orange)

## 📌 Project Overview
**Challenge Context:** CyberHouse Ghana Cyber Sentinels Training  
**Objective:** Perform Open Source Intelligence (OSINT) gathering on a specific target (`@sp1ritfyre`) to identify their digital footprint, real-world identity, and potential links to malicious activity.

This investigation simulates a real-world scenario of profiling a threat actor involved in a Managed Service Provider (MSP) breach.

---

## 🛠️ Tools & Techniques Used
* **Reconnaissance:** Manual Twitter Analysis, Web Correlation
* **Decoding:** CyberChef (Base64 De-obfuscation)
* **Search Operations:** Advanced Google Dorking
* **Attribution:** Username Enumeration, Metadata Analysis

---

## 🔍 Investigation Walkthrough

### Phase 1: Initial Reconnaissance
The starting point was a Twitter handle provided in the challenge scope.
* **Target:** `@sp1ritfyre`
* **Observation:**  
![Twitter Bio](OSINT-Portfolio/evidence/01-twitter-bio.png)

### Phase 2: Decoding & Pivoting
Suspecting encoded data, I used **CyberChef** to analyze the string.
* **Technique:** Base64 Decoding
* **Input:** `cmVkaHVudC5uZXQK`
* **Output:** `redhunt.net` (Target's personal website)  

![CyberChef Decode](OSINT-Portfolio/evidence/02-cyberchef-decode.png)

### Phase 3: Deep Dorking
Using the discovered domain, I performed Google Dorking to find correlated accounts and hidden pages.

**Query Used:**
```text
"redhunt.net" -site:redhunt.net
````

*Purpose: To find external sites (blogs, forums) that link back to the target's portfolio.*

**Result:**
This pivot revealed a Blogger profile (`sammiewoodsec.blogspot.com`) which contained the target's "About Me" page.

![Blog Profile](OSINT-Portfolio/evidence/03-blog-profile.png)

---

## 📊 Findings & Profile Summary

Through cross-referencing the blog, website, and social media, I established the following profile:

| Attribute          | Detail Discovered                            |
| :----------------- | :------------------------------------------- |
| **Real Name**      | Sammie Woods                                 |
| **Alias**          | Sp1ritFyre                                   |
| **Location**       | United Kingdom                               |
| **Occupation**     | Junior Penetration Tester                    |
| **Email**          | `d1ved33p@gmail.com`                         |
| **Malicious Link** | Linked to MSP Data Breach & Credential Sales |

---

## 🧠 Skills Demonstrated

* **Digital Footprinting:** Mapping a target's presence across multiple platforms.
* **Data De-obfuscation:** Recognizing and decoding Base64 strings.
* **Pivot Logic:** Moving from a single handle to a full identity using search operators.
* **Reporting:** Documenting findings in a structured, actionable format.

---

## ⚠️ Disclaimer

*This project was performed as part of a cybersecurity training challenge (CTF). All "personally identifiable information" (PII) found refers to fictional characters created for the educational scenario. No real individuals were doxxed or investigated.*
