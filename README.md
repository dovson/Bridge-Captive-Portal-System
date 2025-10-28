# 🧩 Captive Portal Project (NDIS Filter + Internal DHCP/DNS)

![Captive Portal Demo](images/demo_screenshot.png)

## 📖 Overview
This project is a custom-built **captive portal system** designed for Windows, implementing a **network-level access control system** using a custom **NDIS filter driver**.

It intercepts packets at the data-link layer to manage user sessions, authentication, and data accounting — similar to commercial solutions used by ISPs and enterprise networks.

This was part of my deep dive into **Windows kernel networking** and **network access control (NAC)** systems.

---

## ⚙️ Key Features
- 🔒 **NDIS Filter Driver:** Intercepts and manages packets at the OSI Layer 2 level.
- 🌐 **Built-in DHCP & DNS Servers:** Internal DHCP assigns IPs, and DNS redirects clients to a captive web page.
- 💡 **Integrated Web Server:** Serves the login and status portal directly from a lightweight custom HTTP server.
- 🧮 **User Billing System:** Tracks data usage per session, billing by bytes sent/received.
- 🧠 **Radix Tree Database:** High-performance in-memory structure for user sessions and lookups.
- 🧾 **Encrypted Storage:** User data saved with XOR-based lightweight encryption.
- ⚡ **Cross-Platform Web Interface:** Frontend communicates via a DLL with the kernel driver, making it compatible with most web servers (IIS, Apache, Nginx).

---

## 🏗️ System Architecture

![Architecture Diagram](images/architecture.png)

1. **NDIS Filter Driver** captures packets and checks user authentication status.  
2. **Internal DHCP/DNS** handles pre-authentication requests.  
3. **Web Server Module** communicates with the driver via DeviceIoControl.  
4. **Billing System** records data usage and applies access limits or policies.  
5. **Database Layer** (Radix Tree) manages active sessions efficiently.

---

## 💻 Technologies & Tools Used
| Category | Technologies |
|-----------|---------------|
| **Languages** | C, C++, C#, Visual Basic |
| **Kernel Framework** | Windows Driver Kit (WDK) |
| **Networking** | NDIS, PPPoE, DHCP, DNS |
| **Data Handling** | Custom Radix Tree, XOR Encryption |
| **Frontend** | ASP.NET / Bootstrap |
| **Integration** | DeviceIoControl API |

---

## 🎯 What This Project Demonstrates
- Deep understanding of **network protocol stacks** and **kernel-level programming**.  
- Expertise in **Windows networking**, **NDIS architecture**, and **packet filtering**.  
- Ability to design **end-to-end systems** combining kernel drivers, databases, and web interfaces.  
- Strong focus on **performance, security, and modular design**.

---

## 📸 Screenshots

| Login Page | Session Dashboard |
|-------------|------------------|
| ![Login Page](images/login_page.png) | ![Dashboard](images/dashboard.png) |

---

## 🔐 Note
The actual **source code is private** for security and proprietary reasons.  
This repository is intended as a **technical showcase** of my design, architecture, and engineering approach.

---

## 📬 Contact
**Author:** David Chirikutsi  
**LinkedIn:** [Your LinkedIn Profile]  
**Email:** [your.email@example.com]

---

## 🧠 Related Work
- **PPPoE Server Project** – Implemented authentication and accounting via CHAP.
- **NAT Gateway System** – Custom packet-forwarding module with traffic shaping.
