# Comparative Analysis of Advanced MFA Approaches in PAM Products Against Phishing-Based Cyberattacks

**Authors:**  
- **Kübra Nur Canbay**, Gazi University, Graduate School of Natural and Applied Sciences, Department of Mathematics, Ankara, Turkey  
  ORCID: https://orcid.org/0000-0002-3608-4483  
  Email: kubranurcanbay@gmail.com  
- **Osman Kaan Kars**, Yeditepe University, Faculty of Engineering, Department of Computer Engineering, Istanbul, Turkey  
  ORCID: https://orcid.org/0009-0003-3490-8412  

## Abstract

This work provides a focused comparison of advanced Multi-Factor Authentication (MFA) approaches used in Privileged Access Management (PAM) environments, specifically evaluating their resistance to modern phishing and Man-in-the-Middle (MitM) attacks. The study analyzes three primary advanced MFA methods:

- **FIDO2 / WebAuthn (Passkeys & Hardware Security Keys)**
- **Device-Integrated Biometric Authentication**
- **Certificate-Based Smart Cards (PKI)**

Traditional OTP-based MFA methods (SMS, email, mobile app OTP, push notifications, hardware tokens) are also assessed to highlight their limitations.

---

## 🎯 Purpose
Privileged accounts are the highest-value targets in an enterprise. As phishing techniques evolve—via fake login portals, reverse-proxy MitM tools, SIM-swapping, push-bombing, and social engineering—authentication becomes a critical weakness.  
This summary captures the key insights into which MFA technologies offer *true phishing resistance* for PAM systems.

---

## 🔍 Key Findings

### **1) FIDO2 / WebAuthn — Strongest Protection**
- Phishing success rate: **2%**
- MitM bypass rate: **0.5%**
- Cryptographic origin binding prevents credentials from being replayed on phishing domains.
- Highly usable; supports passwordless flows.

### **2) Biometrics — High Security + Excellent Usability**
- Phishing success rate: **3%**
- MitM bypass rate: **2%**
- Biometric templates stay on the device and unlock private keys locally.
- Seamless user experience.

### **3) Certificate-Based Smart Cards — Secure but Complex**
- Phishing success rate: **5%**
- MitM bypass rate: **8%**
- Strong physical security but high deployment and maintenance cost.
- Lowest usability.

### **4) Traditional OTP MFA (Including Kron PAM Built-ins)**
| MFA Method | Phishing | MitM |
|------------|----------|------|
| Hardware OTP Token | 10% | 15% |
| Mobile App OTP | 15% | 20% |
| Push Notifications | 25% | 30% |
| Email OTP | 35% | 40% |
| SMS OTP | 45% | 50% |

➡ OTP methods lack origin binding and are highly vulnerable to phishing and proxy-based attacks.

---

## 🧪 Method Overview
The evaluation included:
- Credential-harvesting phishing sites  
- Reverse-proxy MitM simulations (Evilginx2)  
- SIM-swapping  
- Push-bombing (MFA fatigue)  
- False Acceptance / False Rejection testing  
- Usability and deployment cost scoring  

---

## 📌 Recommendations
- Prefer **phishing-resistant MFA** for privileged accounts:  
  **FIDO2/WebAuthn** and **biometric-backed FIDO authenticators**.
- Avoid SMS/Email OTP for PAM access due to high compromise rates.
- PAM vendors should expand full WebAuthn/FIDO2 support across all login flows (portal + SSH/RDP proxy).
- Introduce risk-adaptive MFA that strengthens authentication based on context, user behavior, and environment.

---

## 🧾 Conclusion
FIDO2 and device-integrated biometric authentication offer the strongest protection against phishing in PAM environments, combining high security with excellent usability. Traditional OTP methods remain inadequate against modern phishing and MitM attacks. The study highlights that the future of PAM authentication lies in passwordless, phishing-resistant MFA.
