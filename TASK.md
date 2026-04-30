Task summary here.

Each step:

Step 1: <action>
  → bin/tasktree.exe append "[decision] Plan: <what and why>"
  → checkpoint: bin/tasktree.exe list && bin/tasktree.exe show <id>
  → execute
  → verify
  → bin/tasktree.exe append "[progress] <result>" or "[friction] <block>"

Step N: ...

End with [done] if complete, [open] if paused.

Before destructive actions: follow the checkpoint rule in AGENTS.md.
