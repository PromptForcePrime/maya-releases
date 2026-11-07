# Maya releases

Release archives for Maya, a governed control plane for AI-assisted
development: it builds from a spec on its own branch, checks the result with
your tests, and holds it for a person to approve. The source is private; this
repository only hosts the builds.

## Install (macOS, Linux)

```sh
curl -fsSL https://github.com/PromptForcePrime/maya-releases/releases/latest/download/get.sh | sh
```

Needs git and a logged-in Claude Code. The installer checks each archive
against `SHA256SUMS` and puts `maya` in `~/.local/bin`. Then, in a repository:

```sh
maya init
maya build SPEC.md
```

A specific version: `MAYA_VERSION=v0.1.0`. Each release lists its archives
(`maya-<os>-<arch>.tar.gz`), `get.sh` and `SHA256SUMS`.
