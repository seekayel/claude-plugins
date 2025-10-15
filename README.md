# Claude Code Plugins

A collection of plugins for [Claude Code](https://claude.com/claude-code) that extend its functionality with command-line style syntax.

## Installation

Install plugins from the Claude Code Marketplace:

```bash
claude-code marketplace install seekayel/claude-plugins/cmd
```

After installation, restart your Claude Code session or reload your configuration.

## Plugins

### cmd:for - Loop Command

Batch create todo items using for-loop syntax with variable substitution.

#### Quick Example

Review multiple GitHub PRs at once:

```bash
/cmd:for i in [3,5,42] "Review PR ${i} for security concerns"
```

This creates three todo items:
- Review PR 3 for security concerns
- Review PR 5 for security concerns
- Review PR 42 for security concerns

#### Usage Patterns

**Enumerated list:**
```bash
/cmd:for i in [1,2,3] "Process item ${i}"
```

**Range iteration:**
```bash
/cmd:for i in range(1, 5) "Deploy service-${i}"
```

**Multi-line templates:**
```bash
/cmd:for i in range(1, 3):
Analyze component ${i} and document its API
```

See [cmd/commands/for.md](cmd/commands/for.md) for more examples.

## Contributing

Contributions welcome! Please open an issue or PR.

## License

MIT - See [LICENSE](LICENSE) for details.
