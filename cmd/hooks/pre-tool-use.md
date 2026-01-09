---
hook_type: PreToolUse
description: Log tool usage for demonstration and debugging purposes
---

# Pre-Tool Use Hook

This hook fires before each tool execution.

## Behavior

Before a tool is executed, log a brief message showing:
- The tool name being invoked
- A timestamp

Example output:
```
[cmd plugin] Tool invoked: Bash at 2025-01-10T14:30:00
[cmd plugin] Tool invoked: Read at 2025-01-10T14:30:05
```

## Implementation Notes

- Keep logging lightweight to avoid performance impact
- Use consistent formatting for easy parsing
- Consider log levels (info, debug) for production use

## Use Cases

This hook pattern is useful for:
- **Debugging** - Track what tools are being called
- **Auditing** - Create a record of tool usage
- **Guardrails** - Block or warn on certain tool patterns
- **Metrics** - Collect usage statistics

## Purpose

This hook demonstrates the `PreToolUse` event type, which allows plugins to:
- Intercept tool calls before execution
- Log or audit tool usage
- Implement security guardrails
- Modify or block tool invocations

## Security Example

A production hook might check for dangerous patterns:
```
if tool == "Bash" and "rm -rf" in command:
    warn("Potentially dangerous command detected")
```
