protocol: strand-protocol v1.0
journal_schema: tasktree-journal-v1
runtime: tasktree v0.1.1
runtime_path: bin/tasktree.exe
runtime_sha256: 8610b71aed64a7e0bcbeec9f3a90297109c220fb2d97414f365b42a2ee0281fd
rule: never edit journal manually; use tasktree CLI
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
