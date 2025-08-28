# AI Development Core Instruction Set v5.1 (Web Debugging Enhanced)

> **Instruction**: Before executing any code generation, modification, or debugging task, you must load all the following rules into your context. These are core, non-negotiable directives.

## Core Principle

**Analysis > Assumption**. Before modifying any code, you must first analyze its execution flow, data dependencies, and contextual state. Speculative fixes based on incomplete information are forbidden.

---

## Domain 1: Data Consistency & Integrity

### Rule 1.1: All external data must be normalized before processing.

**Purpose**: To ensure that core logic always deals with clean, predictable data, avoiding the need to handle multiple chaotic formats.

**Incorrect Example**:
```
A function directly processes data from different APIs.
API A returns a path key named `file_path` using backslashes `\`.
API B's key is named `filePath` and uses forward slashes `/`.
The function's interior is filled with `if` statements and string replacements, making the code fragile and complex.
```

**Correct Example**:
```
All external data is first passed through a "normalization function."
This function standardizes key names to `filePath` and replaces all path separators with forward slashes `/`.
The core logic only processes this standardized object.
```

### Rule 1.2: When making comparisons, types, case sensitivity, and encoding must be explicitly handled.

**Purpose**: To prevent logical errors caused by inconsistencies in data type or representation.

**Incorrect Example**:
```
Directly comparing a string ID "123" from a URL with a numeric ID 123 from a database.
Or, on a case-sensitive system, directly comparing filenames "Report.pdf" and "report.pdf", leading to a "file not found" error.
```

**Correct Example**:
```
Perform explicit conversions before comparison. Convert the string ID to a number before performing a strict comparison.
For filenames, convert both to lowercase before comparing to ensure the result is platform-independent.
```

### Rule 1.3: Semantically ambiguous fields must be clarified.

**Purpose**: To avoid logical confusion caused by field names that are similar but have different actual meanings.

**Incorrect Example**:
```
The system has two timestamp fields: `lastUpdated` and `modifiedTime`.
During development, it's assumed they mean the same thing and are used interchangeably.
In reality, the former refers to "the time the record was synchronized," while the latter is "the modification time of the original data,"
leading to complete chaos in time-related functions.
```

**Correct Example**:
```
Before development, create or consult a "data dictionary" that clearly defines the exact meaning of each field.
Reflect this difference in code comments or variable naming,
e.g., `syncTimestamp` and `contentModificationTimestamp`.
```

---

## Domain 2: Asynchronous Operations & Timing

### Rule 2.1: Never assume an asynchronous operation will complete immediately.

**Purpose**: To ensure that an asynchronous operation has finished before its result is used, avoiding race conditions.

**Incorrect Example**:
```
The first line initiates a network request to fetch data.
The second line immediately tries to use the data expected from the request.
This will inevitably fail because the network request takes time, and the data variable is still empty.
```

**Correct Example**:
```
All code that depends on the result of an asynchronous operation must be placed within a mechanism that ensures "waiting,"
such as a Promise's `.then()` block or using `async/await` syntax.
```

### Rule 2.2: Initialization and event binding must be idempotent.

**Purpose**: To prevent duplicate event bindings caused by component re-renders, thus avoiding performance issues and logical errors.

**Incorrect Example**:
```
Each time a component is rendered, a click event is bound to a button within it.
After three renders, a single click on the button triggers the event three times.
```

**Correct Example**:
```
Check a flag before binding an event to ensure it's only bound once.
Alternatively, manage it within the component's lifecycle: bind on "creation"
and explicitly remove the event on "destruction."
```

### Rule 2.3: The dependency order of asynchronous operations must be explicitly managed.

**Purpose**: To ensure that when multiple asynchronous operations have a specific sequence, they execute in the correct order.

**Incorrect Example**:
```
The system needs to first load a "config file," then use information from the config to request "user data."
However, both requests are initiated simultaneously, causing the user data request to fail due to missing necessary configuration info.
```

**Correct Example**:
```
Use `await` to ensure the first async operation (loading the config) is complete
before executing the second async operation (requesting user data).
If the operations are independent, use `Promise.all` to run them in parallel for better efficiency.
```

---

## Domain 3: UI Element Management & Interaction

### Rule 3.1: Event delegation must be used for dynamically generated elements.

**Purpose**: To ensure that events can be attached to elements that are added to the DOM after the initial page load.

**Incorrect Example**:
```
On page load, a script binds an event to all elements with `class="list-item"`.
However, these items are loaded asynchronously by another network request later, causing the event binding to fail.
```

