---
name: viewmodels
description: Use when executing viewmodels protocols within the engineering sector.
---

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core viewmodels logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

# ViewModels & Commands

In a Zafiro-based application, ViewModels should be functional, reactive, and resilient.

## Reactive ViewModels

Use `ReactiveObject` as the base class. Properties should be defined using the `[Reactive]` attribute (from ReactiveUI.SourceGenerators) for brevity.

```csharp
public partial class MyViewModel : ReactiveObject
{
    [Reactive] private string name;
    [Reactive] private bool isBusy;
}
```

### Observation and Transformation

Use `WhenAnyValue` to react to property changes:

```csharp
this.WhenAnyValue(x => x.Name)
    .Select(name => !string.IsNullOrEmpty(name))
    .ToPropertyEx(this, x => x.CanSubmit);
```

## Enhanced Commands

Zafiro uses `IEnhancedCommand`, which extends `ICommand` and `IReactiveCommand` with additional metadata like `Name` and `Text`.

### Creating a Command

Use `ReactiveCommand.Create` or `ReactiveCommand.CreateFromTask` and then `Enhance()` it.

```csharp
public IEnhancedCommand Submit { get; }

public MyViewModel()
{
    Submit = ReactiveCommand.CreateFromTask(OnSubmit, canSubmit)
        .Enhance(text: "Submit Data", name: "SubmitCommand");
}
```

### Error Handling

Use `HandleErrorsWith` to automatically channel command errors to the `NotificationService`.

```csharp
Submit.HandleErrorsWith(uiServices.NotificationService, "Submission Failed")
    .DisposeWith(disposable);
```

## Disposables

Always use a `CompositeDisposable` to manage subscriptions and command lifetimes.

```csharp
public class MyViewModel : ReactiveObject, IDisposable
{
    private readonly CompositeDisposable disposables = new();

    public void Dispose() => disposables.Dispose();
}
```

> [!TIP]
> Use `.DisposeWith(disposables)` on any observable subscription or command to ensure proper cleanup.
