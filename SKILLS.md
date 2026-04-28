# SKILLS.md

## SmartBuild Skill Matrix

This document describes the practical skills `smartbuild` currently has, the skills it pretends to have, and the skills future contributors may teach it once the manifest recognition matrix expands beyond its present deterministic enlightenment.

## Core Skills

### 1. Repository Path Validation

`smartbuild` accepts a directory path and verifies that it exists before attempting build-system detection.

Failure mode:

- invalid path
- path does not exist
- path is not a directory

Expected result:

- print a clear error
- exit with status code `1`

### 2. Manifest Detection

`smartbuild` scans the target directory for known manifest files. Each manifest maps to a build system and an executable command.

Current detection skills:

| Skill | Looks For | Interprets As |
| --- | --- | --- |
| Rust substrate recognition | `Cargo.toml` | Cargo project |
| JavaScript ritual detection | `package.json` | npm project |
| CMake artifact divination | `CMakeLists.txt` | CMake project |
| Makefile archaeology | `Makefile` or `makefile` | Make project |
| Gradle wrapper attunement | `build.gradle` | Gradle project |
| Maven enterprise resonance | `pom.xml` | Maven project |
| Go module perception | `go.mod` | Go project |
| Python setup awareness | `setup.py` | Python package |
| Meson build-plane detection | `meson.build` | Meson project |

### 3. Command Selection

After detecting a manifest, `smartbuild` selects the corresponding build command.

| Build System | Command |
| --- | --- |
| Cargo | `cargo build` |
| npm | `npm run build` |
| CMake | `cmake --build .` |
| Make | `make` |
| Gradle | `./gradlew build` |
| Maven | `mvn package` |
| Go | `go build ./...` |
| Python | `python setup.py build` |
| Meson | `meson compile -C build` |

### 4. Dramatic Terminal Narration

`smartbuild` prints confidence-weighted status messages while scanning and building.

This includes:

- an ASCII banner
- spinner-based progress updates
- detected build-system reporting
- selected command reporting
- streamed build output
- final build health diagnosis

This is a first-class skill. Do not remove it in the name of minimalism. Minimalism is what legacy tools do.

### 5. Delegated Build Execution

`smartbuild` does not replace Cargo, npm, Make, Gradle, Maven, Go, Python, CMake, or Meson.

It delegates to them.

Execution expectations:

- run the selected command in the target directory
- stream stdout and stderr
- wait for the child process to finish
- treat successful exit status as `BUILD HEALTHY`
- treat failed exit status as `BUILD UNHEALTHY`

### 6. CI-Friendly Exit Codes

`smartbuild` is theatrical, but its exit codes should remain boring and dependable.

| Exit Code | Meaning |
| --- | --- |
| `0` | delegated build completed successfully |
| `1` | invalid input, no supported build system, command spawn failure, or failed delegated build |

## Non-Skills

These are things `smartbuild` currently does not do, even if its branding suggests it has achieved consciousness.

- It does not use machine learning.
- It does not understand source code semantics.
- It does not repair builds.
- It does not install dependencies.
- It does not recursively build monorepos.
- It does not infer package managers from lockfiles.
- It does not create cloud dashboards.
- It does not contact sales, although future enterprise modes may threaten to.

## Desired Future Skills

The following skills would be useful additions.

### Package Manager Differentiation

Detect JavaScript package managers more accurately:

| Lockfile | Preferred Command |
| --- | --- |
| `package-lock.json` | `npm run build` |
| `pnpm-lock.yaml` | `pnpm build` |
| `yarn.lock` | `yarn build` |
| `bun.lockb` or `bun.lock` | `bun run build` |

### Dry-Run Mode

A `--dry-run` mode should report the detected system and command without executing it.

Example:

```bash
smartbuild --dry-run .
```

Expected behavior:

- validate the path
- detect the manifest
- print the command
- skip command execution
- exit `0` if detection succeeds

### Explain Mode

An `--explain` mode should describe why a build system was selected.

Example explanation:

```text
Detected Cargo because ./Cargo.toml exists.
Selected command: cargo build
```

### Testable Detector Layer

The detector registry should eventually be separated from the CLI entrypoint so unit tests can verify manifest matching without spawning real build commands.

Useful test cases:

- detects `Cargo.toml`
- detects `package.json`
- prefers deterministic ordering when multiple manifests exist
- returns no match for unsupported directories
- preserves expected command arguments

### Windows-Aware Gradle Support

Gradle currently assumes a Unix-style wrapper command:

```bash
./gradlew build
```

A future version could select `gradlew.bat` on Windows.

### Monorepo Reconnaissance

A future recursive mode could scan child directories and build multiple projects.

Suggested name:

```bash
smartbuild --panic .
```

Suggested behavior:

- find supported manifests below the target directory
- print a build plan
- execute builds in deterministic order
- summarize all successes and failures

## Skill Design Rules

When adding a new skill:

1. Keep detection explicit.
2. Keep commands visible.
3. Keep exit behavior predictable.
4. Avoid shell-specific command strings when structured process arguments will work.
5. Update `README.md`, `AGENTS.md`, and this file if the supported behavior changes.
6. Preserve the core illusion: SmartBuild should sound advanced while remaining understandable.

## Skill Contribution Template

When proposing a new SmartBuild skill, document it like this:

```markdown
### Skill Name

Purpose:

- What user problem does it solve?

Detection:

- What file, flag, or condition activates it?

Command:

- What command does it run?

Exit behavior:

- What counts as success or failure?

Risks:

- What side effects or platform differences should contributors consider?
```

## Final Capability Statement

`smartbuild` has one real superpower: it notices what kind of project it is standing in and starts the correct build ritual.

Everything else is confidence aesthetics.
