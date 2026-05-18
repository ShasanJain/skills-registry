---
name: 4-configure-smb-service-port-445
description: Use when executing 4 configure smb service port 445 protocols within the engineering sector.
---

# 4 Configure Smb Service Port 445: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing 4 Configure Smb Service Port 445. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core 4 configure smb service port 445 logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

# 4. Configure SMB Service (Port 445)

Set up SMB file shares for enumeration:

**Windows SMB Share:**
1. Create folder to share
2. Right-click → Properties → Sharing → Advanced Sharing
3. Enable sharing and set permissions
4. Configure NTFS permissions

**Linux Samba Setup:**

```bash
# Install Samba
sudo apt install samba

# Create share directory
sudo mkdir -p /srv/samba/share
sudo chmod 777 /srv/samba/share

# Configure Samba
sudo nano /etc/samba/smb.conf

# Add share:
# [public]
#    path = /srv/samba/share
#    browsable = yes
#    guest ok = yes
#    read only = no

# Restart service
sudo systemctl restart smbd
```

**SMB Enumeration Commands:**

```bash
# List shares anonymously
smbclient -L //192.168.1.1 -N

# Connect to share
smbclient //192.168.1.1/share -N

# Enumerate with smbmap
smbmap -H 192.168.1.1

# Full enumeration
enum4linux -a 192.168.1.1

# Check for vulnerabilities
nmap --script smb-vuln* 192.168.1.1
```