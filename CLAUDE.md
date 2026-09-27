# CLAUDE.md — AI Toolchain and Development Guidelines

This document outlines the architecture, toolchain conventions, and developer guidelines for the **Environment-and-AI-toolchain** capstone repository. AI assistants (including Claude Code, Cursor, and related agents) must adhere to these directives when working in this repository.

---

## 1. Project Overview & Philosophy

- **Project:** Environment and AI Toolchain Capstone
- **Maintainer:** Pawan Jakhar ([@P1-Jakhar](https://github.com/P1-Jakhar))
- **Mission:** Establish a robust, reproducible, and production-ready local AI developer toolchain integrating modern CLI tools, intelligent code assistance, and strict version control hygiene.
- **Core Standard:** Automated, self-documenting workflows backed by Conventional Commits and clean repository architecture.

---

## 2. Environment & Toolchain Specifications

All contributors and AI agents must assume and verify the following environment prerequisites:

| Tool | Minimum / Installed Version | Purpose |
| :--- | :--- | :--- |
| **Node.js** | `>= 20.0.0` (LTS v24.19.0) | JavaScript runtime & script execution |
| **npm** | `>= 10.0.0` (v11.17.0) | Package management |
| **Git** | `>= 2.40.0` (v2.55.0) | Version control & release management |
| **Claude Code** | `>= 2.0.0` (v2.1.283) | Terminal-based AI agent workflow |
| **Cursor / VS Code** | Latest Stable | IDE with AI coding extensions |
| **Shell** | PowerShell 7+ / Bash | Cross-platform automation scripts |

---

## 3. Essential Toolchain Commands

When executing tasks or generating automation, prioritize these commands:

### Environment Diagnostics
```bash
# Verify Claude Code installation and diagnostic health
claude doctor

# Verify Node.js and npm versions
node -v
npm -v

# Verify Git version and user configuration
git --version
git config --list --show-origin
```

### Git & Branching
```bash
# Check status with untracked files
git status

# Inspect commit log formatted cleanly
git log --oneline --graph --decorate -n 10
```

---

## 4. Conventional Commits Standard

This project strictly enforces the **Conventional Commits 1.0.0** specification. Every commit message must be structured as follows:

```
<type>[optional scope]: <description>

[optional body]

[optional footer(s)]
```

### Allowed Types
- **`feat`**: A new feature or capability introduced to the repository.
- **`fix`**: A bug fix or corrective adjustment.
- **`docs`**: Documentation updates or additions (e.g., README, guides).
- **`style`**: Formatting, whitespace, or visual styling changes (no production code change).
- **`refactor`**: Code restructurings that neither fix bugs nor add features.
- **`perf`**: Performance optimizations or efficiency enhancements.
- **`test`**: Adding missing tests, mocking routines, or updating test configurations.
- **`build`**: Changes affecting build systems or external dependencies.
- **`ci`**: CI/CD pipeline and automation configuration updates.
- **`chore`**: Maintenance tasks, repository housekeeping, license, or .gitignore updates.

### Rules for Commit Messages
1. Use imperative, present-tense verbs: *"add"*, not *"added"* or *"adds"*.
2. Do not capitalize the first letter of the description.
3. No trailing period (`.`) in the subject line.
4. Keep the summary under 72 characters.
5. Provide detailed rationale in the commit body when the change is non-trivial.

---

## 5. AI Assistant & Agent Directives

When interacting with this codebase as an AI assistant:

1. **Verify Before Modifying:** Always inspect existing files, tests, and configuration prior to issuing changes.
2. **Atomic Changes:** Keep edits focused and self-contained; do not introduce unrelated modifications.
3. **No Secret Leaks:** Never commit API keys, tokens, credentials, or private URLs. Check `.gitignore` before adding sensitive file patterns.
4. **Preserve Documentation Integrity:** Maintain existing comments, markdown structures, and author attributions unless explicitly requested to revise.
5. **Cross-Platform Compatibility:** Ensure shell scripts and instructions function seamlessly across Windows (PowerShell) and POSIX (Bash/Linux/macOS).

---

## 6. Project Layout

```text
Environment-and-AI-toolchain/
├── .gitignore          # Ignored files, caches, and environment secrets
├── assets/             # Media, verification screenshots, and diagrams
├── CLAUDE.md           # Instructions and conventions for AI assistants
├── .cursorrules        # Workspace guidelines for Cursor IDE
├── LICENSE             # MIT License
└── README.md           # Comprehensive repository guide and capstone documentation
```
