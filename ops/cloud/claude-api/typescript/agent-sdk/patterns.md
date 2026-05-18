---
name: patterns
description: Use when executing patterns protocols within the ops sector.
---

# Patterns: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Patterns. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core patterns logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the ops sector.

---

## 📚 Reference Material

# Agent SDK Patterns — TypeScript

## Basic Agent

```typescript
import { query } from "@anthropic-ai/claude-agent-sdk";

async function main() {
  for await (const message of query({
    prompt: "Explain what this repository does",
    options: {
      cwd: "/path/to/project",
      allowedTools: ["Read", "Glob", "Grep"],
    },
  })) {
    if ("result" in message) {
      console.log(message.result);
    }
  }
}

main();
```

---

## Hooks

### After Tool Use Hook

```typescript
import { query, HookCallback } from "@anthropic-ai/claude-agent-sdk";
import { appendFileSync } from "fs";

const logFileChange: HookCallback = async (input) => {
  const filePath = (input as any).tool_input?.file_path ?? "unknown";
  appendFileSync(
    "./audit.log",
    `${new Date().toISOString()}: modified ${filePath}\n`,
  );
  return {};
};

for await (const message of query({
  prompt: "Refactor utils.py to improve readability",
  options: {
    allowedTools: ["Read", "Edit", "Write"],
    permissionMode: "acceptEdits",
    hooks: {
      PostToolUse: [{ matcher: "Edit|Write", hooks: [logFileChange] }],
    },
  },
})) {
  if ("result" in message) console.log(message.result);
}
```

---

## Subagents

```typescript
import { query } from "@anthropic-ai/claude-agent-sdk";

for await (const message of query({
  prompt: "Use the code-reviewer agent to review this codebase",
  options: {
    allowedTools: ["Read", "Glob", "Grep", "Agent"],
    agents: {
      "code-reviewer": {
        description: "Expert code reviewer for quality and security reviews.",
        prompt: "Analyze code quality and suggest improvements.",
        tools: ["Read", "Glob", "Grep"],
      },
    },
  },
})) {
  if ("result" in message) console.log(message.result);
}
```

---

## MCP Server Integration

### Browser Automation (Playwright)

```typescript
for await (const message of query({
  prompt: "Open example.com and describe what you see",
  options: {
    mcpServers: {
      playwright: { command: "npx", args: ["@playwright/mcp@latest"] },
    },
  },
})) {
  if ("result" in message) console.log(message.result);
}
```

---

## Session Resumption

```typescript
import { query } from "@anthropic-ai/claude-agent-sdk";

let sessionId: string | undefined;

// First query: capture the session ID
for await (const message of query({
  prompt: "Read the authentication module",
  options: { allowedTools: ["Read", "Glob"] },
})) {
  if (message.type === "system" && message.subtype === "init") {
    sessionId = message.session_id;
  }
}

// Resume with full context from the first query
for await (const message of query({
  prompt: "Now find all places that call it",
  options: { resume: sessionId },
})) {
  if ("result" in message) console.log(message.result);
}
```

---

## Session History

```typescript
import { listSessions, getSessionMessages, getSessionInfo } from "@anthropic-ai/claude-agent-sdk";

async function main() {
  // List past sessions (supports pagination via limit/offset)
  const sessions = await listSessions();
  for (const session of sessions) {
    console.log(`Session ${session.sessionId} in ${session.cwd} (tag: ${session.tag})`);
  }

  // Get metadata for a single session
  if (sessions.length > 0) {
    const info = await getSessionInfo(sessions[0].sessionId);
    console.log(`Created: ${info.createdAt}, Tag: ${info.tag}`);
  }

  // Retrieve messages from the most recent session
  if (sessions.length > 0) {
    const messages = await getSessionMessages(sessions[0].sessionId, { limit: 50 });
    for (const msg of messages) {
      console.log(msg);
    }
  }
}

main();
```

---

## Session Mutations

```typescript
import { renameSession, tagSession, forkSession } from "@anthropic-ai/claude-agent-sdk";

async function main() {
  const sessionId = "your-session-id";

  // Rename a session
  await renameSession(sessionId, "Refactoring auth module");

  // Tag a session for filtering
  await tagSession(sessionId, "experiment-v2");

  // Clear a tag
  await tagSession(sessionId, null);

  // Fork a conversation to branch from a point
  const { sessionId: forkedId } = await forkSession(sessionId);
  console.log(`Forked session: ${forkedId}`);
}

main();
```

---

## Custom System Prompt

```typescript
import { query } from "@anthropic-ai/claude-agent-sdk";

for await (const message of query({
  prompt: "Review this code",
  options: {
    allowedTools: ["Read", "Glob", "Grep"],
    systemPrompt: `You are a senior code reviewer focused on:
1. Security vulnerabilities
2. Performance issues
3. Code maintainability

Always provide specific line numbers and suggestions for improvement.`,
  },
})) {
  if ("result" in message) console.log(message.result);
}
```
