# Network-lab-test
Learning nmap,wireshark to perform scan and address ip,open ports.

## 🚀 Lab Details

- **Environment:** VMware 17 Player  
- **OS:** Kali Linux (VM)  
- **Test Network:** `192.168.131.0/24` subnet

---

## 🔧 Tools Covered

- **Nmap**: Network exploration and port scanning
- **Wireshark**: Packet capture and analysis

---

## 📚 What You'll Find Here

- **Installation guides** for each tool (Kali Linux focus)
- **Step-by-step instructions** for scanning IPs and ports with Nmap
- **Network traffic capture and analysis** using Wireshark
- **Basic intrusion detection** with Snort
- **Example bash scripts** for automating scans and captures
- **Beginner tips** on spotting security risks in your network

---

## 🖥️ Lab Setup

1. **Install VMware 17 Player**
2. **Download and install Kali Linux VM**
3. **Configure your VM network** to `192.168.131.0/24`

---

## 1️⃣ Installing Nmap

```bash
sudo apt update
sudo apt install nmap
```
Verify installation:
```bash
nmap --version
```

---

## 2️⃣ Scanning IPs and Open Ports

Scan the whole subnet:
```bash
nmap -sn 192.168.131.0/24
```
Scan a specific machine for open ports:
```bash
nmap -v -A 192.168.131.10
```

---

## 3️⃣ Capturing and Analyzing Packets with Wireshark

Install Wireshark:
```bash
sudo apt update
sudo apt install wireshark
```
Start Wireshark (as root to see all interfaces):
```bash
sudo wireshark
```
- Select your VM’s network interface.
- Start capture, filter traffic (e.g., `ip.addr == 192.168.131.10`).
- Analyze HTTP, DNS, suspicious packets.

---
## 4️⃣ Basic Intrusion Detection with Snort

Install Snort:
```bash
sudo apt update
sudo apt install snort
```
Run Snort in packet logging mode:
```bash
sudo snort -i eth0 -l /tmp/snort-logs -c /etc/snort/snort.conf

------


## ⚠️ Possible Security Risks to Watch For

- Unusual open ports (e.g., 23/Telnet, 445/SMB)
- Unknown services running on hosts
- Suspicious packet payloads (malformed, strange protocols)
- Frequent failed login attempts or port scans in Snort logs
**https://prince-cyber7.github.io/Network-lab-test/lab-test.html**
---
*Feel free to suggest improvements!*
