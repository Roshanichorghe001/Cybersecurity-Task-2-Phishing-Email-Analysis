# Cybersecurity Task 2 – Phishing Email Analysis  
**Internship Task – Phishing Email Header & Content Analysis**

This repository contains the analysis of a suspicious email received for the Cybersecurity Internship Task 2.  
The analysis includes:  
- Email content inspection  
- Header investigation  
- SPF/DKIM/DMARC verification  
- Indicators of phishing  
- Final conclusion  

---

## 📌 1. Email Content (from TXT File)

**Sender:** SBI Support  
**Email:** support@sbi-secure-verification.com  
**Subject:** *"Urgent! Your SBI account will be blocked in 24 hours!"*  

### **Content Summary**
The email claims the user's SBI bank account will be blocked within 24 hours and urges the user to click a verification link. The message uses fear and urgency to trick the user into giving credentials.

---

## 📌 2. Email Headers (From Screenshot)

### **Headers Extracted**
| **Header Name** | **Header Value** |
|----------------|------------------|
| **From** | SBI Support <support@sbi-secure-verification.com> |
| **To** | chorgheroshani205@gmail.com |
| **Subject** | Urgent! Your SBI account will be blocked in 24 hours! |
| **Message ID** | <93hf83hdsf8sd9f8sd@secure-update-banking.com> |
| **Created On** | 16 November 2025 • 14:04 |
| **Mailed-by** | sbi-secure-verification.com |
| **Signed-by** | NONE |

---

## 📌 3. Authentication Results  
(From Screenshot – SPF, DKIM, DMARC)

| **Protocol** | **Result** | **Details** |
|--------------|------------|-------------|
| **SPF** | ❌ FAIL | IP 185.222.202.19 is **NOT authorized** |
| **DKIM** | ❌ FAIL | No DKIM signature found |
| **DMARC** | ❌ FAIL | Domain policy = reject |

This means the domain did **not** authorize the sender → Strong sign of spoofing.

---

## 📌 4. Detailed Phishing Indicators

### **1. Fake Domain Used**
`sbi-secure-verification.com` is NOT an official SBI domain.  
Official SBI domains use:  
- `sbi.co.in`  
- `onlinesbi.com`

### **2. Urgency and Threat Language**
Words used:  
- *"Urgent"*  
- *"Account will be blocked in 24 hours"*  
These are common phishing techniques.

### **3. SPF/DKIM/DMARC All Failed**
All three authentication failures clearly show the email is spoofed.

### **4. Suspicious Message-ID**
`secure-update-banking.com` is not related to SBI.

### **5. No Digital Signature**
Signed-by = NONE → Legit banks always use DKIM signatures.

---

## 📌 5. Conclusion  
Based on header analysis, failed authentication, suspicious domain, and threatening language, **this email is 100% a phishing email**.  
The attacker attempted to impersonate SBI banking services to steal login details.

---

## 📁 Files in This Repository
- `phishing_email_sample.txt` → Full email content  
- `email_headers_screenshot.png` → Header result screenshot  
- `analysis.txt` → Step-by-step explanation (if added)  
- `README.md` → Complete documentation  

---

## 📌 6. Purpose of This Repository
This GitHub repository is created as part of **Cybersecurity Internship Task 2**, where the objective is to analyze a suspicious email and provide a detailed technical report with evidence.

---

## 📌 7. How to View
Simply open the files in this repository.  
Screenshots can be found in the `/screenshots` folder (if added).

---

## ✔️ Status:  
**Task Completed & Ready for Review**  
