protocol: strand-protocol v1.0
journal_schema: tasktree-journal-v1
runtime: tasktree v0.1.1
runtime_path: bin/tasktree.exe
runtime_sha256: 8610b71aed64a7e0bcbeec9f3a90297109c220fb2d97414f365b42a2ee0281fd
rule: never edit journal manually; use tasktree CLI
discover: bin/tasktree.exe --help
version_check: bin/tasktree.exe --version
spec: https://github.com/GodOnlyKn0w/strand-protocol/releases/tag/v1.0

An empty .tasktree/journal.jsonl is a valid empty strand journal.
