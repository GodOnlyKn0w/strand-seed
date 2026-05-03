# strand-seed

A drop-in folder for agent work.

1. Write the task in TASK.md.
2. Ask an agent to work in this folder.
3. Check output/ for results.
4. If work stops mid-task, drop in a different agent. It will resume.

Supports [Packet v3](https://github.com/GodOnlyKn0w/packet-protocol)
for cross-boundary constraint delivery.

The tasktree journal is excluded from Git (see AGENTS.md).
Git snapshots the code; tasktree records the agent's thinking.
They are separate timelines, connected by git.head in each entry.
