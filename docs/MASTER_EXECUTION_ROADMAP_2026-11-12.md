# Master Execution Roadmap — 2026-11-12

## Objective and authority

Commercial readiness means **a real operator can safely accomplish a valuable job in a controlled hosted system**, not merely that a demo boots. No source repository is declared production-ready without exact-head verification, independent negative/security tests, recovery evidence, legal/privacy review and a customer outcome baseline.

**Default:** feature branches, draft PRs, synthetic or rights-cleared test data, no unapproved merges/hosted migrations/sending/publishing/trading. This document sets dependency order and acceptance evidence; it does not authorize release.

## Workstream priority

| Order | System | Immediate deliverable | Completion gate |
|---|---|---|---|
| P0 | Project 6+8 | Reconcile existing Project 8 integration PRs #52 + #53 in a controlled branch | Golden scoring parity, disposable tenant-negative tests, CI exact-head green |
| P0 | GitHub portfolio | Replace outdated project naming and make statuses and product outcomes explicit | Reviewed documentation PR; no unverified live/revenue claims |
| P0 | Sports statistics research | Validate existing manual CSV player logs and rights/provenance; document a strictly offline historical schema | Mixed data rejected, historical splits reproducible, no wagering/odds/staking logic |
| P1 | Distribution Hub | Adopt shot manifest, motion continuity and human signoff standard | One episode passes complete in-sequence picture/audio/caption QA |
| P1 | Project 9 | Freeze strategy and data-source contract; independent chronological holdout with simulated-cost stress | Verified data provenance, no lookahead, holdout report from unseen dates |
| P1 | Project 5 | Resource-isolated worker design, evidence-linked PDF/DOCX verification | No code execution, bounded parsing, PII controls, exact source citations |
| P2 | Project 7 | Independent two-source observations and operator discovery | Grounded data and measurable customer workflow benefit |
| P2 | Commercial pilot | One consenting customer and a baseline | Reviewed access, recovery, support, consent, invoice/legal controls |

## Phase 1 (days 0–5): align and prove existing components

### Project 6 + 8

