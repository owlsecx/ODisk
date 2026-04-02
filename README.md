# 💾 ODisk

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-informational?style=flat-square&logo=linux&logoColor=white&color=0a0c10"/>
  <img src="https://img.shields.io/badge/Category-OForensics%20%2F%20Disk%20Forensics-cyan?style=flat-square"/>
  <img src="https://img.shields.io/badge/Dependencies-None%20(Standalone)-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-Proprietary-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-v1.5-cyan?style=flat-square"/>
</p>

> **ODisk** is a low-level disk forensic tool. It supports direct disk access, partition analysis (MBR/GPT), hex dumping, multi-algorithm hashing, custom sector reading, and forensic image (.dd/.img) support.

**Requires root privileges** — designed for authorized forensic analysis only.

---

## 📌 Overview

ODisk provides safe, controlled access to physical disks and forensic images for investigators. It includes built-in warnings for write protection and logs all actions for audit purposes.

---

## 🖥️ Modules

| # | Module                    | Description |
|---|---------------------------|-------------|
| **[1]** | **List Disks**            | Show filtered physical disks (lsblk) |
| **[2]** | **Sector Hex Dump**       | Read and display first sectors in hex + ASCII |
| **[3]** | **Disk Integrity**        | Calculate MD5, SHA1, SHA256 hashes |
| **[4]** | **Custom Sector Read**    | Read any offset + size (supports .dd/.img) |
| **[5]** | **Reload Config**         | Refresh settings from odisk_config.yaml |

---

## 📊 Key Features

- **Physical Disk Detection** — Filtered list of real disks (excludes loop/ram)
- **MBR/GPT Analysis** — Automatic detection of classic MBR and GPT protective headers
- **Hex Dump Viewer** — Detailed hex + ASCII output with offset display
- **Forensic Hashing** — Multiple algorithms (SHA256, MD5, SHA1) with progress bar
- **Custom Sector Reading** — Read any byte offset and length from disks or images
- **Forensic Safety** — Clear warnings before any disk operation + audit logging
- **.dd / .img Support** — Works directly on forensic disk images
- **Persistent Audit Log** — All actions logged to `odisk_audit.log`

---

## ⚙️ Requirements

- **Linux** (recommended)
- **Root privileges** (required for direct disk access)
- **No additional Python dependencies**

---

## 🚀 Usage

```bash
sudo ./ODisk

📁 Output

Live Hex Dumps — Color-coded hex + ASCII with absolute offsets
Hash Reports — MD5, SHA1, SHA256 values
MBR/GPT Analysis — Partition table detection
Audit Log — odisk_audit.log records all operations
Saved Dumps — Optional hex dumps saved to dumps/ folder


📦 Part of OwlSec Toolkit
This tool is part of the OwlSec suite — a collection of 300+ security and privacy tools.
🔗 owlsec.org

©️ License
Proprietary — © Khaled S. Haddad
Tools are distributed as pre-built executables. Source code is proprietary.

AUTHORISED FORENSIC DISK ANALYSIS USE ONLY
Always use hardware write-blockers when working with original evidence.
