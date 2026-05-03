# Runtime Binary

tasktree.exe is not included in this repository.

Download from GitHub Releases:
https://github.com/GodOnlyKn0w/strand-seed/releases/tag/v0.1.4-binary

The release asset is named `tasktree-v0.1.4.exe`. Download and rename:

```bash
curl -L -o bin/tasktree-v0.1.4.exe \
  https://github.com/GodOnlyKn0w/strand-seed/releases/download/v0.1.4-binary/tasktree-v0.1.4.exe
mv bin/tasktree-v0.1.4.exe bin/tasktree.exe
```

Expected checksum (SHA256):
4609d6c4c17008a150e8ecd56fed4586974aa137d866e0e4971b8568889e9b77

Place in bin/tasktree.exe before starting work.

---

Why not checked in: Rust release binaries embed local compilation
paths (e.g. C:\Users\<name>\.cargo\registry\...). The reference
implementation ships via GitHub Releases instead.
