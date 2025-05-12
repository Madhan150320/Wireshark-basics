# Wireshark-basics
Hands-on Wireshark project focused on analyzing HTTP, DNS, and other network protocols as part of my cybersecurity training.

```
wireshark-basics
```

```markdown
# 🕵️‍♂️ Wireshark – Network Traffic Analysis

This repository documents my hands-on learning with **Wireshark**, a powerful open-source packet analyzer. As part of my cybersecurity training, I used Wireshark to capture, filter, and analyze network traffic for educational and ethical purposes.

---

## 📌 What is Wireshark?

Wireshark is a network protocol analyzer that lets you inspect network traffic in real time. It’s widely used in cybersecurity for:
- Packet inspection
- Protocol analysis
- Troubleshooting networks
- Detecting suspicious or malicious activity

---

## 🧰 Tools & Environment

- **Wireshark** (GUI-based packet analyzer)
- **tcpdump** (for command-line captures)
- **Kali Linux / Ubuntu** OS
- **Sample PCAP files** (captured manually or downloaded)

---

## 🗂️ Repository Structure

```

wireshark-basics/
├── pcaps/
│   ├── http-traffic.pcapng
│   ├── dns-query.pcapng
├── screenshots/
│   ├── http-get-request.png
│   ├── dns-analysis.png
├── filters/
│   └── common\_display\_filters.txt
├── notes/
│   └── wireshark-tips.md
├── README.md

````

---

## 🧪 What I Did

### 1️⃣ Captured HTTP Traffic
- Opened Wireshark and started capturing on interface `eth0`.
- Visited a website over HTTP.
- Filtered using:  
  ```wireshark
  http.request
````

### 2️⃣ Analyzed DNS Queries

* Used filter:

  ```wireshark
  dns && ip.addr == 8.8.8.8
  ```

### 3️⃣ Extracted Login Info (HTTP)

* Captured POST request over HTTP (non-HTTPS) to demonstrate credential exposure.
* Exported as screenshot: `http-get-request.png`

---

## 📘 Common Display Filters

```
http
tcp.port == 80
ip.addr == 192.168.1.5
dns
ftp
ssl || tls
```

See `filters/common_display_filters.txt` for more.

---

## 📚 What I Learned

* How to capture live network packets safely
* The difference between HTTP and HTTPS in packet visibility
* How DNS queries can expose domain history
* How filters work to isolate meaningful traffic
* Basics of protocol-level analysis

---

## ⚠️ Disclaimer

> This project is intended for **ethical and educational use only**. All traffic was either generated on my own system or downloaded from safe public sources. Do not use Wireshark to capture or analyze traffic without proper authorization.
