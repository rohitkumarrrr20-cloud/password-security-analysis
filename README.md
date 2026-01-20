# password-security-analysis
Practical analysis of password hashing, cracking techniques using Hashcat &amp; John the Ripper, and implementation of strong authentication with MFA.
# 🔐 Password Security & Authentication Analysis

**Author:** Ch Rohit Kumar  
**Email:** rohitkumarrrr20@gmail.com  
**University:** Aditya University  

---

## 📌 Project Overview
Passwords remain the most widely used authentication method, yet many users still rely on weak credentials such as `123456`, `password`, or `admin`. This project analyzes:

- How passwords are stored using hashing  
- How attackers crack weak passwords  
- Comparison of Hashcat and John the Ripper  
- Importance of Multi-Factor Authentication (MFA)  
- Best practices for strong authentication  

The goal is to understand real-world password attacks and how to defend against them.

---

## 🎯 Objectives

- Understand secure password storage using hashes  
- Identify different hash types (MD5, SHA-1, bcrypt)  
- Generate and analyze sample hashes  
- Perform dictionary & brute force attacks  
- Compare Hashcat vs John the Ripper  
- Study why weak passwords fail  
- Learn the importance of MFA  

---

## 🛠 Tools Used

### Primary Tools

#### Hashcat
- GPU/CPU based password cracking  
- Supports MD5, SHA, NTLM, bcrypt  
- Very fast and efficient  

#### John the Ripper
- CPU based cracking  
- Supports wordlist & brute force  
- Excellent for hash analysis  

---

## 📖 Theory

### What is Hashing?
Hashing converts a password into a fixed length value.

Example:  
```
Password: hello123  
Hash: 5d41402abc4b2a76b9719d911017c592
```

- One-way process  
- Cannot be directly reversed  
- Used for secure storage  

### Common Hash Types

| Algorithm | Features | Security |
|---------|-----------|---------|
| MD5 | 32 hex chars | Weak |
| SHA-1 | 40 hex chars | Weak |
| bcrypt | Slow + salted | Strong |
| Argon2 | Modern | Very Strong |

---

## 🧪 Practical Work

### 1. Hash Generation
Test passwords used:

**Weak**
- 123456  
- password  
- admin123  
- qwerty  

**Strong**
- Rohith@2026#Secure  
- Mfa+Strong!Pass99  

### 2. Hash Identification
- 32 hex → MD5  
- 40 hex → SHA-1  
- $2y$ → bcrypt  

### 3. Cracking with Hashcat

```bash
hashcat -m <type> -a 0 hashes.txt wordlist.txt
```

### 4. Cracking with John

```bash
john --wordlist=rockyou.txt hashes.txt
john --show hashes.txt
```

✅ Result: Weak passwords cracked within seconds.

---

## ⚔ Attack Types

### Dictionary Attack
- Uses common password lists  
- Very fast  
- Works on predictable passwords  

### Brute Force
- Tries all combinations  
- Slow for long passwords  
- Guaranteed with enough time  

---

## ❌ Why Weak Passwords Fail

- Too short  
- Common patterns  
- Dictionary words  
- No symbols  
- Password reuse  

---

## 🔑 Multi Factor Authentication

### MFA Uses:
- Something you know – password  
- Something you have – OTP  
- Something you are – biometrics  

✅ Even if password is cracked, account stays s
