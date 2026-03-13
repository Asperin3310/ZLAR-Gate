# Legal Notice — ZLAR Gate

**Effective Date:** March 2026
**Entity:** ZLAR Inc., a corporation incorporated under the Canada Business Corporations Act (CBCA)

---

## 1. Regulatory Classification

ZLAR Gate is a deterministic, rule-based policy enforcement tool. It does not use machine learning, does not make inferences from inputs, and does not generate predictions, recommendations, or decisions. It classifies tool calls via string matching against human-authored rules and halts actions pending human approval.

Under the definitions established by the EU AI Act (Regulation 2024/1689, Article 3(1)), the OECD AI framework, the Colorado AI Act (SB 24-205), and other enacted AI legislation, **ZLAR Gate does not meet the definition of an "AI system."** Recital 12 of the EU AI Act explicitly excludes "systems that are based on the rules defined solely by natural persons to automatically execute operations."

ZLAR Gate is a governance tool that helps operators of AI systems manage risk. It is not itself an AI system. AI-specific regulatory obligations do not apply to ZLAR Gate.

ZLAR Gate may assist AI system operators in satisfying obligations under Articles 9 (risk management), 14 (human oversight), and 15 (cybersecurity) of the EU AI Act. However, ZLAR Inc. makes no representation that use of ZLAR Gate satisfies any specific regulatory requirement.

---

## 2. Software Provided "As Is"

ZLAR Gate is provided "AS IS" and "AS AVAILABLE" without warranty of any kind, express or implied, including but not limited to the implied warranties of merchantability, fitness for a particular purpose, non-infringement, and any warranties arising out of course of dealing or usage of trade.

ZLAR Inc., its founders, officers, directors, employees, contributors, and agents (collectively, "ZLAR Parties") make no representations or warranties regarding:

- The completeness, accuracy, reliability, or suitability of ZLAR Gate for any purpose
- The ability of ZLAR Gate to prevent, detect, contain, or mitigate any specific threat, vulnerability, or harmful action
- The continuous, uninterrupted, error-free, or secure operation of ZLAR Gate
- The compatibility of ZLAR Gate with any specific framework, tool, model, or runtime environment, including but not limited to Claude Code, Cursor, Windsurf, or any future AI coding agent framework

---

## 3. No Guarantee of Governance

**ZLAR Gate is a governance tool, not a guarantee.**

ZLAR Gate provides policy enforcement mechanisms for AI agent tool calls across supported frameworks. It is designed to classify risk, match against human-authored policy rules, and halt actions pending human approval. However:

- **No governance system can guarantee containment.** AI agents may behave in ways that are novel, unexpected, or outside the design parameters of any enforcement mechanism.
- **ZLAR Gate does not control the AI model.** It operates at the tool-call layer. The model's reasoning, intent, and outputs are outside ZLAR Gate's enforcement surface.
- **ZLAR Gate does not replace human judgment.** It provides a structured mechanism for human review. The quality of governance depends on the policy rules you write, the approval decisions you make, and the diligence of your oversight.
- **Agentic AI is an emerging technology.** The behavior of autonomous AI systems is not fully understood by any entity — including model providers, researchers, and governance tool developers. Users acknowledge this inherent uncertainty.

### Known Limitations

ZLAR Inc. discloses the following limitations in the interest of transparency:

- **Cursor's `afterFileEdit` hook fires after the edit is applied.** File edits in Cursor are audited but cannot be pre-blocked. Shell commands and MCP calls are fully gated.
- **Policy rules use regex matching for shell commands.** Obfuscated commands (variable indirection, base64 encoding, eval wrappers) may not be caught by string-level rules. This is a fundamental limitation of any regex-based classifier.
- **The adapter translation layer maps each framework's tool names and JSON schema.** When frameworks update their hook protocols, adapters may need updating. ZLAR Inc. makes no guarantee of compatibility with future framework versions.
- ZLAR Gate governs only the tool-call layer. Actions taken outside the hooks protocol are not intercepted.
- ZLAR Gate has not undergone independent third-party security audit as of the effective date of this notice.

This disclosure is provided to ensure that users can make informed decisions. It is not an exhaustive list of all possible limitations.

---

## 4. Assumption of Risk

By downloading, installing, configuring, or using ZLAR Gate, you expressly acknowledge and agree that:

a) You understand that agentic AI systems can take actions that are unexpected, harmful, or irreversible.

b) You understand that ZLAR Gate is a risk-reduction tool, not a risk-elimination tool.

c) You assume full responsibility for all actions taken by any AI agent operating on your systems, whether or not ZLAR Gate is installed and functioning.

d) You assume full responsibility for the configuration, deployment, and maintenance of ZLAR Gate, including the authoring of policy rules, the management of cryptographic keys, and the review of approval requests.

e) You understand that ZLAR Gate has not been independently certified, audited, or validated by any regulatory body, standards organization, or third-party security firm as a sufficient governance mechanism for any particular use case, jurisdiction, or compliance requirement.

f) You are solely responsible for determining whether ZLAR Gate is appropriate for your use case, your regulatory environment, and your risk tolerance.

---

## 5. Limitation of Liability

TO THE MAXIMUM EXTENT PERMITTED BY APPLICABLE LAW, IN NO EVENT SHALL ANY ZLAR PARTY BE LIABLE FOR ANY:

