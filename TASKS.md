# Financial-Literacy-Open — TASKS.md

> Status: Draft · Version: 0.1.0 · Last updated: 2026-06-28 · Owner: TBD (maintainer) · Lane: donated

Backlog for **Financial-Literacy-Open** (slug: `financial-literacy-open`): an openly-licensed,
plain-language, **product-neutral** curriculum + privacy-preserving toolkit teaching budgeting,
saving, and debt basics — **education, not financial advice**. See `PLAN.md` for full context.

The **editorial / product-neutrality / not-advice policy charter + linter is the first build item**
and a hard product requirement. This is a **MEDIUM risk-tier** project: any task stating a financial
fact, figure, or rule requires **credentialed financial-educator sign-off** (AFC® or equivalent)
before it ships. No delivery partner or credentialed reviewer is yet secured, so delivery- and
content-dependent tasks carry `requestor: TO BE SECURED` and `verifiedNeed: false`.

## How these tasks map to Hee-Lee Oss

Each task below becomes a Hee-Lee Oss **Task JSON** validated against `packages/schema/src/schemas.ts`.
Field mapping:

- **id** — stable slug `financial-literacy-open-<area>-NNN` (e.g. `financial-literacy-open-policy-001`).
- **title** — the task title in the milestone table.
- **project** — `financial-literacy-open`.
- **type** — one of `code | research | writing | data | design-spec | maintenance`.
- **lane** — `donated` (default; no funded tasks planned. Any `funded` task must add
  `fundedBudgetUsd` with a hard cap — e.g., a future funded reviewer-hours lane).
- **priority** — `high | medium | low`.
- **domain** — array, e.g. `["education","financial-literacy","oer","accessibility"]`.
- **riskTier** — `low | medium | high`. Anything stating a financial fact/figure/rule is `medium`;
  pure pipeline/site/tooling is `low`; nothing here is `high` (individualized/investment/tax/legal
  advice is out of scope — it would be `high`).
- **urgent** — boolean (no urgent tasks at cold-start).
- **deliverable** — `pr | dataset | document | translation`.
- **tokenEstimate** — `small | medium | large` (maps to the Size column).
- **status** — `open | in-progress | review | delivered | done` (all start `open`).
- **context / objective / acceptanceCriteria[] / resources[] / output** — per task.
- **requestor** — partner/steward/reviewer; `TO BE SECURED` where unknown.
- **verifiedNeed** — `true` only once a specific partner/need is confirmed; currently `false`
  everywhere (no partner secured).
- **outputLicense** — code: **MIT**; content/data/curriculum/glossary/worksheets: **CC-BY-4.0**
  (or **CC-BY-SA-4.0** where inherited from a share-alike source); docs: **CC-BY-4.0**.

Size legend: small ≈ tokenEstimate `small`, med ≈ `medium`, large ≈ `large`.
Reviewer "Expert (fin-ed)" = credentialed financial educator (AFC® or equivalent / nonprofit credit
counselor), **TO BE SECURED**; "Neutrality reviewer" = product-neutrality / not-advice auditor;
"PL/a11y reviewer" = plain-language + accessibility reviewer.

---

## Milestone M0 — Editorial policy, pipeline & linter (cold-start)

| ID | Title | Type | Size | Risk | Deliverable | Depends on | Reviewer |
|---|---|---|---|---|---|---|---|
| financial-literacy-open-policy-001 | Editorial / product-neutrality / not-advice policy charter (refused-use set, non-commercial redirect, non-shaming, jurisdiction-honesty) | design-spec | medium | medium | document | — | Expert (fin-ed) + Neutrality reviewer |
| financial-literacy-open-repo-002 | Monorepo + pnpm + TS/ESM + static-site toolchain + CI (build/test/lint) skeleton | code | small | low | pr | — | Maintainer |
| financial-literacy-open-linter-003 | Product-neutrality + not-advice linter (brand/affiliate/ticker/advice-phrasing/unflagged-jurisdiction + non-shaming flags) wired into CI | code | medium | medium | pr | 001, 002 | Neutrality reviewer + Maintainer |
| financial-literacy-open-schema-004 | Content/lesson + glossary JSON Schema (sources[], reviewer sign-off, lastVerified/validUntil, jurisdiction, license) | code | small | low | pr | 002 | Maintainer |
| financial-literacy-open-scope-005 | Launch jurisdiction-scope decision (neutral core confirmed; overlay criteria + deadline) | research | small | medium | document | — | Maintainer + Expert (fin-ed) |