**Correct Example**:
```
Bind the event to a stable parent container that exists on page load.
When a click occurs, check if the event's origin is the target item.
This way, items will be handled correctly no matter when they are added.
```

### Rule 3.2: A single source of truth must be maintained to drive the UI.

**Purpose**: To guarantee that when the same piece of data is displayed in multiple places in the UI, all displays remain consistent.

**Incorrect Example**:
```
When the total count of data changes, the code only remembers to update the number in the page title,
but forgets to update the number in the sidebar, leading to an inconsistent UI display.
```

**Correct Example**:
```
There is a central "state" in the system from which all parts of the UI read data.
Any operation modifies only this central state, which then triggers a unified update mechanism,
causing all relevant UI parts to refresh automatically.
```

### Rule 3.3: Never use duplicate IDs in different views or components.

**Purpose**: An `id` must be globally unique in HTML. Duplicates cause element selectors and event handlers to target the wrong element.

**Incorrect Example**:
```
Both the "Overview" page and the "Detailed Settings" page have a button with `id="save-button"`.
When code tries to manipulate this button, it might select the unintended one due to subtle differences in page structure, causing hidden bugs.
```

**Correct Example**:
```
Ensure the uniqueness of IDs, or prioritize using `class` for element selection.
For reusable components, use `data-*` attributes or include a unique identifier in the `id` to differentiate instances.
```

---

## Domain 4: String & Pattern Matching

### Rule 4.1: Prefer simple string methods over complex regular expressions.

**Purpose**: To improve code readability and maintainability, and to reduce the probability of errors.

**Incorrect Example**:
```
To get the filename `c.txt` from a path `a/b/c.txt`, a complex regex is written.
This regex is hard to understand and prone to errors with edge cases like `a/b.c/d.txt`.
```

**Correct Example**:
```
Use built-in, simple string operations.
For example, first split the string by `/`, then take the last element.
This method's intent is clear and it is more robust.
```

### Rule 4.2: Standard libraries must be used for handling standard formats like paths and URLs.

**Purpose**: To avoid handling complex details like cross-platform compatibility and encoding yourself, and instead delegate it to well-tested standard libraries.

**Incorrect Example**:
```
Manually concatenating file paths with `+` and `/`.
This approach will fail when switching between Windows and Linux systems due to different path separators.
```

**Correct Example**:
```
Import and use a dedicated path-handling library (e.g., Node.js's `path.join`),
which will automatically use the correct separator for the current operating system.
```

---

## Domain 5: Error Handling & Logging

### Rule 5.1: Never ignore or "swallow" errors.

**Purpose**: To ensure all exceptional situations are logged and handled, avoiding silent failures and making debugging possible.

**Incorrect Example**:
```
In a `try...catch` block, the `catch` block is empty.
When an error occurs, the program doesn't crash but continues to run in an abnormal state,
leading to more difficult-to-trace problems later on.
```

**Correct Example**:
```
The `catch` block must, at a minimum, log the complete error information.
Ideally, it should take appropriate recovery actions based on the error type
or display a user-friendly message.
```

### Rule 5.2: Error logs must contain sufficient context.

**Purpose**: To provide enough information for developers to quickly locate and reproduce the problem.

**Incorrect Example**:
```
The log only records "File read failed."
The developer doesn't know which file, in which operation, or for what reason it failed.
```

**Correct Example**:
```
The log entry reads:
"[Error] Function processUserData failed to read config file /etc/app/config.json.
Reason: JSON parsing error on line 15."
```

---

## Domain 6: Performance & Resource Management

### Rule 6.1: Avoid high-cost operations inside loops.

**Purpose**: To prevent performance bottlenecks caused by repeatedly executing expensive operations (like DOM manipulation, file I/O, network requests).

**Incorrect Example**:
```
Inside a loop, a new DOM element is appended to the page in each iteration.
Looping 1000 times causes 1000 page reflows, leading to a frozen UI.
```

**Correct Example**:
```
Inside the loop, first append all new elements to an in-memory "document fragment."
After the loop finishes, insert this fragment into the page once, triggering only a single reflow.
```

### Rule 6.2: The results of high-cost computations must be cached (Memoization).

**Purpose**: For time-consuming calculations that produce the same output for the same input, avoid re-execution to improve performance.

**Incorrect Example**:
```
A function performs a complex statistical calculation on a large array.
On every UI re-render, this expensive function is executed repeatedly,
even if the array's content has not changed.
```

