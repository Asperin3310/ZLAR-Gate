# Contributing to ZLAR Gate

ZLAR Gate is an open-source policy enforcement gateway for AI coding agents. It is maintained by [ZLAR Inc.](https://zlar.ai) and welcomes contributions from anyone who cares about agent governance.

---

## How to Contribute

### Reporting Issues

If you find a bug, a gap in documentation, or have a suggestion, open an issue. Be specific — include what you expected, what happened, and steps to reproduce if applicable.

### Security Disclosures

If you discover a security vulnerability, **do not open a public issue.** Use [GitHub's private vulnerability reporting](https://github.com/ZLAR-AI/ZLAR-Gate/security/advisories) instead. See [SECURITY.md](SECURITY.md) for our full disclosure policy.

### Pull Requests

1. Fork the repository
2. Create a branch from `main` for your change
3. Make focused changes — one concern per PR
4. Run `bash -n bin/zlar-gate` to syntax-check your changes
5. Write a clear description of what the change does and why
6. Submit the PR

We review PRs for correctness, security implications, and alignment with the project's architecture. PRs that affect policy evaluation, audit trail integrity, or Telegram approval flow receive closer scrutiny — this is expected and intentional.

### Code Standards

ZLAR Gate's codebase is primarily shell scripts and JSON configuration. Contributions should:

- Follow existing patterns and naming conventions
- Include comments explaining *why*, not *what*
- Document security implications in the commit message if the change touches enforcement logic

### Documentation

Documentation improvements are always welcome. If you found something confusing during setup, a PR that clarifies it helps everyone who comes after you.

---

## What We're Looking For

- **Adapter testing** — testing Gate with different Cursor and Windsurf configurations and hook payloads
- **Edge case coverage** — unusual tool-call patterns, Unicode in arguments, very long commands
- **Platform support** — ZLAR Gate targets macOS and Linux
- **Policy templates** — domain-specific policy examples (web dev, data science, DevOps)

---

## Code of Conduct

Be respectful, be specific, be constructive. Engage with the substance of ideas, not the identity of contributors.

---

## License

By contributing to ZLAR Gate, you agree that your contributions will be licensed under the [Apache License 2.0](LICENSE).
