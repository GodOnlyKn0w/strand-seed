Read TASK.md first.

Ensure bin/tasktree.exe is present. Download and verify per CHECKSUMS.md.
Use bin/tasktree.exe for work memory.
Use PROTOCOL.md only for runtime version, checksum, and spec link.
Use REDACTION.md before publishing, redacting, or writing public evidence.

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

Checkpoint rule:
  observe -> checkpoint -> act

Checkpoint is not a save point.
It is a pre-action attribution anchor.

Before any state-closing action, observe the relevant state, then run checkpoint,
then act only if checkpoint exits 0.

State-closing actions include:
  commit, push, merge, tag, delete, move, overwrite, redact, publish,
  close PR, mark done, declare verdict

Observation means reading the current relevant state:
  git: status, diff, staged diff, log, branch
  files: list target paths and inspect affected content
  reports: read the section being closed
  release/publish: run redaction and checksum checks
  experiment verdict: re-read primary evidence, not only summaries

Run:
  bin/tasktree.exe checkpoint --id <current_strand> --action "<intended action, observed state, and reason>"

Continue only if checkpoint exits 0.
If checkpoint fails, stop. Do not perform the intended action.

Journal is append-only.
Do not edit existing journal entries.
If a record is wrong, append a correction.

## Journal and Git

The journal (.tasktree/journal.jsonl) is your runtime memory.
It is NOT tracked by Git. This is intentional:

- Git manages version snapshots. tasktree manages event streams.
- If the journal were tracked, git checkout/stash/branch switch
  would replace it with an older version — silent timeline fork.
- Instead, each entry records git.head as an observation anchor.
  This preserves the causal link without coupling the two timelines.

To create a citable snapshot for evidence or publication:

    bin/tasktree.exe export --out evidence/journal-export.jsonl

The export file can be committed to Git.

Checkpoint records observable action attribution, not private knowledge provenance.

If you get stuck, append before working around.
When stopping, append [open] with current status and what remains.

If command usage is unclear:
  bin/tasktree.exe --help
  bin/tasktree.exe <command> --help

## Packet

Before each session, check inbox:

    ls .packets/inbox/

If packets exist, consume each one before starting work.

### Consume

    Read .packets/inbox/<id>.jsonl
    If .packets/processed/<semantic_hash>.seen exists → skip
    If .packets/processed/<id>.ack exists → skip
    Append to active strand:
      constrain → "[decision] imported constrain: <body> source_packet: <id>"
      incident  → "[observation] incident: <body>"
      next_open → "[open] <body>"
      status    → "[observation] status: <body>"
    touch .packets/processed/<id>.ack
    touch .packets/processed/<semantic_hash>.seen

### Send

    Write packet JSONL to .packets/outbox/<id>.jsonl
    Copy to target project's .packets/inbox/

See https://github.com/GodOnlyKn0w/packet-protocol for format.
