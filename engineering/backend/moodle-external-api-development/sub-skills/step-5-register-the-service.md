---
name: step-5-register-the-service
description: Use when executing step 5 register the service protocols within the engineering sector.
---

# Step 5 Register The Service: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Step 5 Register The Service. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Step 5: Register the Service

**Location**: `/local/yourplugin/db/services.php`

```php
<?php
defined('MOODLE_INTERNAL') || die();

$functions = [
    'local_yourplugin_your_api_name' => [
        'classname'   => 'local_yourplugin\external\your_api_name',
        'methodname'  => 'execute',
        'classpath'   => 'local/yourplugin/classes/external/your_api_name.php',
        'description' => 'Brief description of what this API does',
        'type'        => 'read',  // or 'write'
        'ajax'        => true,
        'capabilities'=> 'moodle/course:view', // comma-separated if multiple
        'services'    => [MOODLE_OFFICIAL_MOBILE_SERVICE] // Optional
    ],
];

$services = [
    'Your Plugin Web Service' => [
        'functions' => [
            'local_yourplugin_your_api_name'
        ],
        'restrictedusers' => 0,
        'enabled' => 1
    ]
];
```

**Service Registration Keys**:
- `classname` - Full namespaced class name
- `methodname` - Always 'execute'
- `type` - 'read' (SELECT) or 'write' (INSERT/UPDATE/DELETE)
- `ajax` - Set true for AJAX/REST access
- `capabilities` - Required Moodle capabilities
- `services` - Optional service bundles