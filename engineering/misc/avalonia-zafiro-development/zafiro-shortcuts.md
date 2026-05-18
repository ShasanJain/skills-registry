---
name: zafiro-shortcuts
description: Use when executing zafiro shortcuts protocols within the engineering sector.
---

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core zafiro shortcuts logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

# Zafiro Reactive Shortcuts

Use these Zafiro extension methods to replace standard, more verbose Reactive and DynamicData patterns.

## General Observable Helpers

| Standard Pattern | Zafiro Shortcut |
| :--- | :--- |
| `Replay(1).RefCount()` | `ReplayLastActive()` |
| `Select(_ => Unit.Default)` | `ToSignal()` |
| `Select(b => !b)` | `Not()` |
| `Where(b => b).ToSignal()` | `Trues()` |
| `Where(b => !b).ToSignal()` | `Falses()` |
| `Select(x => x is null)` | `Null()` |
| `Select(x => x is not null)` | `NotNull()` |
| `Select(string.IsNullOrWhiteSpace)` | `NullOrWhitespace()` |
| `Select(s => !string.IsNullOrWhiteSpace(s))` | `NotNullOrEmpty()` |

## Result & Maybe Extensions

| Standard Pattern | Zafiro Shortcut |
| :--- | :--- |
| `Where(r => r.IsSuccess).Select(r => r.Value)` | `Successes()` |
| `Where(r => r.IsFailure).Select(r => r.Error)` | `Failures()` |
| `Where(m => m.HasValue).Select(m => m.Value)` | `Values()` |
| `Where(m => !m.HasValue).ToSignal()` | `Empties()` |

## Lifecycle Management

| Description | Method |
| :--- | :--- |
| Dispose previous item before emitting new one | `DisposePrevious()` |
| Manage lifecycle within a disposable | `DisposeWith(disposables)` |

## Command & Interaction

| Description | Method |
| :--- | :--- |
| Add metadata/text to a ReactiveCommand | `Enhance(text, name)` |
| Automatically show errors in UI | `HandleErrorsWith(notificationService)` |

> [!TIP]
> Always check `Zafiro.Reactive.ObservableMixin` and `Zafiro.CSharpFunctionalExtensions.ObservableExtensions` before writing custom Rx logic.
