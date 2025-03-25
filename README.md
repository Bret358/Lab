# 🧪 Home Lab Project: Active Directory with Splunk SIEM and Offensive Simulation

Hey everyone, I’ve been working on a home lab to get more hands-on experience with enterprise-level systems, SIEM tools, and security workflows. I set up a Windows-based Active Directory environment with log forwarding to Splunk, and ran some basic adversary simulations using Atomic Red Team. I’m still expanding the lab and have a few things planned next like pen testing with Kali, building custom dashboards, and hardening the environment with STIGs.

---

## 🖥️ Lab Overview

This environment is running inside Oracle VirtualBox. Right now it includes:

- A Windows Server 2022 Domain Controller
- A domain-joined Windows 10 Pro client
- A Splunk server on Ubuntu for centralized log collection
- A Kali Linux box set up for future penetration testing

So far I’ve installed Sysmon and Splunk Universal Forwarder on both Windows machines and confirmed logs are flowing into Splunk. I also installed and ran Atomic Red Team to simulate common attack techniques.

---

## 🔧 Tech Stack

- **Virtualization**: Oracle VirtualBox
- **Directory Services**: Active Directory (Windows Server 2022)
- **SIEM**: Splunk Enterprise (on Ubuntu)
- **Endpoint Logging**: Sysmon + Splunk Universal Forwarder
- **Attack Simulation**: Atomic Red Team
- **Attacker Machine**: Kali Linux (configured, pen testing planned)

---

## 🗺️ Network Diagram

Here's a simple diagram showing the current setup:

![Network Diagram](images/network-diagram.png)

---

## ⚙️ What’s Been Configured

### Domain Controller (Windows Server 2022)
- Promoted to Domain Controller (`MyLab.local`)
- Set up DNS and AD services
- Created OUs and security groups (e.g. HR, IT)
- Installed Sysmon and Splunk Universal Forwarder

### Windows 10 Client
- Joined to the domain
- Installed Sysmon and Splunk Universal Forwarder
- Installed and ran Atomic Red Team simulations

### Splunk Server (Ubuntu)
- Installed Splunk Enterprise
- Configured to receive logs from both Windows hosts
- Verified log ingestion from Sysmon and Windows Event Logs

### Kali Linux
- Set up and connected to the internal network
- Ready for use in future pen testing (Nmap, Hydra, Metasploit)

---

## 🧠 Skills Practiced

- Active Directory deployment and management
- Domain joining and DNS configuration
- Security group creation and user management
- Log collection, forwarding, and ingestion with Splunk
- Basic attack simulation with Atomic Red Team
- Network and system architecture design

---

## 📈 Next Steps

- Perform manual pen testing from Kali (targeting AD)
- Build custom dashboards in Splunk to visualize key events
- Apply Group Policies (GPOs) to strengthen endpoint security
- Harden the environment using DISA STIGs
- Run SCAP compliance scans and document findings
- Expand alerting and detection logic in Splunk

---

## 💭 Final Thoughts

Building this lab has been a great learning experience. Getting everything running from the ground up helped me understand how these systems interact in the real world. Seeing logs flow into Splunk and testing detection with Atomic Red Team brought it all to life. I’m excited to keep growing the lab and push it further in the next few phases.

Feel free to connect if you want to chat about this setup or share ideas.
