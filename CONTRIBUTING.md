# Contributing to Revert Labs

Thanks for wanting to build this with us. The short version: **PR-driven, small
commits, tests with every change, zero new dependencies without discussion.**

## How to contribute

1. **Pick or open an issue.** Every PR should reference one. If you're unsure where
   to start, look for `good first issue`.
2. **Fork or branch.** Branch names: `feat/`, `fix/`, `docs/`, `chore/` + a short
   slug.
3. **Write the code + the test.** `node --test` must pass before you open the PR.
4. **Open the PR** with the template filled in: what, why, how it was verified.
5. **Review cycle.** A core-team member reviews; address feedback; squash on merge.

## Rules of the road

- **Conventional commits** (`feat:`, `fix:`, `docs:`, `test:`, `refactor:`,
  `chore:`). One logical change per commit. Never push directly to `main`.
- **No dependencies by default.** This project is deliberately zero-dependency.
  Argue for any addition in the PR.
- **No secrets.** Keys, tokens, credentials: never in code, commits, or logs.
- **The boundary is structural.** Anything that belongs to the enterprise layer
  (cross-service compensation, compliance exports, hosted control plane) lives in
  the private `revert-enterprise` repo. Do not commit it to the open core.

## Teams

- **Core** — vision, the open/closed boundary, the crown jewel
- **Dev** — the SDK and ledger
- **Research** — compensation correctness, ADRs
- **Infra / Ops / Sec / PR** — platform, deployments, security, community

If you're an org member and want to join a team, ask a core-team member.

## Style

Follow the conventions in each repo's `AGENTS.md`. Be kind, be precise, and remember
what we build: trust. The history of this org should be as clean as the ledgers we
sell.
