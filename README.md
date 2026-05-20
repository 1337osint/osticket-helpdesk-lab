# osTicket Helpdesk Lab

## Overview
Deployed and administered a fully functional helpdesk ticketing system from scratch using osTicket on Ubuntu Server 24.04. Configured the full environment including web server stack, database, departments, SLA plans, agents, and worked tickets through their complete lifecycle.

## Environment
- Host OS: Windows 11
- Hypervisor: VirtualBox
- Server OS: Ubuntu Server 24.04 LTS
- Web Server: Apache2
- Database: MySQL
- Language: PHP 8.3
- Ticketing System: osTicket 1.18

## Network Architecture
- pfSense VM: LAN gateway at 192.168.1.1
- osTicket Server: 192.168.1.104 (internal) / 192.168.18.3 (host-only)
- Access: Staff Control Panel via browser from host machine

## What I Built

### Server Infrastructure
- Deployed Ubuntu Server 24.04 LTS in VirtualBox
- Installed and configured Apache2, MySQL, and PHP 8.3
- Secured MySQL with mysql_secure_installation
- Created dedicated osTicket database and user with proper permissions
- Deployed osTicket 1.18 and completed full web-based installation

### Helpdesk Configuration
- Created 3 departments: IT Support, Networking, Security
- Created 2 agents: John Smith (IT Support), Jane Doe (Networking)
- Configured 3 SLA plans:
  - SEV-A: 1 hour response, 24/7 schedule (critical)
  - SEV-B: 4 hour response, 24/7 schedule (moderate)
  - SEV-C: 8 hour response, business hours (low)
- Created 4 Help Topics mapped to departments and SLA plans:
  - Password Reset → IT Support → SEV-C
  - Account Lockout → IT Support → SEV-B
  - Network Connectivity Issue → Networking → SEV-B
  - Security Incident → Security → SEV-A

### Ticket Lifecycle Demonstrated
| Ticket | User | Issue | SLA | Resolution |
|--------|------|-------|-----|------------|
| #167976 | John Smith | Password Reset | SEV-C | Password reset and temporary credentials issued |
| #684455 | Jane Doe | Network Connectivity Issue | SEV-B | DNS flush and adapter troubleshooting steps provided |
| #502000 | Bob Wilson | Suspicious Login Activity | SEV-A | Account locked, security investigation initiated, user notified |

## Skills Demonstrated
- Linux server administration (Ubuntu 24.04)
- Apache, MySQL, PHP (LAMP stack) deployment and configuration
- Helpdesk administration and ticketing system management
- SLA configuration and priority-based ticket routing
- Department and agent management
- Full ticket lifecycle: creation, assignment, response, resolution
- Internal note documentation for investigation tracking
- Web-based application deployment and troubleshooting

## Screenshots
### Prerequisites Check — All Green
![Prerequisites](osTicket%20Prerequisites.png)

### Installation Success
![Installation](osTicket%20Installation%20Evidence.png)

### Staff Login Portal
![Login](osTicket%20Login%20Page%2C%20My%20Helpdesk%20Lab.png)

### Ticket Queue
![Queue](Dashboard%20Ticket%20Queue.png)

### Password Reset Ticket (SEV-C)
![Password Reset](Ticket%20-%20Password%20Reset%2C%20John%20Smith.png)

### Network Connectivity Ticket (SEV-B)
![Network](Ticket%20-%20Network%20Connectivity%20Issue%20Resolved.png)

### Security Incident Ticket (SEV-A)
![Security](Ticket%20-%20Security%20Incident%2C%20Bob%20Wilson%2C%20SEV-A.png)

### Closed Tickets Overview
![Closed](Closed%20Tickets%20Overview.png)
