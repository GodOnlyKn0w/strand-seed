Read TASK.md first.

Ensure bin/tasktree.exe is present. Download and verify per CHECKSUMS.md.
Use bin/tasktree.exe for work memory.
Use PROTOCOL.md only for runtime version, checksum, and spec link.

Before reconnaissance:
  bin/tasktree.exe list
  If strands exist, show the most recently active strand.
  If no strands exist, create one with: bin/tasktree.exe add "<task summary>"

Record as you work, not after:
  [decision] when choosing a path
  [progress] when a step lands
  [friction] when blocked
  [correction] when wrong
  [open] when stopping

Before rm, rmdir, mv, git commit, git rebase, or any state-closing action:
  bin/tasktree.exe checkpoint --id <current_strand> --action "<action and reason>"

If you get stuck, append before working around.
When stopping, append [open] with current status and what remains.

If command usage is unclear:
  bin/tasktree.exe --help
  bin/tasktree.exe <command> --help
