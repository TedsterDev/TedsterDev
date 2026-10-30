# Teddy Williams

Firmware engineer at CalAmp, building embedded C/C++ for connected-vehicle and IoT devices, with a background in security operations and secure cloud development. I build security tooling and guardrails for AI agents.

## Selected projects

The source for these is private (see below). I am happy to walk through the code on request.

- **Guardrail policy engine for Claude Code.** A Python hook that auto-approves routine agent actions and asks or blocks on risky ones: destructive SQL, TLS downgrades, shell tracing of secret-bearing scripts, lowered test-coverage thresholds, and edits to its own rules. It fails closed, and it is tested against recorded real incidents, each paired with near-miss cases that must not trigger, under a 100% line and branch coverage gate.
- **LLM safety benchmark and local model harness.** An assertion-based benchmark (dangerous-command refusal, credential handling, hallucinated platform facts, security guidance) that runs against local open-weight models or Claude through the Anthropic API. Model-proposed commands pass a dangerous-command blocker, and a redaction layer scrubs keys and identifiers before output returns to the model.
- **Airlock, an isolated malware-triage sandbox.** Static analysis of untrusted files inside a disposable, network-isolated virtual machine, with custom YARA rules and an offline threat-intelligence mirror so default lookups send no traffic. A file it cannot open is reported "unknown," never "clean."
- **Security dashboard and PDF malware analyzer.** A passkey-only dashboard with read-only cloud posture audits and a hash-chained audit log, plus static malicious-PDF triage that never executes document scripts.
- **Reverse engineering.** Binary patching with ARM assembly hooks, emulator-driven testing, and file-format analysis cross-checked against an independent implementation.

## Why the source is private

Some of these are live services that handle sensitive data. Now that AI can find vulnerabilities in public code far faster than before, I keep their source private to limit the attack surface.

## Contact

[LinkedIn](https://www.linkedin.com/in/teddy-williams/)