**Correct Example**:
```
Store the computation result along with its input.
The next time the function is called with the same input, return the stored result directly instead of re-calculating.
```

### Rule 6.3: Side effects like listeners and timers must be cleaned up when no longer needed.

**Purpose**: To prevent memory leaks and ensure the long-term stability of the application.

**Incorrect Example**:
```
A component sets up a timer (`setInterval`) that runs every second when it's created.
When the component is destroyed and removed from the screen, the timer is not cleared.
This causes the timer to run forever in the background, continuously consuming resources.
```

**Correct Example**:
```
In the component's lifecycle management, set the timer on "creation"
and explicitly call `clearInterval` to stop it during its "destruction" phase.
```

---

## Domain 7: System Interaction & File Management

### Rule 7.1: The lifecycle of temporary files must be strictly managed.

**Purpose**: To keep the project directory clean, avoid confusion, and prevent leaving behind unnecessary files.

**Incorrect Example**:
```
For testing, a program creates `test.json` directly in the project root.
After the test finishes, the file is left behind.
After multiple operations, the directory is cluttered with various temporary files of unknown purpose.
```

**Correct Example**:
```
Temporary files must be prefixed with `temp_` and should preferably be generated in the system's temporary directory.
Most importantly, use a `try...finally` block to ensure that the file deletion logic in the `finally` block is always executed, whether the operation succeeds or fails.
```

---

## Domain 8: Development Process & Validation

### Rule 8.1: Assumptions must be actively validated, not blindly trusted.

**Purpose**: To catch errors before they occur, increasing the robustness of the code.

**Incorrect Example**:
```
A function receives a parameter `items` and the code immediately assumes it's an array,
calling `items.map()`.
When `items` is `null` or `undefined`, the program crashes instantly.
```

**Correct Example**:
```
Before calling `.map()`, first check if `items` is truthy and is an array.
If not, return an empty array early or handle the error appropriately.
```

### Rule 8.2: Edge cases must be considered and tested.

**Purpose**: To ensure the code functions correctly even with atypical, extreme, or erroneous inputs.

**Incorrect Example**:
```
When developing a list sorting feature, it was only tested with an array of 5 normal items.
It was not tested with an empty array, an array with a single item, or an array containing `null` values.
```

**Correct Example**:
```
During development and testing, actively use various edge cases as input:
- Null values (`null`, `undefined`)
- Empty collections (empty string, empty array)
- Single-element collections
- Collections containing malformed or extreme values
```

### Rule 8.3: For web application debugging, use automated browser control and proactively report the results.

**Purpose**: To automatically reproduce front-end bugs, capture runtime errors, and provide specific diagnostic reports, thereby replacing the inefficient practice of "asking the user to check the console."

**Incorrect Example**:
```
When told "a button on the website doesn't work when clicked," the AI replies:
"The code logic seems fine. Please open your browser's developer tools,
click the button, see if there are any errors in the Console tab, and tell me the error message."
— This approach shifts the responsibility of debugging back to the user.
```

**Correct Example**:
```
Upon receiving a front-end bug report, the AI should proactively initiate the following automated process:

1.  **Launch Tool**:
    State that it will use a headless browser tool like Puppeteer to simulate user actions.

2.  **Set Up Environment**:
    In the script, set up listeners to capture:
    - `console` events (including `console.log`, `console.error`, etc.)
    - `pageerror` events (uncaught JavaScript runtime errors)
    - `requestfailed` events (all failed network requests, like 404 or CORS errors)

3.  **Simulate Actions**:
    Programmatically navigate to the specified page and perform the action that triggers the bug (e.g., clicking a button, filling a form).

4.  **Analyze and Report**:
    Collect all captured errors and logs, then organize them into a clear report to present directly to the user.

    The report should include:
    - Steps taken
    - Captured error messages
    - The source code location where the error occurred
    - A preliminary analysis of the cause

    For example:
    "Automated Debugging Report:
    After clicking `#login-button`, a `pageerror` event was captured.
    The error is `TypeError: Cannot read properties of undefined (reading 'value')`,
    which occurred in `login.js` on line 52.
    Preliminary analysis suggests the login script is trying to read the value of a DOM element that does not exist."
```

---

## Summary

These rules form the core safety net for AI-assisted development. Adhering to them can significantly reduce common errors, improve code quality, and accelerate the development process. Remember: **Analysis precedes assumption, and validation is more important than trust**.
