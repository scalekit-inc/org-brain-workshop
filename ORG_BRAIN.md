# Org Brain — org-brain-workshop

Discovered from the repo's own closed-issue and PR history (27 closed issues, 14 merged PRs). Verified against real fetched data, not assumed.

## Ownership by area

| Area | Owner |
|---|---|
| `area:auth` | `owner:alex-chen` |
| `area:billing` | `owner:priya-nair` |
| `area:frontend` | `owner:sam-osei` |
| `area:infra` | `owner:jordan-lee` |

Confirmed: every closed `area:auth` issue sampled carries `owner:alex-chen` with no exceptions.

## Severity

- `P0` = either (a) a real security/credential exposure, or (b) a genuine availability incident (e.g. DB connection pool exhaustion) — P0 does **not** by itself imply a security review, see below.
- `P1` = real bug, real impact, not urgent enough to drop everything.
- `P2` = cosmetic, copy, or low-impact.

## `needs-security-review` trigger — cross-area, topic-based, not area-based

Attached whenever an issue involves tokens, credentials, secrets, API keys, session/cookie security, or webhook signature verification — **regardless of which area the issue is filed under**. Confirmed: this label appears on `area:billing` issue #13 ("Stripe webhook signature verification skipped in staging"), not just `area:auth` issues. Do not gate this label on area — gate it on topic.

## Closing comment convention

Every real fix closes with exactly three lines:
```
Root cause: <one line>
Fix: <one line>
Verified via: <one line>
```

## Duplicate convention

`Duplicate of #<N> - closing in favor of the earlier report.` plus the `duplicate` label.

## PR / merge convention

- Title: `[area] <short description> (Closes #N[, #M...])`
- Body includes a checklist: tests added, changelog updated, verified in staging.
- An approval comment posted before merge: `Approved by owner:<area-owner> - LGTM, merging via squash.`
- Always squash merge.
- **Known gap, don't assume this works:** closing keywords in the PR title/body did not reliably auto-close the linked issue in this repo's history — issue state must be verified (and closed manually if needed) after merge, not assumed from the PR merge alone.
