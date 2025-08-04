# 🔐 CyberSecurity Task 1 – Port Scanning with Nmap

Welcome to my **Day 1 Internship Task** at **Elevate Labs**!  
This task was focused on performing **port scanning and network enumeration** using the tool **Nmap**, a vital skill in cybersecurity.

---

## 📌 Task Objective

To perform a **TCP SYN Scan** using Nmap on the local network to:
- Identify **live hosts** on the network
- Detect **open/filtered/closed ports**
- Learn about **subnetting**, **CIDR notation**, and **scan interpretation**
- Save and document scan output results

---

## 🛠 Tools & Environment

| Tool/Concept       | Description                                      |
|--------------------|--------------------------------------------------|
| 💻 Operating System | Windows 10 (Command Prompt)                     |
| 🔍 Scanner Tool     | Nmap v7.97 + Npcap driver                        |
| 🌐 Subnet Used      | `192.168.1.0/24` – based on my IP configuration |
| 🧠 Concept Focus     | Subnetting, TCP ports, SYN scan, CIDR notation  |

---

## 🧾 Step-by-Step Procedure

### ✅ 1. **Check your IP Address**
```bash
ipconfig
This gave me my local IP:

nginx
Copy
Edit
IPv4 Address: 192.168.1.45
Subnet Mask: 255.255.255.0
From the subnet mask, we calculate the CIDR notation:
255.255.255.0 → 8 + 8 + 8 = /24
So our network range is: 192.168.1.0/24

✅ 2. Navigate to Nmap Directory
bash
Copy
Edit
cd "C:\Program Files (x86)\Nmap"
✅ 3. Run TCP SYN Scan and Save Result
bash
Copy
Edit
nmap -sS 192.168.1.0/24 -oN result.txt
🔍 Explanation:
Command	Meaning
-sS	TCP SYN Scan (Stealth scan)
192.168.1.0/24	Scans IP range from .0 to .255
-oN result.txt	Save output in normal format to a file

📄 Key Results
IP Address	Ports Detected	MAC Vendor
192.168.1.1	23 (filtered), 53, 80, 443 (open)	ZTE
192.168.1.20	All 1000 ports closed	Xiaomi Communications
192.168.1.21	All 1000 ports closed	Unknown
192.168.1.22	All 1000 ports closed	Samsung Electronics
192.168.1.23	9100 (open - JetDirect printer port)	Unknown
192.168.1.24	23, 80 (open), 8000 (filtered)	Guangzhou Shiyuan Tech
192.168.1.45	135, 139, 445, 903, 3306, 5432 (open)	My own system (Trishul)

🖼️ Screenshots (Optional)
To visually validate the task, I captured key screenshots and uploaded them to the repo.

Step	Screenshot
IP Config	
Nmap CMD	
Output	
GitHub Repo	

Ensure image files are present in the repo for them to render.

📁 Files in This Repository
File Name	Description
result.txt	Raw scan output saved from Nmap
Day 1 Internship Report.docx	Detailed documentation of the task
Day1_Screenshots_Trishul.docx	All screenshots captured from the scan
README.md	This file – serves as a project overview

📚 What I Learned
✔️ CIDR Notation & Subnetting
✔️ How to find local IP and calculate IP ranges
✔️ How to use Nmap and its basic options
✔️ TCP SYN Scan behavior and when it’s used
✔️ Open vs filtered vs closed ports
✔️ How to identify vendors from MAC addresses
✔️ Creating technical documentation and versioning with GitHub
✔️ Professional task submission practices

🧑‍💻 Author
Konakalla Trishul
Intern – Elevate Labs | Aspiring Cybersecurity Analyst 🔐
GitHub Profile