**Acceptance criteria — key tasks**

- **financial-literacy-open-policy-001** (policy charter)
  - Enumerates the **refused-use set** in concrete, testable terms: individualized financial advice
    ("what should *I* do with my money"); investment/securities/crypto/forex/retirement-allocation
    advice and ticker/fund picks; naming/ranking specific products, brands, or institutions;
    affiliate/referral/lead-gen/sponsored content; tax/legal/accounting/insurance/bankruptcy advice;
    get-rich-quick / day-trading / MLM / gambling / "credit-repair" / debt-settlement schemes;
    collecting users' personal financial data.
  - Defines the allowed **educational** categories and the **education-vs-advice line** in plain terms.
  - Mandates the **non-commercial redirect** on refusals (free nonprofit counselor / public
    consumer-finance agency + relevant lesson — never a product) and the persistent **"educational,
    not financial advice"** framing.
  - Defines the **non-shaming / structurally-honest** editorial rules (no blame/moralizing of poverty
    or debt; never imply hardship is a personal failing; route distress to free help).
  - Defines the **jurisdiction-honesty** rule (neutral core; figures as labeled examples;
    country-specifics only in a labeled, locally-reviewed overlay).
  - Reviewed and signed off by a credentialed financial educator + the neutrality reviewer (recorded).

