<div align="center">

    ┌─┐        • ← commit
    │ │        │
    │ │   ┌────┘
    │ │   │
    └─┼───┘     ← the branch returns
      │
      •
revert - every action is a commit

# Revert Labs

### git for AI agent actions — every action is a commit, anything can be rolled back.

**Agents are probabilistic. They will do something *plausible but wrong* — delete the
wrong row, email the wrong person, approve the wrong invoice. You can't make them
perfect. You make failure survivable.**

</div>

---

## What we build

| Repo | What it is |
|---|---|
| [`revert`](https://github.com/revert-labs/revert) | **The open core** (Apache-2.0). An event-sourced action ledger + undo engine for AI agents. SDK, CLI, docs, tests — zero dependencies. |
| `revert-enterprise` | **The control plane** (private). Cross-service compensation, compliance exports, timelines. The crown jewel. |
| `.github` | This org: community health files, team charter, branding. |

## The idea in one diagram

```
agent ──► [ tool call ] ──► SDK records: payload · before-image · idempotency key
                                  │
                                  ▼
                          action ledger (immutable events)
                                  │
                       undo engine (tiers 1–5, verify-by-read-back)
                                  │
                                  ▼
                    the outside world — now reversible
```

## Why it matters

85% reliability per step × 10 steps ≈ 20% end-to-end. Making agents 90% reliable still
fails 65% of 10-step workflows. **The fix isn't better agents — it's survivable
failure.** Revert is the undo button that makes autonomous agents safe to deploy.

## Status

- 🛠️ **v0.1 — SDK MVP** in progress ([roadmap board](https://github.com/orgs/revert-labs/projects/1))
- 🧪 Research-backed: replay-or-fork restore, compensation tiers, ACRFence defense
- 🤝 Open core, teaching-first culture

## Get involved

- **Contribute:** read [`CONTRIBUTING.md`](https://github.com/revert-labs/.github/blob/main/CONTRIBUTING.md) — PR-driven, small commits, tests with everything
- **Learn:** our [`learning path`](https://github.com/revert-labs/revert/blob/main/docs/learning-path.md) maps every concept to the code
- **Ask:** no question is too basic — the whole company is learning

---

<div align="center">

*Revert Labs — ship agents fearlessly. Every action is a commit; anything can be rolled back.*

</div>
