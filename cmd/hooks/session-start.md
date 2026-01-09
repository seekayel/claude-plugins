---
hook_type: SessionStart
description: Display a welcome message when a Claude Code session starts
---

# Session Start Hook

This hook fires when a new Claude Code session begins.

## Behavior

When a session starts, display a brief welcome message:

```
[cmd plugin] Session started. Hello world hooks are active.
```

## Implementation Notes

- Keep the message brief and non-intrusive
- Use a prefix like `[cmd plugin]` to identify the source
- Avoid blocking or delaying session startup

## Purpose

This hook demonstrates how to respond to session lifecycle events in Claude Code plugins. Hooks differ from commands, agents, and skills in that they:
- Fire automatically in response to events
- Cannot be directly invoked by users
- Are useful for setup, logging, and guardrails

## Available Hook Types

- `SessionStart` - Fires when session begins (this hook)
- `PreToolUse` - Fires before each tool execution
- `Stop` - Fires when session is ending
