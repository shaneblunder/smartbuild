# smartbuild

> Autonomous AI build orchestration for repositories that are tired of being understood by humans.

![Status](https://img.shields.io/badge/status-autonomous-blue)
![AI](https://img.shields.io/badge/AI-neural%20build%20detection-purple)
![Confidence](https://img.shields.io/badge/confidence-99.7%25-brightgreen)
![Rust](https://img.shields.io/badge/written%20in-Rust-orange)
![Enterprise](https://img.shields.io/badge/enterprise-contact%20sales-gold)

---

## What is smartbuild?

**smartbuild** is the next evolutionary phase of build tooling: an intelligent, autonomous, terminal-native AI experience layer that scans your project, detects its build system, and delegates execution to the correct underlying build mechanism.

In other words:

```sh
smartbuild .
```

Then smartbuild stares deeply into your repository’s soul and decides whether it is dealing with Cargo, npm, CMake, Make, Gradle, Maven, Go, Python, Meson, or whichever build ritual your codebase has chosen as its emotional support system.

---

## The Breakthrough

For decades, developers have been expected to know what kind of project they are in.

This is an unreasonable burden.

Why should a human look for `Cargo.toml`, `package.json`, `Makefile`, `pom.xml`, or `go.mod` when a tiny Rust binary can do that while pretending to be a sentient build agent?

**smartbuild** eliminates this entire class of developer cognition.

It performs revolutionary repository introspection, applies industry-leading confidence aesthetics, and launches the correct build command with the kind of terminal drama normally reserved for cyberpunk operating systems in movies.

---

## Installation

Clone the repository:

```sh
git clone https://github.com/shaneblunder/smartbuild.git
cd smartbuild
```

Build smartbuild using yesterday’s obsolete, non-agentic build tooling:

```sh
cargo build --release
```

Install it somewhere on your `PATH`:

```sh
cp target/release/smartbuild /usr/local/bin/smartbuild
```

Or run it directly:

```sh
cargo run -- .
```

---

## Usage

Point smartbuild at a directory:

```sh
smartbuild .
```

Point it at another directory:

```sh
smartbuild ./some-project
```

Then watch as smartbuild performs:

1. repository consciousness scanning
2. manifest detection
3. heuristic build-system inference
4. confidence-weighted terminal narration
5. autonomous command execution
6. post-build health diagnosis

Which older tools might reductively describe as:

> “checking for files and running a command”

That is the kind of limited thinking smartbuild was created to disrupt.

---

## Why smartbuild?

Because every repository has a build system.

But not every repository has a build system that introduces itself with a box-drawn ASCII banner and a fake neural confidence score.

smartbuild gives you:

- automatic build system detection
- consistent build invocation across ecosystems
- dramatic terminal output
- streaming build logs
- success and failure diagnosis
- a 99.7% confidence rating, because 100% would look suspicious
- enough AI language to make your CI pipeline feel venture-backed

---

## Architecture

```txt
Developer Intent
      ↓
smartbuild .
      ↓
Neural Directory Fingerprint Scanner
      ↓
Manifest Recognition Matrix
      ↓
Build Substrate Classifier
      ↓
Autonomous Command Delegation Layer
      ↓
Cargo / npm / CMake / Make / Gradle / Maven / Go / Python / Meson
      ↓
BUILD HEALTHY or BUILD UNHEALTHY
```

This architecture cleanly separates three mission-critical concerns:

1. **looking impressive**
2. **finding the right build file**
3. **running the command you probably would have typed anyway**

---

## Is this AI?

smartbuild uses the most powerful form of intelligence known to software engineering:

```txt
if file exists, run command
```

Some people call this deterministic programming.

We call it **symbolic repository cognition**.

The difference is branding.

---

## Error Handling

If smartbuild cannot detect a supported build system, it will calmly inform you that your repository has failed to achieve recognizability.

```txt
✘ No recognizable build system detected.
→ Cargo.toml, package.json, CMakeLists.txt, Makefile, makefile, build.gradle, pom.xml, go.mod, setup.py, meson.build
```

This is not an error.

This is a growth opportunity for your repository.

---

## Exit Codes

smartbuild exits with:

| Exit code | Meaning                                                                                                   |
| --------: | --------------------------------------------------------------------------------------------------------- |
|       `0` | The build completed successfully and is officially BUILD HEALTHY                                          |
|       `1` | The build failed, the path was invalid, usage was incorrect, or no recognizable build system was detected |

---

## Roadmap

- [ ] Add `--explain` to describe why a manifest file exists
- [ ] Add `--confidence` to let users choose their preferred fake certainty
- [ ] Add `--enterprise` to print “contact sales”
- [ ] Add `--vibes` to select the build system emotionally
- [ ] Add support for `pnpm`, `yarn`, `bun`, and whatever JavaScript invents next week
- [ ] Add recursive monorepo mode, also known as “panic”
- [ ] Add “AI repair” mode that runs the same command again
- [ ] Add cloud dashboard that displays a spinner and invoices you
- [ ] Add `smartbuild doctor`, which says “have you tried installing dependencies?”
- [ ] Add machine learning once the `if` statements become self-aware

---

## FAQ

### Does smartbuild replace Cargo, npm, Make, Gradle, Maven, Go, Python, CMake, or Meson?

No.

It stands above them as an executive thought leader and tells them when to start working.

### Does smartbuild really detect the build system?

Yes. It checks the target directory through highly complicated detection systems and selects the associated build command.

### Does smartbuild really use AI?

It uses Artificially Inflated terminology.

### Can I use it in CI?

Absolutely.

```yaml
script:
  - smartbuild .
```

Your CI will continue doing normal CI things, but with significantly improved executive presence.

### Is this production-ready?

It is a Rust binary that runs build commands.

So yes.

Also no.

Choose whichever answer helps your pitch deck.

---

## Contributing

Contributions are welcome, especially if they increase:

- actual build system support
- terminal theatrics
- acronym surface area
- investor readability

To contribute:

```sh
git checkout -b feature/autonomous-whatever
```

Then open a pull request explaining how your change advances the field of AI-native deterministic build orchestration.

Bonus points for phrases like:

- agentic
- autonomous
- substrate
- context-aware
- build graph
- neural heuristic
- developer velocity
- self-healing
- enterprise-grade
- frontier model adjacent

---

## License

MIT.

Because intelligence should be free, but enterprise support should probably be a separate SKU.

---

## Final Thought

`make` built the past.

`cargo`, `npm`, `cmake`, `gradle`, `mvn`, `go`, `python`, and `meson` build the present.

**smartbuild** detects the vibe and builds the future.

With 99.7% confidence.
