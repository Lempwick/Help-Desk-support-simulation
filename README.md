# Help-Desk-support-simulation
A hands-on lab simulating Tier 1 IT support using virtual machines and the osTicket ticketing system. This project demonstrates my ability to troubleshoot real-world issues, communicate professionally, and manage help desk operations using industry-standard tools.
# 🖥️ Help Desk Support Simulation (Home Lab)

A hands-on lab simulating Tier 1 IT support using virtual machines and the osTicket ticketing system. This project demonstrates my ability to troubleshoot real-world issues, communicate professionally, and manage help desk operations using industry-standard tools.

---

## 📁 Project Structure

- **Lab Environment**  
  Ubuntu (osTicket server), Kali Linux, Windows 11 — all running on VMware on macOS M3.

- **Ticketing System**  
  osTicket — open-source support ticket system used to simulate real help desk workflows.

---

## 🔧 Setup Steps

### 1. 🖥️ Virtual Lab Setup

- Installed and configured VMware
- Created and ran VMs for:
  - Ubuntu (osTicket host)
  - Kali Linux (security testing)
  - Windows 11 (user simulation)

> 📸 *Screenshot Placeholder: VM list running in VMware*

---

### 2. 🛠️ Apache + PHP + MySQL Setup

```bash
sudo apt update
sudo apt install apache2 php mysql-server php-mysql php-imap php-apcu php-intl php-mbstring php-gd php-xml php-cli php-common unzip
