# Security Policy

## Scope

ZLAR Gate is a policy enforcement gateway for AI coding agents. It intercepts tool calls from Claude Code, Cursor, and Windsurf, evaluates them against a signed policy, and routes flagged actions through Telegram for human approval.

Any vulnerability that allows an agent (or external attacker) to bypass policy evaluation, forge approval responses, tamper with the audit trail, or execute actions without gate interception is in scope.

---

## Reporting a Vulnerability

**Do not open a public issue for security vulnerabilities.**

Use GitHub's private vulnerability reporting:

1. Go to [ZLAR-AI/ZLAR-Gate Security Advisories](https://github.com/ZLAR-AI/ZLAR-Gate/security/advisories)
2. Click **"Report a vulnerability"**
3. Provide a clear description, reproduction steps, and affected components

We will acknowledge receipt within 48 hours and provide a timeline for remediation. We aim to resolve critical issues within 14 days.

If you cannot use GitHub's reporting tool, email **hello@zlar.ai** with the subject line "Security: ZLAR-Gate" and we will establish a private channel.

---

## Threat Model

ZLAR Gate defends against the following adversaries:

**Policy bypass.** The agent or a tool-call payload attempts to circumvent policy evaluation — for example, by injecting newlines into hook arguments to split a single command into multiple evaluations, or by encoding dangerous operations to evade pattern matching. Ed25519 signature verification ensures policy integrity.

**Audit trail manipulation.** An attacker attempts to modify or truncate the hash-chained audit log to conceal unauthorized actions. The prev_hash chain makes silent deletion or reordering mathematically detectable.

**Telegram channel compromise.** An attacker sends forged approval responses to the gate. The gate validates message source against configured chat_id and bot token.

### Out of Scope

ZLAR Gate does not protect against compromise of the host operating system, IDE vulnerabilities, or attacks that occur outside the tool-call interception layer. For OS-level containment, see [ZLAR-OC](https://github.com/ZLAR-AI/ZLAR-OC).

---

## Supported Versions

| Version | Supported |
|---------|-----------|
| main (HEAD) | Yes |
| Tagged releases | Yes, current and previous minor |

---

## Disclosure Policy

We practice coordinated disclosure. If you report a vulnerability, we will:

1. Acknowledge within 48 hours
2. Confirm the issue and assess severity within 7 days
3. Develop and test a fix
4. Release the fix and publish a security advisory
5. Credit you in the advisory (unless you prefer anonymity)

We ask that reporters refrain from public disclosure until a fix is available, or until 90 days have elapsed — whichever comes first.

---

## Security Design Principles

ZLAR Gate follows one invariant: **intelligence above, enforcement below, human authority over both.**

The gate daemon evaluates actions against a signed policy — it does not reason, negotiate, or make exceptions. Simplicity is the security property. A mechanism too simple to be persuaded is a mechanism that cannot be socially engineered.

For the complete ZLAR security architecture, see [ZLAR-OC SECURITY.md](https://github.com/ZLAR-AI/ZLAR-OC/blob/main/SECURITY.md).
