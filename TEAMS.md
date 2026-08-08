# Revert Labs — team plan

This is the org's team charter. It answers: who's on what team, what each team can do,
and when the structure changes. Review it whenever the org grows or the access
boundaries shift.

## The rule

> **One team per access boundary.** Teams exist for access control, not titles.
> If two people should have the same access, they're the same team.

## Current structure (v1 — startup)

| Team | Members | Access | Why it exists |
|---|---|---|---|
| **Core** | founders (org owners) | admin on every repo, incl. `revert-enterprise` | Owns the vision, the open/closed boundary, and the crown jewel. Smallest possible group — the crown jewel is core-only by design. |
| **Dev** | everyone building (current + new members) | write (push) on `revert` (open core) | The builders. PRs, issues, docs, tests. |
| **Bots** | automation identities (`revert-bot`, CI) | least privilege needed per workflow | The exception to the two-member rule: machines, not people. A bot gets exactly the permissions its workflow needs — never human-level access. |

Access summary:

```
revert (public, Apache-2.0)      → Core: admin · Dev: push · everyone else: read
revert-enterprise (private)      → Core: admin · nobody else
revert-labs/.github (meta)       → Core: admin · Dev: push
```

## Joining a team

- **Dev:** ask a core member. No ceremony — the bar is "wants to build and will
  follow the PR flow" (see `CONTRIBUTING.md`).
- **Core:** founder decision only. Being in Core means being trusted with the crown
  jewel and the company's access model.

## Learning structure (we're a learning team)

- Every PR gets a **teaching review** — feedback with reasoning, not just approval.
- **Good-first-issues** are the homework: small, scoped, acceptance criteria included.
- **ADRs** are the textbook: read one before writing code; write one for big decisions.
- Questions live in **Discussions**; no question is too basic.
- Full map: `docs/learning-path.md` in the `revert` repo.

## When to add teams (growth triggers)

Add a team only when a real boundary appears. Candidate splits, in order of likelihood:

1. **Enterprise** — the day a non-core member needs write access to
   `revert-enterprise` (e.g., a hired engineer for the control plane). Create
   `enterprise` with maintain access; Core stays admin.
2. **Research** — when 3+ people work on compensation correctness/ADRs full-time and
   need a review lane separate from product work.
3. **Security / Platform** — when there's a dedicated security or infra role with
   different access needs (e.g., secret handling, CI runners).
4. **Reviewers** — only if review load becomes a bottleneck (unlikely before ~10
   builders; prefer rotating reviews over a separate team).

Trigger threshold: a proposed team needs at least **2 members with a distinct access
need**. One person wanting a title is not a team — it's a vanity rename.

## Change process

- Team changes (create/rename/delete) go through Core and are recorded here.
- Permission changes follow the same PR-driven review as code.
- If this file feels too big, the org has outgrown it — that's a good problem; re-plan
  it in a PR.
