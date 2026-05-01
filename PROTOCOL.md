protocol: strand-protocol v1.0
journal_schema: tasktree-journal-v1
runtime: tasktree v0.1.3
runtime_path: bin/tasktree.exe
runtime_sha256: b3b8fe18e6cad9e9a5aec865019c46ded4a6def3db400958f5e053b41afb8994
discover: bin/tasktree.exe --help
version_check: bin/tasktree.exe --version
spec: https://github.com/GodOnlyKn0w/strand-protocol/releases/tag/v1.0

The journal is plain text JSONL and can be read directly by any tool.
Never edit it manually. Write only through tasktree CLI.
An empty .tasktree/journal.jsonl is a valid empty strand journal.
