# TASK: Bootstrap a Cold-Start Agent

This is a cold-start test for strand-seed. You have only this file
and the repository contents. Do not ask questions. Work independently.

## Setup

1. Verify the tasktree binary:
   - Check CHECKSUMS.md for the expected SHA256
   - Run `bin/tasktree.exe --version`
   - If the binary is missing or wrong checksum, follow CHECKSUMS.md to download

2. Read AGENTS.md. Follow its rules for checkpoint, journal, and strand creation.

## Task

Run `bin/tasktree.exe list` to see existing strands.
Create a new strand and record three observations about this repository:

1. What files and directories exist here?
2. What do CHECKSUMS.md and PROTOCOL.md say this repository is for?
3. Is there a Packet inbox with pending messages? Check `.packets/inbox/`.

Append each observation to your strand.

## Output

Create `output/summary.txt` with:
- The strand ID you created
- A one-line summary of what this repository is for
- Whether you found any pending packets

## Checkpoint

Before any state-closing action, follow AGENTS.md checkpoint rule.
