---
name: bolt-app-foundation-pattern
description: Use when executing bolt app foundation pattern protocols within the design sector.
---

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core bolt app foundation pattern logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the design sector.

---

## 📚 Reference Material

# Bolt App Foundation Pattern

The Bolt framework is Slack's recommended approach for building apps.
It handles authentication, event routing, request verification, and
HTTP request processing so you can focus on app logic.

Key benefits:
- Event handling in a few lines of code
- Security checks and payload validation built-in
- Organized, consistent patterns
- Works for experiments and production

Available in: Python, JavaScript (Node.js), Java


**When to use**: ['Starting any new Slack app', 'Migrating from legacy Slack APIs', 'Building production Slack integrations']

```python
# Python Bolt App
from slack_bolt import App
from slack_bolt.adapter.socket_mode import SocketModeHandler
import os

# Initialize with tokens from environment
app = App(
    token=os.environ["SLACK_BOT_TOKEN"],
    signing_secret=os.environ["SLACK_SIGNING_SECRET"]
)

# Handle messages containing "hello"
@app.message("hello")
def handle_hello(message, say):
    """Respond to messages containing 'hello'."""
    user = message["user"]
    say(f"Hey there <@{user}>!")

# Handle slash command
@app.command("/ticket")
def handle_ticket_command(ack, body, client):
    """Handle /ticket slash command."""
    # Acknowledge immediately (within 3 seconds)
    ack()

    # Open a modal for ticket creation
    client.views_open(
        trigger_id=body["trigger_id"],
        view={
            "type": "modal",
            "callback_id": "ticket_modal",
            "title": {"type": "plain_text", "text": "Create Ticket"},
            "submit": {"type": "plain_text", "text": "Submit"},
            "blocks": [
                {
                    "type": "input",
                    "block_id": "title_block",
                    "element": {
                        "type": "plain_text_input",
                        "action_id": "title_input"
                    },
                    "label": {"type": "plain_text", "text": "Title"}
                },
                {
                    "type": "input",
                    "block_id": "desc_block",
                    "element": {
                        "type": "plain_text_input",
                        "multiline": True,
                        "action_id": "desc_input"
                    },
                    "label": {"type": "plain_text", "text": "Description"}
                },
                {
                    "type": "input",
                    "block_id": "priority_block",
                    "element": {
                        "type": "static_select",
                        "action_id": "priority_select",
   
```