- **financial-literacy-open-linter-003** (product-neutrality + not-advice linter)
  - Detects and **fails CI** on: product/brand/institution names (curated denylist + heuristics),
    ticker symbols, affiliate/referral URL + UTM/lead-gen patterns, advice phrasing ("you should
    buy/invest/choose," "the best card/bank/broker is"), and guaranteed-return claims.
  - Flags **unflagged jurisdiction-specific terms** ("credit score," "401(k)," "ISA," etc.) outside a
    labeled overlay.
  - Emits **non-shaming heuristics** flags (blame/moralizing phrasing) for human review.
  - Verifies presence of the **not-advice framing** + a **non-commercial redirect** on relevant
    surfaces; a missing/incorrect redirect is a failure.
  - Runs in CI; documented; denylist/patterns versioned and extensible.

- **financial-literacy-open-schema-004** (content schema)
  - Frontmatter schema requires `sources[]` (citation, URL, license/legal-status, `lastVerified`,
    `validUntil`), `reviewer` + `reviewedVersion` + `signoffDate`, `jurisdiction`
    (`"neutral"`|ISO code), `readingLevel`, `plainLanguageChecked`, `a11yChecked`, `license`,
    `notAdviceFraming: true`.
  - A claim without a source, or a lesson without a current-version sign-off, **fails validation**.

- **financial-literacy-open-scope-005** (jurisdiction-scope decision)
  - Confirms **jurisdiction-neutral core** as the launch scope; records the criteria for choosing the
    first overlay (open-source availability, local reviewer, underserved audience, tractable
    complexity) and the M0 decision deadline.
  - The specific overlay jurisdiction remains `TO BE SECURED`; the rule + deadline are fixed.

**M0 Definition of Done:** editorial/product-neutrality/not-advice **policy charter**
(expert + neutrality reviewed) merged; **linter** wired into CI and failing the build on violations;
TS/ESM + static-site skeleton + green CI; content/glossary **JSON Schema** with provenance/staleness
fields; "educational, not advice" framing + non-commercial-redirect pattern wired in;
**jurisdiction-scope decision** recorded. *(Credentialed-reviewer engagement targeted by 2026-09-30
gates M1 content.)*

---

## Milestone M1 — Budgeting module + provenance proof (first reviewed content)

| ID | Title | Type | Size | Risk | Deliverable | Depends on | Reviewer |
|---|---|---|---|---|---|---|---|
| financial-literacy-open-sources-006 | Source vetting: verify reuse terms + record provenance for budgeting sources | data | medium | medium | dataset | 004, 005 | Expert (fin-ed) + Maintainer |
| financial-literacy-open-content-007 | Budgeting-basics module (cited, plain-language, accessible, neutral, expert-signed-off) | writing | large | medium | document | 001, 003, 006 | Expert (fin-ed) + PL/a11y reviewer |
| financial-literacy-open-glossary-008 | Glossary v1 (budgeting terms; cited, jurisdiction-flagged) | writing | small | medium | document | 006 | Expert (fin-ed) |
| financial-literacy-open-staleness-009 | Provenance + citation-coverage + staleness fail-safe enforcement | code | medium | medium | pr | 004, 006 | Maintainer |

**Acceptance criteria — key tasks**

- **financial-literacy-open-sources-006** (source vetting)
  - Reuse terms verified + recorded per source (public-domain / CC; no all-rights-reserved commercial
    finance content; no commercial rate/product/comparison data).
  - Provenance recorded (source, publisher, jurisdiction, citation, URL, retrieval date,
    license/legal-status, `lastVerified`, `validUntil`); CC-BY-SA sources tagged for inheritance.
  - Expert sign-off recorded before sources are enabled.

- **financial-literacy-open-content-007** (budgeting module)
  - All factual/numeric claims **cited**; numbers shown as **labeled illustrative examples** (never
    recommendations/benchmarks); currency shown neutrally.
  - **Linter-clean** (no product/brand/affiliate/advice phrasing; no unflagged jurisdiction terms);
    persistent **not-advice framing** + non-commercial redirect present.
  - Meets readability target (≤ grade 8; grade 6 for foundational) and WCAG 2.2 AA; plain-language
    review passed.
  - **Credentialed financial-educator sign-off recorded** for the shipped version.

- **financial-literacy-open-staleness-009** (provenance + staleness)
  - No claim surfaces without an attached `Source` (citation-coverage check).
  - A claim past `validUntil` is **auto-flagged or withheld** until re-verified and **re-signed-off**;
    staleness test asserts no time-sensitive figure serves as current past its window.

**M1 Definition of Done:** the **Budgeting-basics** module shipped end-to-end — cited, plain-language,
accessible, linter-clean, and **expert-signed-off** — with provenance + citation-coverage + staleness
fail-safe working on real sources and a glossary v1. **Kill-gate:** if no credentialed reviewer is
engaged, M1 content does not start (project holds at M0).

---

## Milestone M2 — Core curriculum (Saving, Debt, Banking, Scams)

| ID | Title | Type | Size | Risk | Deliverable | Depends on | Reviewer |
|---|---|---|---|---|---|---|---|
| financial-literacy-open-content-010 | Saving-basics module (emergency-buffer concept; cited, expert-signed-off) | writing | medium | medium | document | 007, 009 | Expert (fin-ed) + PL/a11y reviewer |
| financial-literacy-open-content-011 | Debt-basics module (interest/principal/compounding/prioritization/cost of borrowing) | writing | large | medium | document | 007, 009 | Expert (fin-ed) + PL/a11y reviewer |
| financial-literacy-open-content-012 | Banking/accounts-basics module (generic, product-neutral) | writing | medium | medium | document | 007, 009 | Expert (fin-ed) + Neutrality reviewer |
| financial-literacy-open-content-013 | Recognizing scams & predatory products module (recognize + verify; names no brands) | writing | medium | medium | document | 007, 009 | Expert (fin-ed) + Neutrality reviewer |

**Acceptance criteria — key tasks**

- **financial-literacy-open-content-011** (debt-basics module)
  - Explains interest, principal, compounding, and prioritization with **labeled illustrative**
    examples; never recommends a specific loan/product or "good debt" purchase.
  - Cited, linter-clean, plain-language, accessible; not-advice framing + non-commercial redirect.
  - Expert sign-off recorded; debt-distress content routes to **free nonprofit** counseling, never a
    debt-settlement/"credit-repair" service.

- **financial-literacy-open-content-013** (scams & predatory products)
  - Teaches red flags **and verification steps** (how to check a claim/entity via public/nonprofit
    sources), not just recognition.
  - **Names no specific brands/products**; describes *categories* and tactics (payday/rent-to-own/MLM/
    "credit-repair"/advance-fee) neutrally; cited; expert + neutrality sign-off.

**M2 Definition of Done:** Saving, Debt, Banking-basics, and Recognizing-scams modules shipped to the
M1 bar (cited, plain-language, accessible, linter-clean, expert-signed-off); glossary expanded; all
numbers labeled illustrative; non-commercial-redirect coverage verified across modules.

---

## Milestone M3 — Privacy-preserving tools & printables

| ID | Title | Type | Size | Risk | Deliverable | Depends on | Reviewer |
|---|---|---|---|---|---|---|---|
| financial-literacy-open-tools-014 | Client-side-only calculators (budget worksheet, debt-payoff illustrator, savings-goal) + no-data-egress test | code | large | medium | pr | 003, 010, 011 | Maintainer + Neutrality reviewer |
| financial-literacy-open-print-015 | Printable worksheets / one-pagers (offline, B/W + screen-reader friendly) | design-spec | small | low | document | 007, 010, 011 | PL/a11y reviewer |

**Acceptance criteria — key tasks**

- **financial-literacy-open-tools-014** (privacy-preserving calculators)
  - All computation is **client-side**; **no financial input is transmitted or persisted
    server-side**; no analytics on inputs. Optional "save my numbers" is **local-device-only, opt-in,
    never uploaded**.
  - A **no-data-egress test** (network + storage) passes for each tool as a release gate.
  - Each tool carries not-advice framing + an "illustration, not a recommendation" label; debt-payoff
    illustrator shows methods (e.g., snowball vs. avalanche) as illustration, not advice; linter-clean.

- **financial-literacy-open-print-015** (printables)
  - Worksheets render from the same source; usable in black-and-white; screen-reader/tagged-PDF
    friendly; carry not-advice framing; no brand/product content (linter-clean).

**M3 Definition of Done:** the three calculators shipped **client-side-only** with passing
no-data-egress/no-PII tests and not-advice/illustration framing; accessible, offline-friendly
printables available.

---

## Milestone M4 — i18n, accessibility hardening & QA/eval; pilot readiness

| ID | Title | Type | Size | Risk | Deliverable | Depends on | Reviewer |
|---|---|---|---|---|---|---|---|
| financial-literacy-open-i18n-016 | i18n: externalize strings + translate core curriculum into ≥ 2 pilot languages (each language-reviewed) | translation | large | medium | translation | 010, 011, 012, 013 | Expert (fin-ed) + per-language reviewer |
| financial-literacy-open-qa-017 | QA/eval suite + pilot readiness: linter + citation-coverage + staleness + WCAG 2.2 AA + readability + anonymous pre/post instrument + facilitation runbook | code | medium | medium | pr | 003, 009, 014 | Maintainer + PL/a11y reviewer |

**Acceptance criteria — key tasks**

- **financial-literacy-open-i18n-016** (translation)
  - Strings externalized; core curriculum translated into ≥ 2 pilot languages; each translation
    **reviewed by a language reviewer** (and a financial-educator for accuracy); translations
    inherit CC-BY (or CC-BY-SA where applicable); translators credited.

- **financial-literacy-open-qa-017** (QA/eval + pilot readiness)
  - Full QA suite (product-neutrality linter, citation coverage, staleness, WCAG 2.2 AA, readability)
    runs green in CI.
  - **Anonymous, no-PII** pre/post comprehension instrument + money-action survey built and
    partner-administrable; facilitation runbook written.

**M4 Definition of Done:** core curriculum available in ≥ 2 language-reviewed languages; WCAG 2.2 AA
+ readability targets met; full QA suite green; anonymous pre/post instrument + facilitation runbook
ready — the curriculum is pilot-ready.

---

## Milestone M5 — Partner delivery & measured outcomes (the deed)

| ID | Title | Type | Size | Risk | Deliverable | Depends on | Reviewer |
|---|---|---|---|---|---|---|---|
| financial-literacy-open-pilot-018 | Secure delivery partner + steward; deliver to real learners; record anonymous outcomes (comprehension gain + money actions) | maintenance | medium | medium | document | 016, 017 | Steward + Expert (fin-ed) |

**Acceptance criteria — financial-literacy-open-pilot-018**
- A real delivery partner (library/adult-ed/community-college/nonprofit-counseling/CDFI/resettlement)
  is secured; steward assigned; `verifiedNeed` flips to `true`.
- Curriculum delivered to real learners; **anonymous, aggregate** pre/post shows the comprehension-gain
  target and **≥ 20 learners report ≥ 1 concrete money action**; content expert-signed-off,
  linter-clean, accessible, privacy-preserving; outcomes recorded (no PII).
- Driven by the **dated plan** (partners in conversation by 2026-08-31, reviewer by 2026-09-30, partner
  by 2026-12-31). **Fallback:** if no partner by **~2027-03-31**, **release the reviewed curriculum to
  an OER commons** as a standing public good and continue outreach for the measured pilot — recorded
  in governance.

**M5 Definition of Done:** project-level **Definition of Shipped** met — real learners reached via a
secured partner **demonstrably improve** (comprehension gain + ≥ 1 money action), using cited,
expert-signed-off, product-neutral, accessible, privacy-preserving content, with anonymous outcomes
recorded. *(Gated on a secured partner — TO BE SECURED.)*

---

## Milestone M6 — Sustain, review cadence & expansion (post-delivery)

| ID | Title | Type | Size | Risk | Deliverable | Depends on | Reviewer |
|---|---|---|---|---|---|---|---|
| financial-literacy-open-ops-019 | Ops runbook + outcomes dashboard (aggregate/anonymous) + maintenance rotation + content review cadence | maintenance | medium | medium | document | 018 | Maintainer + Steward |

**Acceptance criteria — financial-literacy-open-ops-019**
- Runbook covers build/deploy, source re-verification, linter/denylist updates, and partner support.
- Dashboard tracks comprehension gain, money-action counts, reviewer/linter status (not engagement
  vanity metrics); all aggregate and anonymous.
- Named maintenance rotation; **content review cadence** (figures re-verified on schedule; re-sign-off
  on change) defined; documented, **reviewer-gated** process for adding a jurisdiction overlay or a
  new language.

**M6 Definition of Done:** project sustainably maintained with anonymous outcomes tracked, a rotation
owning it, a runtime-enforced review cadence for financial figures, and a reviewer-gated expansion
process.

---

## Backlog / future

| ID | Title | Type | Size | Risk | Deliverable | Notes |
|---|---|---|---|---|---|---|
| financial-literacy-open-overlay-020 | First jurisdiction overlay (credit reporting / account types / consumer rights) | data | large | medium | dataset | Only with a local credentialed reviewer; labeled overlay; full source-vetting |
| financial-literacy-open-content-021 | Extended modules (income basics, insurance concepts, planning concepts) — all neutral, non-advice | writing | large | medium | document | Stay out of investment/tax/legal advice; expert-signed-off |
| financial-literacy-open-audio-022 | Read-aloud audio narration of core lessons (low-literacy access) | data | medium | low | dataset | Text-aligned; accessibility benefit |
| financial-literacy-open-assistant-023 | Gated live learner-facing Q&A assistant (full guardrail port) | code | large | high | pr | Backlog only; would require runtime guardrail layer + higher safety bar; governance decision |
| financial-literacy-open-funded-024 | Funded reviewer-hours lane (hard budget cap) for credentialed review | maintenance | small | medium | document | Funded lane; requires `fundedBudgetUsd`; must not compromise reviewer independence |

---

## Generated task index

> Auto-generated by Hee-Lee Oss task-decomposition agent on 2026-06-29. All 24 tasks validated
> against the Hee-Lee Oss taskSchema (exit 0). Pre-existing seed file kept as-is.

| File | ID | Milestone | Type | Priority | Risk | Lane |
|---|---|---|---|---|---|---|
| tasks/financial-literacy-open-policy-001.json | financial-literacy-open-policy-001 | M0 | design-spec | high | medium | donated |
| tasks/financial-literacy-open-repo-002.json | financial-literacy-open-repo-002 | M0 | code | high | low | donated |
| tasks/financial-literacy-open-linter-003.json | financial-literacy-open-linter-003 | M0 | code | high | medium | donated |
| tasks/financial-literacy-open-schema-004.json | financial-literacy-open-schema-004 | M0 | code | high | low | donated |
| tasks/financial-literacy-open-scope-005.json | financial-literacy-open-scope-005 | M0 | research | medium | medium | donated |
| tasks/financial-literacy-open-sources-006.json | financial-literacy-open-sources-006 | M1 | data | high | medium | donated |
| tasks/financial-literacy-open-content-007.json | financial-literacy-open-content-007 | M1 | writing | high | medium | donated |
| tasks/financial-literacy-open-glossary-008.json | financial-literacy-open-glossary-008 | M1 | writing | medium | medium | donated |
| tasks/financial-literacy-open-staleness-009.json | financial-literacy-open-staleness-009 | M1 | code | high | medium | donated |
| tasks/financial-literacy-open-content-010.json | financial-literacy-open-content-010 | M2 | writing | medium | medium | donated |
| tasks/financial-literacy-open-content-011.json | financial-literacy-open-content-011 | M2 | writing | medium | medium | donated |
| tasks/financial-literacy-open-content-012.json | financial-literacy-open-content-012 | M2 | writing | medium | medium | donated |
| tasks/financial-literacy-open-content-013.json | financial-literacy-open-content-013 | M2 | writing | medium | medium | donated |
| tasks/financial-literacy-open-tools-014.json | financial-literacy-open-tools-014 | M3 | code | medium | medium | donated |
| tasks/financial-literacy-open-print-015.json | financial-literacy-open-print-015 | M3 | design-spec | medium | low | donated |
| tasks/financial-literacy-open-i18n-016.json | financial-literacy-open-i18n-016 | M4 | writing | medium | medium | donated |
| tasks/financial-literacy-open-qa-017.json | financial-literacy-open-qa-017 | M4 | code | medium | medium | donated |
| tasks/financial-literacy-open-pilot-018.json | financial-literacy-open-pilot-018 | M5 | maintenance | high | medium | donated |
| tasks/financial-literacy-open-ops-019.json | financial-literacy-open-ops-019 | M6 | maintenance | medium | medium | donated |
| tasks/financial-literacy-open-overlay-020.json | financial-literacy-open-overlay-020 | Backlog | data | low | medium | donated |
| tasks/financial-literacy-open-content-021.json | financial-literacy-open-content-021 | Backlog | writing | low | medium | donated |
| tasks/financial-literacy-open-audio-022.json | financial-literacy-open-audio-022 | Backlog | data | low | low | donated |
| tasks/financial-literacy-open-assistant-023.json | financial-literacy-open-assistant-023 | Backlog | code | low | high | donated |
| tasks/financial-literacy-open-funded-024.json | financial-literacy-open-funded-024 | Backlog | maintenance | low | medium | funded ($500 cap) |

**Notes:**
- task 016 (i18n) uses `type:"writing"` + `deliverable:"translation"` — `translation` is not a valid type in the Hee-Lee Oss schema.
- task 023 (assistant) is `riskTier:"high"` and backlog-only; it requires a governance decision before starting.
- task 024 (funded reviewer-hours) uses `lane:"funded"` with `fundedBudgetUsd:500`; requires Hee-Lee Oss governance approval.
- All `verifiedNeed` values are `false` (no delivery partner or credentialed reviewer yet secured).

---

## Example task JSON

Complete, schema-valid Task JSON for the first M0 task (`financial-literacy-open-policy-001`):

```json
{
  "id": "financial-literacy-open-policy-001",
  "title": "Editorial / product-neutrality / not-advice policy charter (refused-use set, non-commercial redirect, non-shaming, jurisdiction-honesty)",
  "project": "financial-literacy-open",
  "type": "design-spec",
  "lane": "donated",
  "priority": "high",
  "domain": ["education", "financial-literacy", "oer", "consumer-protection", "accessibility"],
  "riskTier": "medium",
  "urgent": false,
  "deliverable": "document",
  "tokenEstimate": "medium",
  "status": "open",
  "context": "Financial-Literacy-Open is an openly-licensed, plain-language curriculum + privacy-preserving toolkit teaching budgeting, saving, and debt basics. It is EDUCATION, NOT financial advice, and is strictly product-neutral: it never recommends a financial product/brand/institution, never carries affiliate or lead-gen links, and never gives individualized advice. Most 'financial literacy' content online is really lead-generation, so commercial disinterest is this project's trust moat and a hard product requirement. This is the cold-start task that writes the editorial/product-neutrality/not-advice charter that all later content, tooling, and the automated linter must implement and be tested against. This is a MEDIUM risk-tier project; no delivery partner or credentialed financial-educator reviewer is yet secured.",
  "objective": "Write the authoritative editorial / product-neutrality / not-advice policy charter that all later content and code must implement and be tested against: the education-vs-advice line, the concrete refused-use set, the non-commercial redirect rule, the persistent 'educational, not financial advice' framing, the non-shaming / structurally-honest editorial rules, the jurisdiction-honesty rule (neutral core; labeled, locally-reviewed overlays), and the credentialed-expert sign-off gate.",
  "acceptanceCriteria": [
    "Enumerates the refused-use set in concrete, testable terms: individualized financial advice ('what should I do with my money'); investment/securities/crypto/forex/retirement-allocation advice and ticker/fund picks; naming or ranking specific products, brands, or institutions; affiliate/referral/lead-gen/sponsored content; tax/legal/accounting/insurance/bankruptcy advice; get-rich-quick / day-trading / MLM / gambling / 'credit-repair' / debt-settlement schemes; and collecting users' personal financial data",
    "Defines the allowed educational categories and the education-vs-advice line in plain terms",
    "Mandates the non-commercial redirect on refusals (free nonprofit counselor / public consumer-finance agency + the relevant lesson - never a product) and the persistent 'educational, not financial advice' framing on every learner-facing surface",
    "Defines the non-shaming / structurally-honest editorial rules: no blame or moralizing of poverty or debt, never imply hardship is a personal failing, never promise budgeting alone fixes structural problems, and route people in distress to free non-commercial help",
    "Defines the jurisdiction-honesty rule: a jurisdiction-neutral core with figures shown as labeled illustrative examples, and country-specific claims only inside a clearly-labeled, locally-reviewed overlay - never presented as universal",
    "Specifies that these rules are enforced by an automated product-neutrality/not-advice linter (a CI gate) AND credentialed expert review, not by a disclaimer footer, and defines what the linter must detect",
    "Reviewed and signed off by a credentialed financial educator (AFC or equivalent) and the product-neutrality reviewer, recorded in the reviewers ledger (version-scoped)"
  ],
  "resources": [
    "planning/projects/financial-literacy-open/PLAN.md",
    "CLAUDE.md",
    "docs/good-deed-definition.md",
    "packages/schema/src/schemas.ts",
    "planning/projects/public-official-guide/PLAN.md"
  ],
  "output": "A reviewed policy-charter document (the editorial / product-neutrality / not-advice charter) defining the education-vs-advice line, the refused-use set, the non-commercial-redirect rule, the not-advice framing, the non-shaming and jurisdiction-honesty rules, and the linter + expert-review gates - the contract that financial-literacy-open-linter-003 (linter) and all content tasks implement and are verified against.",
  "requestor": "TO BE SECURED",
  "verifiedNeed": false,
  "outputLicense": "CC-BY-4.0"
}
```
