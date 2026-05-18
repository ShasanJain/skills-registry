---
name: 5-transaction-deadlocks
description: Use when executing 5 transaction deadlocks protocols within the engineering sector.
---

# 5 Transaction Deadlocks: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing 5 Transaction Deadlocks. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# 5. Transaction Deadlocks

**Solution**:
- Keep transactions short
- Always commit or rollback in finally blocks
- Avoid nested transactions

## Debugging Checklist

- [ ] Check Moodle debug mode: **Site administration > Development > Debugging**
- [ ] Review web services logs: **Site administration > Reports > Logs**
- [ ] Check custom log files in `$CFG->dataroot/local_yourplugin/`
- [ ] Verify database queries using `$DB->set_debug(true)`
- [ ] Test with admin user to rule out permission issues
- [ ] Clear browser cache and Moodle caches
- [ ] Check PHP error logs on server

## Plugin Structure Checklist

```
local/yourplugin/
├── version.php                 # Plugin version and metadata
├── db/
│   ├── services.php           # External service definitions
│   └── access.php             # Capability definitions (optional)
├── classes/
│   └── external/
│       ├── your_api_name.php  # External API implementation
│       └── another_api.php    # Additional APIs
├── lang/
│   └── en/
│       └── local_yourplugin.php  # Language strings
└── tests/
    └── external_test.php      # Unit tests (optional but recommended)
```

## Examples from Real Implementation