# CMD Plugin - Reference Implementation Testbed

A "hello world" style reference implementation demonstrating all Claude Code plugin feature types.

## Purpose

This plugin serves as a learning resource and testbed for plugin developers. Each component type has a minimal working example you can study and extend.

## Plugin Components

### Commands (`/cmd:*`)

Slash commands that users can invoke directly.

| Command | Description |
|---------|-------------|
| `/cmd:for` | Loop over templates using for-loop syntax, creating todo items |
| `/cmd:hello` | Simple hello world greeting with current time and directory |

### Agents

Specialized agents that can be invoked for specific tasks.

| Agent | Description |
|-------|-------------|
| `hello-agent` | Provides context-aware, personalized greetings |

### Skills

Auto-invoked capabilities that activate based on file patterns.

| Skill | Triggers On | Description |
|-------|-------------|-------------|
| `hello-skill` | `*.greeting`, `welcome.*` | Provides greeting/onboarding expertise |

### Hooks

Event handlers that fire automatically on lifecycle events.

| Hook | Event | Description |
|------|-------|-------------|
| `session-start` | SessionStart | Displays welcome message when session begins |
| `pre-tool-use` | PreToolUse | Logs tool invocations for debugging |

### MCP Servers

External tool integrations configured via `.mcp.json`.

| Server | Description |
|--------|-------------|
| `hello-server` | Placeholder demonstrating MCP configuration structure |

## Directory Structure

```
cmd/
├── .claude-plugin/
│   └── plugin.json         # Plugin metadata
├── commands/
│   ├── for.md              # For-loop command
│   └── hello.md            # Hello world command
├── agents/
│   └── hello-agent.md      # Greeting agent
├── skills/
│   └── hello-skill.md      # Auto-invoked greeting skill
├── hooks/
│   ├── session-start.md    # Session start hook
│   └── pre-tool-use.md     # Tool logging hook
├── .mcp.json               # MCP server configuration
└── README.md               # This file
```

## Usage Examples

```bash
# Invoke hello command
/cmd:hello

# Use for-loop to batch create todos
/cmd:for i in [1,2,3] "Review item ${i}"
```

## Creating Your Own Plugin

Use this plugin as a template:

1. Copy the directory structure
2. Update `plugin.json` with your plugin's metadata
3. Replace the example files with your implementations
4. Test with `/plugin install path/to/your/plugin`

## License

MIT
