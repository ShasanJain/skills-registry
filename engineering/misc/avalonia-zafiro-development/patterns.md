---
name: patterns
description: Use when executing patterns protocols within the engineering sector.
---

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core patterns logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

# Common Patterns in Angor/Zafiro

## Refreshable Collections

The `RefreshableCollection` pattern is used to manage lists that can be refreshed via a command, maintaining an internal `SourceCache`/`SourceList` and exposing a `ReadOnlyObservableCollection`.

### Implementation

```csharp
var refresher = RefreshableCollection.Create(
        () => GetDataTask(), 
        model => model.Id)
    .DisposeWith(disposable);

LoadData = refresher.Refresh;
Items = refresher.Items;
```

### Benefits
- **Automatic Loading**: Handles the command execution and results.
- **Efficient Updates**: Uses `EditDiff` internally to update items without clearing the list.
- **UI Friendly**: Exposes `Items` as a `ReadOnlyObservableCollection` suitable for binding.

## Mandatory Validation Pattern

When validating dynamic collections, always use the Zafiro validation extension:

```csharp
this.ValidationRule(
        StagesSource
            .Connect()
            .FilterOnObservable(stage => stage.IsValid)
            .IsEmpty(),
        b => !b,
        _ => "Stages are not valid")
    .DisposeWith(Disposables);
```

## Error Handling Pipeline

Instead of manual `Subscribe`, use `HandleErrorsWith` to pipe errors directly to the user:

```csharp
LoadProjects.HandleErrorsWith(uiServices.NotificationService, "Could not load projects");
```
