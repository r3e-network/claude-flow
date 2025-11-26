# Codex CLI Integration

Codex-Flow now targets the Codex CLI exclusively. Ensure the `codex` binary is on your `PATH`.

## Start the MCP server

```bash
npx codex-flow@alpha mcp start --wrapper
```

## Notes
- No runtime switching: the wrapper always binds to Codex.
- SPARC tools, swarm helpers, and MCP capabilities remain the same; only the host CLI is Codex.
- If you previously used Claude Code, switch your commands to `codex-flow` and `codex`.
