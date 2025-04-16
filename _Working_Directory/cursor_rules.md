https://github.com/PatrickJS/awesome-cursorrules

Copy what you need into the cursorrules folder and link to it for context. Always link to taskrules.mcp and a TASK.md in your fontend/backend so multiple people can work on different things and keeps the AI model on track. 

# Prompt Engineering Tips

Prompt engineering is the art of crafting effective instructions for AI models like **AI Agent**. Well-written prompts lead to better results, fewer errors, and a more efficient workflow.

---

## General Principles

### Be Clear and Specific
Clearly state what you want AI Agent to do. Avoid ambiguity.

- **Bad:** `Fix the code.`
- **Good:** `Fix the bug in the calculateTotal function that causes it to return incorrect results.`

### Provide Context
Use **Context Mentions** to refer to specific files, folders, or problems.

- **Good:** `@/src/utils.ts Refactor the calculateTotal function to use async/await.`

### Break Down Tasks
Divide complex tasks into smaller, well-defined steps.

### Give Examples
If you have a specific coding style or pattern in mind, provide examples.

### Specify Output Format
If you need the output in a particular format (e.g., JSON, Markdown), specify it in the prompt.

### Iterate
Don't be afraid to refine your prompt if the initial results aren't what you expect.

---

## Thinking vs. Doing

It's often helpful to guide AI Agent through a "think-then-do" process:

1. **Analyze** – Ask AI Agent to analyze the current code, identify problems, or plan the approach.  
2. **Plan** – Have AI Agent outline the steps it will take to complete the task.  
3. **Execute** – Instruct AI Agent to implement the plan, one step at a time.  
4. **Review** – Carefully review the results of each step before proceeding.

---

## Using Custom Instructions

You can provide custom instructions to further tailor AI Agent's behavior. There are two types:

- **Global Custom Instructions** – Apply to all modes.
- **Mode-Specific Custom Instructions** – Apply only to a specific mode (e.g., `Code`, `Architect`, `Ask`, `Debug`, or a custom mode).

Custom instructions are added to the system prompt, providing persistent guidance to the AI model. You can use these to:

- Enforce coding style guidelines.
- Specify preferred libraries or frameworks.
- Define project-specific conventions.
- Adjust AI Agent's tone or personality.

_See the **Custom Instructions** section for more details._

---

## Handling Ambiguity

If your request is ambiguous or lacks sufficient detail, AI Agent might:

- **Make Assumptions:** Proceed based on its best guess, which may not be what you intended.
- **Ask Follow-Up Questions:** Use the `ask_followup_question` tool to clarify your request.

It's generally better to provide clear and specific instructions from the start to avoid unnecessary back-and-forth.

---

## Providing Feedback

If AI Agent doesn't produce the desired results, you can provide feedback by:

- **Rejecting Actions:** Click the "Reject" button when AI Agent proposes an action you don't want.
- **Providing Explanations:** Explain why you're rejecting the action. This helps AI Agent learn from its mistakes.
- **Rewording Your Request:** Try rephrasing your initial task or providing more specific instructions.
- **Manually Correcting:** If there are a few small issues, directly modify the code before accepting the changes.

---

## Examples

**Good Prompt:**

```
@/src/components/Button.tsx Refactor the Button component to use the useState hook instead of the useReducer hook.
```

**Bad Prompt:**

```
Fix the button.
```

---

**Good Prompt:**

```
Create a new file named utils.py and add a function called calculate_average that takes a list of numbers and returns their average.
```

**Bad Prompt:**

```
Write some Python code.
```

---

**Good Prompt:**

```
@problems Address all errors and warnings in the current file.
```

**Bad Prompt:**

```
Fix everything.
```

---

By following these tips, you can write effective prompts that get the most out of AI Agent's capabilities.
```
