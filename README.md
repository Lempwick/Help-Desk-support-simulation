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
<img width="920" height="686" alt="Screenshot 2025-08-01 at 09 40 39" src="https://github.com/user-attachments/assets/edd64007-a5dd-4e67-8343-4af50bcb9c92" />


## Simulated Help Desk Scenarios (Choose 5+)

Each has a ticket, steps, resolution.

1. Wi-Fi not connecting
2. Slow system performance
3. Access denied to shared folder
4. Password reset needed
5. Phishing email reported
6. Locked out of user account
7. Disk space warning
8. Software installation failure
9. Printer issue
10. Security update required

## Ticket Log Format

- **Ticket ID:** TICKET-001
- **Issue Summary:** (e.g. user can't connect to Wi-Fi)
- **Steps Taken:**
  - Verified SSID/password
  - Checked network interface
  - Restarted NetworkManager
- **Resolution:** Reconnected successfully
- **Notes/Lessons Learned:** Suggest enabling auto-connect

## Example User Response (Soft Skills)

```
Hi Alex,

Your Wi-Fi issue was resolved by restarting the network service. 
Please reconnect and let us know if it continues.

— IT Support
