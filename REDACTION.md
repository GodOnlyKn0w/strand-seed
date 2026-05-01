# Redaction rules

## Checkpoint action field redaction

The checkpoint `--action` field records action attribution.
It must not expose private causality.

`--action` should describe:

- what was observed
- what action is intended
- why the action is justified by observable evidence

`--action` must not reference:

- private repositories
- internal discussions
- private causal chains
- non-public project names
- private absolute paths

If the reason cannot be stated without private context, cite observable evidence
instead.

Use:

```text
commit seed repair after status/diff review
delete arch32/ after confirming empty via ls
publish report after redaction scan and checksum verification
declare weak-pass after reading journal, diff, and validation log
```

Do not use:

```text
commit fix discovered from private causal chain
delete arch32/ per private discussion on 2026-04-30
publish because a private coordinator approved it
declare pass because Pi-A said it was done
```
