---
name: navigation_sections
description: Use when executing navigation_sections protocols within the engineering sector.
---

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core navigation_sections logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

# Navigation & Sections

Zafiro provides powerful abstractions for managing application-wide navigation and modular UI sections.

## Navigation with INavigator

The `INavigator` interface is used to switch between different views or viewmodels.

```csharp
public class MyViewModel(INavigator navigator)
{
    public async Task GoToDetails()
    {
        await navigator.Navigate(() => new DetailsViewModel());
    }
}
```

## UI Sections

Sections are modular parts of the UI (like tabs or sidebar items) that can be automatically registered.

### The [Section] Attribute

ViewModels intended to be sections should be marked with the `[Section]` attribute.

```csharp
[Section("Wallet", icon: "fa-wallet")]
public class WalletSectionViewModel : IWalletSectionViewModel
{
    // ...
}
```

### Automatic Registration

In the `CompositionRoot`, sections can be automatically registered:

```csharp
services.AddAnnotatedSections(logger);
services.AddSectionsFromAttributes(logger);
```

### Switching Sections

You can switch the current active section via the `IShellViewModel`:

```csharp
shellViewModel.SetSection("Browse");
```

> [!IMPORTANT]
> The `icon` parameter in the `[Section]` attribute supports FontAwesome icons (e.g., `fa-home`) when configured with `ProjektankerIconControlProvider`.
