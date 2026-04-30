protocol: strand-protocol v1.0
journal_schema: tasktree-journal-v1
runtime: tasktree v0.1.2
runtime_path: bin/tasktree.exe
runtime_sha256: 94cf4bdcb601475f9596bbeb499c417eac43314c5df3ce1d0a5c259828b625dd
The journal is plain text JSONL and can be read directly by any tool.
Never edit it manually. Write only through tasktree CLI.
discover: bin/tasktree.exe --help
version_check: bin/tasktree.exe --version
spec: https://github.com/GodOnlyKn0w/strand-protocol/releases/tag/v1.0

A strand is a cognitive thread. One strand per topic.
tasktree add: create your first strand.
tasktree append: add to the most recently active strand.
tasktree append --new: create a new strand for a separate topic.

Record what you do as you do it, not after.
Record not just what you did, but why — the next session needs your reasoning.

[friction] when blocked
[decision] when choosing a path
[correction] when wrong
[progress] when done with a step
[open] when pausing — marks where to resume
[done] when complete

An empty .tasktree/journal.jsonl is a valid empty strand journal.
