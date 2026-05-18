---
name: phase-10-prevention-measures
description: Use when executing phase 10 prevention measures protocols within the engineering sector.
---

# Phase 10 Prevention Measures: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Phase 10 Prevention Measures. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core phase 10 prevention measures logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

# Phase 10: Prevention Measures

Secure coding practices:

```php
// PHP: Use basename() to strip paths
$filename = basename($_GET['file']);
$path = "/var/www/files/" . $filename;

// PHP: Validate against whitelist
$allowed = ['report.pdf', 'manual.pdf', 'guide.pdf'];
if (in_array($_GET['file'], $allowed)) {
    include("/var/www/files/" . $_GET['file']);
}

// PHP: Canonicalize and verify base path
$base = "/var/www/files/";
$realBase = realpath($base);
$userPath = $base . $_GET['file'];
$realUserPath = realpath($userPath);

if ($realUserPath && strpos($realUserPath, $realBase) === 0) {
    include($realUserPath);
}
```

```python
# Python: Use os.path.realpath() and validate
import os

def safe_file_access(base_dir, filename):
    # Resolve to absolute path
    base = os.path.realpath(base_dir)
    file_path = os.path.realpath(os.path.join(base, filename))
    
    # Verify file is within base directory
    if file_path.startswith(base):
        return open(file_path, 'r').read()
    else:
        raise Exception("Access denied")
```

## Quick Reference