# 🔐 CyberSecurity Task 1 – Port Scanning with Nmap

Welcome to my Day 1 Internship Task at **Elevate Labs**!  
This task focuses on **network enumeration and port scanning** using the powerful tool `Nmap`.

---

## 📌 Task Objective

Perform a **TCP SYN scan** on the local network using `Nmap`, identify active devices, open/filtered ports, and document the results.

---

## 🛠 Tools & Environment

| Tool        | Details                          |
|-------------|----------------------------------|
| OS          | Windows 10                       |
| Nmap        | Version 7.97                     |
| Subnet Used | `192.168.1.0/24`                 |
| CIDR Notation | `/24` (from Subnet Mask 255.255.255.0) |

---

## 🔎 Scan Command Used

```bash
nmap -sS 192.168.1.0/24 -oN result.txt
-sS: TCP SYN scan

-oN: Save output to result.txt

📄 Key Results
IP Address	Ports Open/Filtered	MAC Vendor
192.168.1.1	23 (filtered), 53, 80, 443 (open)	ZTE
192.168.1.20	All 1000 ports closed	Xiaomi Communications
192.168.1.21	All 1000 ports closed	Unknown
192.168.1.22	All 1000 ports closed	Samsung Electronics
192.168.1.23	9100 (JetDirect)	Unknown
192.168.1.24	23, 80 (open), 8000 (filtered)	Shiyuan Tech (Guangzhou)
192.168.1.45	135, 139, 445, 903, 3306, 5432 (open)	Host Machine (Trishul)

📘 Files in This Repo
File Name	Description
result.txt	Raw scan output from Nmap
Day 1 Internship Report.docx	Detailed technical report
README.md	This file – overview of the repo

📚 What I Learned
CIDR notation and subnet calculation

TCP SYN scanning using Nmap

Interpreting port scan results

Documenting cybersecurity analysis professionally

📎 Author
Konakalla Trishul
Intern at Elevate Labs | Passionate about Cybersecurity 🔐
GitHub Profile
