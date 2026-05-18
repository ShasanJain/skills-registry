---
name: wwds-variables--using
description: Use when executing wwds variables  using protocols within the production sector.
---

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core wwds variables  using logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the production sector.

---

## 📚 Reference Material

# Working with design systems: Using Variables

When using Figma variables, you need to start by understanding the state of the source and the state of Figma.

For the source, you need to know the breadth of variables code representation. CSS, JSON, theme providers etc will all be able to indicate what the user will expect you to cover in Figma. Some beginner users might not even know what does and doesn't exist in Figma, and if you cant discover that on your own, you will need their help making the right decision.

For Figma, you need to know what collections exist, what their modes are, and what values and names and code syntaxes are in them. This will help you make sure you are using the right things. For properties that "should" have variables but don't, you likely will need to ask the user what to do. Your understanding of Figma's current state should come first.

You can use code syntax and your understanding of the environment you are expected to be referencing to know which variable in Figma to use. You can also use Figma's variable scopes as indicators if they are specified. It is best to audit those up front.

When using variables you should also be aware of mode mismatches, the default mode in Figma may not be the mode referenced by the user in their expectations. Similarly, many collections may refer to values, but the most specific collection is what you should be using. For example, a semantic collection that aliases a primitive collection, the semantic collection would be what you reference. A component token collection (eg. button/background/primary) might alias a semantic collection, and it is the component collection you need to reference. In some other examples, there may be no aliasing and you're simply value matching.

Gap and padding values for frames are really important and often have to be interpreted semantically or based on layout component values.
