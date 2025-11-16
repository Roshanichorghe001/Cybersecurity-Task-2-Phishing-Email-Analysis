# Cyber Security Internship – Task 2  
## Phishing Email Analysis Report

### 📌 Objective  
Identify phishing characteristics in a suspicious email using header analysis tools and document all indicators.

---

## 📥 1. Phishing Email Sample Used  
A dummy phishing email was created for analysis.  
The file **phishing_email_sample.txt** contains:

- Complete email header  
- Full email body  
- Fake sender domain  
- Warning/urgent message  
- Suspicious link  

This sample was used to simulate a real-world phishing attempt.

---

## 📑 2. Tools Used  
- **MXToolbox Header Analyzer**  
  (Used to analyze SPF, DKIM, DMARC, mail server, routing, sender details)

---

## 🕵️‍♀️ 3. Header Analysis Summary  

### ✔ Sender Email  
`support@sbi-secure-verification.com`  
➡ Not an official SBI domain. Fake/unknown sender.

### ✔ SPF Result: **FAIL**  
The IP sending the mail is not authorized for this domain.  
➡ High chance of spoofing.

### ✔ DKIM Result: **FAIL**  
No DKIM signature found.  
➡ Email authenticity cannot be verified.

### ✔ DMARC Result: **FAIL**  
Domain policy would reject this email.  
➡ Strong indicator of phishing.

### ✔ Return-Path Mismatch  
Return-path domain did not match the "From" address.  
➡ Spoofed sender identity.

### ✔ Server Reputation  
Mail routed from unknown/suspicious mail server IP.  
➡ Common trait in phishing emails.

(Analysis screenshots are included in the **screenshots** folder.)

---

## ⚠️ 4. Phishing Indicators Found  

1. **Fake sender domain** (similar name but not official SBI domain)  
2. **Urgent/Threatening language**:  
   “Your account will be blocked in 24 hours”  
3. **Suspicious link** disguised as SBI verification page  
4. **SPF/DKIM/DMARC failures**  
5. **Mismatch in header fields**  
6. **No official contact info provided**  
7. **Unsecure URL format**  
8. **Generic greeting ("Dear Customer") instead of real name**

---

## 🧠 5. Learnings from the Task  

- How to read and interpret email headers  
- How SPF, DKIM, DMARC help validate email authenticity  
- How phishing emails manipulate users with fear/urgency  
- How to identify suspicious link/domain patterns  
- How to verify if a sender is spoofed

---

## 🔚 Conclusion  
Based on header authentication failures, mismatched domains, suspicious links, and threatening language,  
**this email is confirmed to be a phishing attempt.**

This report demonstrates the ability to analyze email threats and identify phishing characteristics effectively.

---

### 📎 Files Included  
- `phishing_email_sample.txt`  
- `README.md` (this report)  
- `screenshots/` folder (MXToolbox analysis)

---

### ✔ Task Completed
