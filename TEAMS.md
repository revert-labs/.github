# Revert Labs — team plan

This is the org's team charter. It answers: who's on what team, what each team can do,
and when the structure changes. Review it whenever the org grows or the access
boundaries shift.

## The rule

> **One team per access boundary.** Teams exist for access control, not titles.
> If two people should have the same access, they're the same team.

## Current structure (v2 — flat, equal access)

Every member gets the same access: **write on every repo**. The git dev flow works
the same for everyone — push a branch, open a PR, review and get reviewed. No member
sits at read-only.

| Team | Members | Access | Why it exists |
|---|---|---|---|
| **Core** | founders (org owners) | admin on every repo | Owns the org itself: settings, the meta repo, and the merge controls. The smallest possible group — administration, not development. |
| **Dev** | **every member** (current + new members) | write (push) on every repo, incl. `revert-enterprise` | The builders. Equal write for everyone — that's the point. PRs, issues, docs, tests. |
| **Bots** | automation identities (`revert-bot`, CI) | least privilege needed per workflow | The exception to the two-member rule: machines, not people. A bot gets exactly the permissions its workflow needs — never human-level access. |

Access summary (all repos, identical):

```
revert (public, Apache-2.0)          → Core: admin · Dev: push
revert-enterprise (private)          → Core: admin · Dev: push
revert-labs/.github (meta)           → Core: admin · Dev: push
revert-labs.github.io (org site)     → Core: admin · Dev: push
```

Membership is one flat default: **joining the org = joining Dev = write everywhere.**
There is no "read-only member" tier. New members are invited with Dev attached, so the
moment they accept they can push branches and open PRs.

## Joining a team

- **Dev:** automatic — every member is Dev. No ceremony.
- **Core:** founder decision only. Being in Core means being trusted with the org's
  settings and merge controls, not more code access (Dev already has that).

## Learning structure (we're a learning team)

- Every PR gets a **teaching review** — feedback with reasoning, not just approval.
- **Good-first-issues** are the homework: small, scoped, acceptance criteria included.
- **ADRs** are the textbook: read one before writing code; write one for big decisions.
- Questions live in **Discussions**; no question is too basic.
- Full map: `docs/learning-path.md` in the `revert` repo.

## When to add teams (growth triggers)

Add a team only when a real boundary appears. With the flat model, the natural next
boundaries are:

1. **Enterprise** — the day `revert-enterprise` needs a *tighter* boundary than the
   rest of the org (e.g., hired engineers who write open core but not the control
   plane). Split `enterprise` off from Dev then; until that day, everyone writes.
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