- Retain **Project 8** as canonical auth/workspace/UI/Supabase boundary. Port only deterministic Project 6 scoring, lifecycle fixtures and outbox semantics.
- Record source SHAs and reconcile **[PR #52](https://github.com/ajlacabe23-2426/Project-8-AI-customer-support/pull/52)** followed by **[PR #53](https://github.com/ajlacabe23-2426/Project-8-AI-customer-support/pull/53)** in a review branch. Never apply production migrations before disposable database verification.
- Add two-owner/two-workspace tests for cases, events, contact data, widget capabilities and any eventual outbox.
- Produce a single customer journey demo: public widget -> knowledge answer/abstain -> handoff -> owner-reviewed lead -> human reply draft.
- Track p50/p90 human response time, lead-review coverage, explicit case resolution and violation counts, each with denominators.

### Portfolio

- Canonical statuses: prototype, verified candidate, private pilot, production. Don't call a repository production because CI is green.
- Ensure profile uses **Axiovela** (not AtlasIQ) and separately shows LeadFlow CX as a *proposed* flagship.
- No fabricated paid usage, deployed endpoints, customer counts or performance claims.

### Sports statistics research only

- Keep manual historical game data offline and rights-clear; no sportsbook or wager interfaces.
- Canonical CSV: `player_id,game_date,team,opponent,home_away,minutes,points,rebounds,assists,source_id`.
- Companion manifest JSON: `schema_version,source_name,retrieved_at,as_of_date,usage_permission,sha256,row_count,units`.
- Validate unique `player_id+game_date`, positive minutes, nonnegative integer counting stats, real ISO dates, strict ordering per player, explicit DNP/missing values (never zero-fill unknown).
- Research outputs: rolling observed means/medians, sample deviations, confidence bands, provenance completeness and chronological consistency checks. Use held-out historical observations for calibration; **no odds ingestion, parlay construction or staking recommendations**.

## Phase 2 (days 6–14): architecture and independent validation

### LeadFlow CX

1. Create case/workspace/event schema and server-side tenant-aware adapter.
2. Implement atomic state transitions with expected version checks; reject duplicate idempotency keys with different payloads.
3. Retain any outbound messaging as a non-executing draft/outbox until consent, retries, suppression, provider sandbox and ambiguous-result reconciliation are reviewed.
4. Verify emergency disable, backup/restore, traceable operator actions, rate limits and prompt injection boundaries.
5. Gate any hosted private pilot on completed privacy/security and operational review.

### Project 9

- Capture point-in-time data provenance, prices/adjustment method, corporate-action checks, source permission and hash.
- Freeze rule version before evaluation; use chronological development/validation/untouched holdout; model data leakage and costs.
- Compare against passive baseline and no-skill baselines with fold-by-fold outcomes, missing data and survivorship warnings.
- Reject all trade execution and performance marketing claims until independently valid (currently local research only).

### Project 5

- Queue parsing jobs in untrusted-document workers with CPU/RAM/time/size/page limits and network isolation.
- Preserve `document_sha256`, field-name, extracted value, start/end source span, parser version, confidence, contradictions and human decision.
- Test malicious/oversized archives, misleading OCR layers, hidden Word changes, prompt injection, embedded objects, cross-tenant access, deletion and retention.
- Report facts with citation provenance; never claim compliance/legal acceptance from extracted wording.

### Project 7

- No integration into flagship decisions until source identity, completeness, contradictions and time alignment are measured against independently checked samples.
- Customer discovery must verify who uses the brief, action taken, time saved and what original decision would have been.

## Phase 3 (days 15–30): controlled pilots

- First private customer workflow for unified Project 6+8 on one approved host, migration/checksum evidence, backup restore drill, rollback/revocation, support escalation, monitoring and privacy reviews.
- Project 5: customer-relevant agreement comparison in isolated worker with reviewer acceptance and verified citations.
- Media: one complete episode released only after QA and human approval; capture actual watch-through/retention rather than promising virality.
- Project 9 and sports research: continue historical evaluation; do not equate retrospective code checks with future validity.

## Broadcast and animation engineering

- Every shot has asset ID, frozen character/voice reference, lens/framing, camera velocity vector, subject screen-direction, beginning/end pose, soundtrack elements and final render URL/hash.
- Generation prompts must continue the exact final frame, pose, direction, subject speed and camera velocity of the approved preceding shot. Reject zero-velocity restarts and morphing.
- At edit: match gesture/action phase and 180-degree screen geography; use J/L audio cuts, layered room tone/foley/ambience and restrained score.
- Use optical flow only to retime coherent continuous motion; do **not** use it to hide unmatching character shots. Review interpolation artifacts at full resolution.
- Run final video `ffprobe`, blackdetect, freezedetect, audio EBU loudness/true peak report, subtitles check, phone speaker/headphone playback and approval packet.
- Internal social audio target around -16 LUFS / <= -1 dBTP; broadcast contracts may require -23 LUFS EBU R128. These are different delivery profiles.
- Stop if any character identity drift, clipped narration, missing license, multi-second unintended freeze, corrupted render, blocked mobile playback or no human approval.

## Engineering release packet, required on each candidate

```yaml
product: LeadFlow CX
release_status: review_candidate
source_commit_sha: REQUIRED
pr_urls: []
ci_pass: false
tenant_negative_tests: pending
data_provenance: pending
security_review: pending
backup_restore_drill: pending
hosted_browser_acceptance: pending
privacy_and_consent_review: pending
customer_baseline: pending
known_defects: []
approver: null
production_approved: false
```

**Hard stop:** any one missing required field keeps the release at NO-GO. Never infer success from a generated report alone.

## Execution success metrics

- Engineering: exact-head CI pass ratio, escaped critical defects, median time to reproduce/resolve incidents, zero unauthorized cross-tenant disclosures.
- Commercial: customer-verified hours saved, response time distribution, support quality, qualified follow-up completeness, paid conversion only after verified measurement.
- Data: provenance coverage %, missingness by field, calibration against historical holdouts, independent source agreement.
- Media: technical export pass rate, creative reviewer approval, corrected continuity defect count, accessible caption quality, actual platform retention after posting.

## Active execution links

- [Profile refresh PR](https://github.com/ajlacabe23-2426/ajlacabe23-2426/pull/1)
- [Flagship consolidation acceptance PR](https://github.com/ajlacabe23-2426/Project-8-AI-customer-support/pull/54)
- [Broadcast production standard PR](https://github.com/ajlacabe23-2426/portfolio-distribution-hub/pull/26)

These are documents awaiting review — not evidence that code integration or commercial acceptance has completed.
