# Security Policy

Revert is a security product: it records and reverses agent actions. That makes the
trustworthiness of this code base the product itself. We take security seriously and
ask that you do too.

## Reporting a vulnerability

**Do not open a public issue for security vulnerabilities.** Report privately to the
core team. For the `revert` repository, GitHub's private vulnerability reporting is
enabled — use it if available. Otherwise, email the core team via a maintainer.

Please include:

- The affected repository, file, and version/commit
- A description of the vulnerability and its impact
- A minimal reproduction if possible

## What happens next

- We acknowledge reports within 72 hours.
- We investigate and release a fix as fast as safely possible.
- We credit researchers in release notes when appropriate (with permission).

## Rules

- Never test against production systems, third-party services, or other people's
  data without explicit permission.
- Never commit secrets, keys, or tokens — in any repository, ever. If you think one
  leaked, rotate it and report it.
- The crown jewel (`revert-enterprise`) is private. If you discover it's exposed,
  that is the highest-priority report.
