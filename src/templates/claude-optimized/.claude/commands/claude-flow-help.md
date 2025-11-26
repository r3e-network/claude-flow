---
name: claude-flow-help
description: Show Claude-Flow commands and usage with batchtools optimization
---

# Claude-Flow Commands (Batchtools Optimized)

## Core Commands with Batch Operations

### System Management (Batch Operations)

- `npx codex-flow start` - Start orchestration system
- `npx codex-flow status` - Check system status
- `npx codex-flow monitor` - Real-time monitoring
- `npx codex-flow stop` - Stop orchestration

**Batch Operations:**

```bash
# Check multiple system components in parallel
npx codex-flow batch status --components "agents,tasks,memory,connections"

# Start multiple services concurrently
npx codex-flow batch start --services "monitor,scheduler,coordinator"
```

### Agent Management (Parallel Operations)

- `npx codex-flow agent spawn <type>` - Create new agent
- `npx codex-flow agent list` - List active agents
- `npx codex-flow agent info <id>` - Agent details
- `npx codex-flow agent terminate <id>` - Stop agent

**Batch Operations:**

```bash
# Spawn multiple agents in parallel
npx codex-flow agent batch-spawn "code:3,test:2,review:1"

# Get info for multiple agents concurrently
npx codex-flow agent batch-info "agent1,agent2,agent3"

# Terminate multiple agents
npx codex-flow agent batch-terminate --pattern "test-*"
```

### Task Management (Concurrent Processing)

- `npx codex-flow task create <type> "description"` - Create task
- `npx codex-flow task list` - List all tasks
- `npx codex-flow task status <id>` - Task status
- `npx codex-flow task cancel <id>` - Cancel task

**Batch Operations:**

```bash
# Create multiple tasks from file
npx codex-flow task batch-create tasks.json

# Check status of multiple tasks concurrently
npx codex-flow task batch-status --ids "task1,task2,task3"

# Process task queue in parallel
npx codex-flow task process-queue --parallel 5
```

### Memory Operations (Bulk Processing)

- `npx codex-flow memory store "key" "value"` - Store data
- `npx codex-flow memory query "search"` - Search memory
- `npx codex-flow memory stats` - Memory statistics
- `npx codex-flow memory export <file>` - Export memory

**Batch Operations:**

```bash
# Bulk store from JSON file
npx codex-flow memory batch-store data.json

# Parallel query across namespaces
npx codex-flow memory batch-query "search term" --namespaces "all"

# Export multiple namespaces concurrently
npx codex-flow memory batch-export --namespaces "project,agents,tasks"
```

### SPARC Development (Parallel Workflows)

- `npx codex-flow sparc modes` - List SPARC modes
- `npx codex-flow sparc run <mode> "task"` - Run mode
- `npx codex-flow sparc tdd "feature"` - TDD workflow
- `npx codex-flow sparc info <mode>` - Mode details

**Batch Operations:**

```bash
# Run multiple SPARC modes in parallel
npx codex-flow sparc batch-run --modes "spec:task1,architect:task2,code:task3"

# Execute parallel TDD for multiple features
npx codex-flow sparc batch-tdd features.json

# Analyze multiple components concurrently
npx codex-flow sparc batch-analyze --components "auth,api,database"
```

### Swarm Coordination (Enhanced Parallelization)

- `npx codex-flow swarm "task" --strategy <type>` - Start swarm
- `npx codex-flow swarm "task" --background` - Long-running swarm
- `npx codex-flow swarm "task" --monitor` - With monitoring

**Batch Operations:**

```bash
# Launch multiple swarms for different components
npx codex-flow swarm batch --config swarms.json

# Coordinate parallel swarm strategies
npx codex-flow swarm multi-strategy "project" --strategies "dev:frontend,test:backend,docs:api"
```

## Advanced Batch Examples

### Parallel Development Workflow:

```bash
# Initialize complete project setup in parallel
npx codex-flow batch init --actions "memory:setup,agents:spawn,tasks:queue"

# Run comprehensive analysis
npx codex-flow batch analyze --targets "code:quality,security:audit,performance:profile"
```

### Concurrent Testing Suite:

```bash
# Execute parallel test suites
npx codex-flow sparc batch-test --suites "unit,integration,e2e" --parallel

# Generate reports concurrently
npx codex-flow batch report --types "coverage,performance,security"
```

### Bulk Operations:

```bash
# Process multiple files in parallel
npx codex-flow batch process --files "*.ts" --action "lint,format,analyze"

# Parallel code generation
npx codex-flow batch generate --templates "api:users,api:products,api:orders"
```

## Performance Tips

- Use `--parallel` flag for concurrent operations
- Batch similar operations to reduce overhead
- Leverage `--async` for non-blocking execution
- Use `--stream` for real-time progress updates
- Enable `--cache` for repeated operations

## Monitoring Batch Operations

```bash
# Real-time batch monitoring
npx codex-flow monitor --batch

# Batch operation statistics
npx codex-flow stats --batch-ops

# Performance profiling
npx codex-flow profile --batch-execution
```
