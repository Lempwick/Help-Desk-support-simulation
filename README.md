# Help Desk Support Simulation (Home Lab)

A hands-on project simulating Tier 1 IT support using virtual machines and the osTicket ticketing system. This demonstrates troubleshooting ability, communication skills, and help desk process knowledge.

## Project Structure

**Lab Environment:**
Ubuntu (osTicket server), Kali Linux, Windows 11 — running in VMware on macOS M3

**Ticketing System:**
osTicket — open-source support ticket platform

## Setup Steps

### 1. Virtual Lab Setup

- Installed VMware
- Created and ran:
  - Ubuntu VM for osTicket
  - Kali Linux for diagnostics and testing
  - Windows 11 for client simulation
  <img width="364" height="432" alt="Screenshot 2025-07-31 at 20 19 44" src="https://github.com/user-attachments/assets/99c2e2fd-b05f-4bea-ae26-5122d7477bc7" />


### 2. Apache + PHP + MySQL Setup

- Installed LAMP stack on Ubuntu:
  - Apache2
  - PHP
  - MySQL
  - Required PHP modules
- Verified services are running
<img width="811" height="341" alt="Screenshot 2025-08-01 at 09 25 42" src="https://github.com/user-attachments/assets/beccbac7-3501-4273-85c0-132d549d456a" />
<img width="819" height="356" alt="Screenshot 2025-08-01 at 09 25 34" src="https://github.com/user-attachments/assets/3f55b8c3-08f3-4197-9f48-a78c8252a11a" />

### 3. osTicket Installation

- Downloaded and extracted osTicket to `/var/www/html/osticket`
- Set file permissions
- Accessed installer via `http://localhost/osticket/setup`
- Completed setup:
  - Used MySQL credentials
  - Created admin user
- Deleted setup directory for security
  <img width="1405" height="796" alt="Screenshot 2025-08-01 at 09 52 32" src="https://github.com/user-attachments/assets/be460313-bc23-4cbf-a168-214bceb7a824" />
### 4. First Simulated Ticket — Add Local User via `lusrmgr.msc`

After completing the osTicket installation, I created my first ticket simulating a real-world Tier 1 help desk scenario.

#### 🧾 Ticket: Add Local User via `lusrmgr.msc`

**Ticket ID:** TICKET-001  
**Issue Summary:**  
Create a new local user account on a Windows 11 system.

**Steps Taken:**  
1. Opened the Run dialog using `Win + R`.  
2. Entered `lusrmgr.msc` to launch Local Users and Groups Manager.  
3. Navigated to `Users` → Right-clicked → `New User...`.  
4. Filled in details:  
   - Username: `diego.intern`  
   - Full Name: `Diego Rivera`  
   - Temporary Password: `TempP@ss123`  
5. Deselected "User must change password at next logon" for test purposes.  
6. Clicked “Create” and confirmed user `diego.intern` appeared.

**Resolution:**  
User account successfully added and verified on the Windows system.

<img width="987" height="757" alt="Screenshot 2025-08-01 at 16 51 01" src="https://github.com/user-attachments/assets/71ae6baf-57e6-456f-a46a-f35205e132df" />

<img width="968" height="719" alt="Screenshot 2025-08-01 at 19 26 12" src="https://github.com/user-attachments/assets/5b7283ba-231d-49a9-8689-6f32948412dc" />


**Lessons Learned:**  
This method is ideal for Windows Pro editions. For Home editions, you can use `net user` via CMD.

### 5. Simulated Ticket — Computer Won’t Power On

**Ticket ID:** TICKET-002  
**Issue Summary:**  
User reports their desktop PC will not power on when pressing the power button.

**Steps Taken:**  
- Confirmed outlet is working by testing another device  
- Checked power cable — was loosely connected to PSU  
- Reseated cable and system powered on  
- No signs of hardware failure

**Resolution:**  
Reconnected loose power cable. System powered on successfully.

<img width="1029" height="798" alt="Screenshot 2025-08-01 at 16 42 32" src="https://github.com/user-attachments/assets/d14e4bef-6c16-4ba9-9cda-9a6bb2b43f88" />

**Lessons Learned:**  
Start with simple, non-invasive checks — loose cables are a common issue. Document all steps, even if the solution is quick.

### 6. Simulated Ticket — Add User to Ubuntu Server

**Ticket ID:** TICKET-006  
**Issue Summary:**  
User requested the creation of a new standard Linux account (`sierra.contractor`) on the Ubuntu server for SFTP access. No administrative privileges required.

**Steps Taken:**  
- SSH’d into Ubuntu server as admin  
- Verified the user account didn’t already exist: `id sierra.contractor`  
- Created the user with: `sudo adduser sierra.contractor`  
  - Set temporary password  
  - Filled optional fields (Name, Room, etc.)  
- Verified account presence: `getent passwd sierra.contractor`  
- Checked shell and home directory: `grep sierra.contractor /etc/passwd`  
- Confirmed no sudo privileges: `sudo -l -U sierra.contractor`

**Resolution:**  
New user `sierra.contractor` created successfully with standard privileges and no sudo access.

<img width="693" height="840" alt="Screenshot 2025-08-02 at 04 16 40" src="https://github.com/user-attachments/assets/3ad32550-e8f4-4864-8424-f526f91e2a51" />

<img width="780" height="760" alt="Screenshot 2025-08-01 at 16 57 35" src="https://github.com/user-attachments/assets/c4b50513-88cc-44b2-8ea2-d1ca61e8da04" />

**Lessons Learned:**  
Always confirm account creation with system commands. Validate access rights to avoid privilege escalation. A secure SFTP user setup is critical for access-limited workflows.

**Project Summary**

## 🧠 What I Learned

Through this hands-on lab, I developed real-world Tier 1 IT support skills, including:

- **Technical Troubleshooting**  
  Learned how to methodically diagnose and resolve hardware, software, and access issues across Windows and Linux environments.

- **Documentation & Ticketing**  
  Practiced structured issue documentation and professional communication using a real ticketing platform (osTicket), simulating workplace expectations.

- **System Administration Basics**  
  Created and managed local user accounts, verified access permissions, and used commands like `adduser`, `getent`, and `lusrmgr.msc` to simulate real admin tasks.

- **Environment Setup & Tooling**  
  Installed and configured Apache, MySQL, PHP, and osTicket in a LAMP stack — reinforcing package management and system configuration.

- **Soft Skills**  
  Wrote user-friendly responses, followed up on issues, and practiced concise technical writing for clarity and empathy.

This project strengthened my confidence in supporting real users and prepared me for entry-level IT roles with practical, demonstrable skills.

Copy and paste this directly into your README.md — let me know if you want it appended to your full doc or want a downloadable version! 💾📄
