---
name: themes
description: Use when executing themes protocols within the engineering sector.
---

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core themes logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

# Theme Organization and Shared Styles

Efficient theme organization is key to avoiding redundant XAML and ensuring visual consistency.

## 🏗️ Structure

Follow the pattern from Angor:

1.  **Colors & Brushes**: Define in a dedicated `Colors.axaml`. Use `DynamicResource` to support theme switching.
2.  **Styles**: Group styles by category (e.g., `Buttons.axaml`, `Containers.axaml`, `Typography.axaml`).
3.  **App-wide Theme**: Aggregate all styles in a main `Theme.axaml`.

## 🎨 Avoiding Redundancy

Instead of setting properties directly on elements:

```xml
<!-- ❌ BAD: Redundant properties -->
<HeaderedContainer CornerRadius="10" BorderThickness="1" BorderBrush="Blue" Background="LightBlue" />
<HeaderedContainer CornerRadius="10" BorderThickness="1" BorderBrush="Blue" Background="LightBlue" />

<!-- ✅ GOOD: Use Classes and Styles -->
<HeaderedContainer Classes="BlueSection" />
<HeaderedContainer Classes="BlueSection" />
```

Define the style in a shared `axaml` file:

```xml
<Style Selector="HeaderedContainer.BlueSection">
    <Setter Property="CornerRadius" Value="10" />
    <Setter Property="BorderThickness" Value="1" />
    <Setter Property="BorderBrush" Value="{DynamicResource Accent}" />
    <Setter Property="Background" Value="{DynamicResource SurfaceSubtle}" />
</Style>
```

## 🧩 Shared Icons and Resources

Centralize icon definitions and other shared resources in `Icons.axaml` and include them in the `MergedDictionaries` of your theme or `App.axaml`.

```xml
<Application.Resources>
    <ResourceDictionary>
        <ResourceDictionary.MergedDictionaries>
            <MergeResourceInclude Source="UI/Themes/Styles/Containers.axaml" />
            <MergeResourceInclude Source="UI/Shared/Resources/Icons.axaml" />
        </ResourceDictionary.MergedDictionaries>
    </ResourceDictionary>
</Application.Resources>
```