- Direct, indirect, incidental, special, consequential, exemplary, or punitive damages
- Loss of profits, revenue, data, goodwill, or business opportunity
- Cost of procurement of substitute goods or services
- Damages arising from unauthorized access to or alteration of your data, systems, or transmissions
- Damages arising from the actions or failures of any AI agent, model, or system, whether or not governed by ZLAR Gate
- Damages arising from the failure of ZLAR Gate to prevent, detect, or contain any specific action, threat, or vulnerability

This limitation applies regardless of the legal theory and regardless of whether any ZLAR Party has been advised of the possibility of such damages.

**In jurisdictions that do not permit the exclusion or limitation of certain damages:** the aggregate liability of all ZLAR Parties for all claims arising from or related to ZLAR Gate shall not exceed the amount you paid to ZLAR Inc. for ZLAR Gate in the twelve (12) months preceding the claim, or CAD $100, whichever is greater.

---

## 6. Third-Party Dependencies

ZLAR Gate interacts with and depends upon third-party software and services, including but not limited to:

- **Anthropic's Claude Code** — ZLAR Inc. is not affiliated with, endorsed by, or responsible for Anthropic or its products.
- **Cursor** — ZLAR Inc. is not affiliated with or responsible for Cursor or Anysphere Inc.
- **Windsurf / Codeium** — ZLAR Inc. is not affiliated with or responsible for Windsurf or Codeium Inc.
- **Telegram** — used for approval notifications. ZLAR Inc. is not responsible for Telegram's service, availability, or security.
- **Any open source dependency** — ZLAR Inc. does not guarantee the security, correctness, or availability of any dependency.

ZLAR Inc. has no control over and assumes no responsibility for the behavior, availability, security, or compliance of any third-party software, service, or platform. Changes to third-party hook protocols may affect ZLAR Gate's operation without notice.

---

## 7. No Professional Advice or Regulatory Certification

Nothing in ZLAR Gate's documentation, source code, examples, or communications constitutes legal advice, security consulting, assurance, or certification, or compliance guidance for any regulatory framework, including but not limited to the EU AI Act, GDPR, CCPA, NIST AI RMF, or any other framework.

ZLAR Inc. does not certify that use of ZLAR Gate constitutes compliance with any standard. If you require assurance, consult qualified legal and security professionals.

---

## 8. Indemnification

You agree to indemnify, defend, and hold harmless all ZLAR Parties from and against any and all claims, damages, losses, liabilities, costs, and expenses (including reasonable legal fees) arising from or related to your use of ZLAR Gate, your violation of these terms, any actions taken by AI agents operating on your systems, or any claim by a third party arising from your deployment of ZLAR Gate.

---

## 9. Vulnerability Disclosure and Security Maintenance

Report security vulnerabilities via [GitHub's private vulnerability reporting](https://github.com/ZLAR-AI/ZLAR-Gate/security/advisories). This commitment does not create an obligation to provide ongoing maintenance, support, or updates. ZLAR Gate is open source software provided without a service level agreement.

---

## 10. Open Source Distribution and EU Compliance

ZLAR Gate is distributed as free, open source software under the Apache License 2.0 outside the course of a commercial activity.

Under the EU Cyber Resilience Act (entered into force December 10, 2024), non-commercial open source software is exempt from the CRA's product cybersecurity requirements. Under the revised EU Product Liability Directive (Directive 2024/2853, transposition deadline December 2026), free open source software developed or supplied outside the course of a commercial activity is excluded from strict product liability.

**ZLAR Inc. relies on these exemptions.** Commercial offerings, if any, will be governed by separate terms.

---

## 11. Intellectual Property

ZLAR Gate is licensed under the Apache License 2.0. "ZLAR," "ZLAR Gate," "ZLAR-OC," "ZLAR-CC," and associated marks are trademarks of ZLAR Inc.

---

## 12. Data and Privacy

ZLAR Gate processes data locally on your machine. It does not transmit data to ZLAR Inc. ZLAR Gate sends approval requests to your Telegram account. You are solely responsible for the handling, storage, and protection of any data processed or logged by ZLAR Gate.

---

## 13. Export Compliance

ZLAR Gate includes cryptographic functionality (Ed25519 signing and verification). You are responsible for compliance with all applicable export control laws and regulations in your jurisdiction.

---

## 14. Governing Law and Jurisdiction

These terms shall be governed by the laws of the Province of Ontario and the federal laws of Canada applicable therein. Disputes are subject to the exclusive jurisdiction of the courts of Ontario, Canada. Parties agree to attempt good-faith resolution for 30 days before initiating legal proceedings.

---

## 15. Severability

If any provision is unenforceable, it will be modified to the minimum extent necessary or severed. Remaining provisions continue in full force.

---

## 16. Entire Agreement

This legal notice, together with the Apache License 2.0, constitutes the entire agreement between you and ZLAR Inc. regarding ZLAR Gate.

---

## 17. Changes to This Notice

ZLAR Inc. reserves the right to modify this legal notice at any time. Changes will be reflected in the repository and on [zlar.ai](https://zlar.ai). Continued use constitutes acceptance.

---

## 18. Contact

**ZLAR Inc.**
Email: [hello@zlar.ai](mailto:hello@zlar.ai)
Web: [zlar.ai](https://zlar.ai)

---

*This legal notice supplements the Apache License 2.0 under which ZLAR Gate is distributed. In the event of any conflict, the terms that provide greater protection to ZLAR Inc. and the ZLAR Parties shall apply to the maximum extent permitted by law.*
