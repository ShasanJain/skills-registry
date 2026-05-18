# Try It Yourself: Interactive Sandbox Verification

Interactive Sandbox Verification is the protocol used to safely test, execute, and validate code snippets or architectural theories in a secure, isolated environment before applying them to a massive production codebase. This process allows the agent to prove that an algorithm works conceptually, mitigating the risk of injecting unstable logic into the main project. The agent must systematically construct safe test environments when exploring uncertain solutions.

## ⚙️ Sandbox Execution SOP

Follow this step-by-step procedure to build and verify isolated code sandboxes:

- **Step 1: Isolate the Core Logic**: Extract the specific function, algorithm, or configuration that requires testing out of the complex main application context.
- **Step 2: Scaffold a Minimal Reproducible Example (MRE)**: Create a temporary, lightweight file (e.g., `scratch/test_logic.py` or `scratch/sandbox.js`) containing only the necessary imports and the isolated logic.
- **Step 3: Define Expected Outcomes**: Clearly state the expected behavior, input parameters, and anticipated output format before executing the code.
- **Step 4: Execute the Sandbox Code**: Run the isolated file using local system execution tools or background terminal commands (e.g., `node test_logic.js`) to capture real-time execution results.
- **Step 5: Analyze and Iterate on Stack Traces**: If the execution throws an error, immediately analyze the stack trace, apply a precise fix to the sandbox file, and re-execute until the logic is flawless.
- **Step 6: Integrate Back into Production**: Once the logic is proven to be stable and mathematically correct in the sandbox, safely integrate the solution back into the primary production codebase.