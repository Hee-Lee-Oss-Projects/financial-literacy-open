# Financial-Literacy-Open — PLAN.md

> Status: Draft · Version: 0.1.0 · Last updated: 2026-06-28 · Owner: TBD (maintainer) · Lane: donated

An open, freely-reusable curriculum and toolkit that teaches the **universal basics of personal
money management** — budgeting, saving, and managing debt — in **plain, non-judgmental, product-
neutral** language. It is **education, not financial advice**: it explains how money concepts work
and helps a learner think, but it never tells an individual what to do with their money, never names
or recommends a financial product, brand, or institution, and never earns a referral. The
"**education-not-advice / product-neutral / non-shaming**" stance is not a disclaimer footer — it is
the project's identity, enforced by an editorial policy layer, an automated linter, and credentialed
expert review.

**Positioning.** The internet is saturated with "financial literacy" that is really lead-generation:
free content that funnels readers toward a credit card, a brokerage, a crypto exchange, a payday
lender, or an MLM. Financial-Literacy-Open is the opposite by construction — openly licensed,
commercially disinterested, jurisdiction-honest, and reviewed by accredited financial educators. Its
moat is **trustworthiness**: content a teacher, librarian, social worker, or refugee-resettlement
caseworker can hand to a vulnerable learner without worrying who profits.

---

## Executive summary

Low financial literacy is widespread and consequential: people pay avoidable fees and interest,
fall for scams and predatory products, lack emergency savings, and carry debt they do not understand
— and the people hit hardest are those with the least margin for error (young adults, students,
recent immigrants and refugees, the unbanked/underbanked, and low-income households). Good,
trustworthy, freely-reusable educational material exists in pockets (public consumer-finance
agencies, some nonprofits) but is fragmented, often jurisdiction-locked, frequently written above
the reading level of the people who most need it, and surrounded by commercially-motivated content
dressed up as education.

Financial-Literacy-Open delivers a small, **excellent**, openly-licensed core curriculum —
budgeting, saving, and debt basics — plus a glossary, printable worksheets, and **stateless,
privacy-preserving** interactive calculators that **store nothing and send nothing**. Every factual
claim is cited to an authoritative, openly-reusable source; every lesson is written in plain language
at a measured reading level, reviewed by a **credentialed financial educator** (e.g., an Accredited
Financial Counselor / AFC® or equivalent), and carries persistent **"educational, not financial
advice"** framing.

Three design facts define the project:

1. **Education, not advice — and product-neutral.** This is a **MEDIUM** risk-tier project: financial
   accuracy matters and the "not advice" line must hold, but the project deliberately stays out of
   the **high**-stakes individualized-advice zone (no "what should *I* do with my money," no
   investment/securities/tax/legal advice, no product recommendations). The line is enforced, tested,
   and reviewed — not asserted in a footer.
2. **Jurisdiction-honest.** Most "money basics" content silently assumes one country's system (US
   credit scores, 401(k)s; UK ISAs; etc.). This project ships a **jurisdiction-neutral core** first
   (concepts true everywhere, with figures shown as labeled examples), and treats anything
   country-specific (credit-reporting systems, tax-advantaged accounts, consumer-protection rights,
   bankruptcy) as a **clearly-labeled overlay reviewed by a local expert** — never as universal truth.
3. **Non-shaming and structurally honest.** Financial-literacy content often moralizes about poverty.
   This project's editorial charter forbids shame/blame framing, never implies hardship is a personal
   failing, never promises that budgeting alone fixes structural problems (low wages, medical debt,
   discrimination), and routes people in genuine distress to free, non-commercial help.

**Honesty note — no partner secured.** No school, library system, adult-education program, nonprofit
counseling agency, CDFI, or resettlement organization has yet agreed to adopt or co-deliver the
curriculum, and **no credentialed financial-educator reviewer is yet engaged.** Every
delivery-dependent task is marked `TO BE SECURED` with `verifiedNeed: false`. Unlike an app, **the
reviewed open curriculum is itself a public good the moment it is released to an open repository** —
so the project has a real fallback — but the project's **measured** Definition of Shipped (learners
demonstrably improving) requires a real delivery partner.

**Partner-acquisition plan (dated) and build-vs-release decision rule.** Outreach is time-boxed
against the build, not open-ended: by **2026-08-31** the launch jurisdiction-scope decision is made
(jurisdiction-neutral core confirmed; see *Open questions*) and ≥ 3 candidate delivery partners
(public library system, community-college/adult-ed program, nonprofit financial-counseling agency,
or refugee-resettlement org) are in active conversation; by **2026-09-30** a **credentialed
financial-educator reviewer** is engaged (hard gate for M1 content); by **2026-12-31** a delivery
partner + steward is secured (M5 gate). **Decision rule:** if no credentialed reviewer is engaged by
the M1 entry date, content drafting does not begin and the project holds at M0 (policy + pipeline +
linter). If no delivery partner is secured by **2027-03-31** (≈ M4 completion), the project does
**not** stall: it **releases the reviewed, openly-licensed curriculum to an OER commons** (e.g., an
open courseware/OER repository) as a standing public good, and continues partner outreach for the
measured-outcome pilot. The reviewed content is valuable in either path.

---

## Problem & beneficiaries

**Who is helped (directly):** learners with low or developing financial literacy and limited access
to trustworthy, non-commercial guidance —

- young people and students approaching first income, first account, first debt;
- recent immigrants and refugees learning a new country's money system (often while learning the
  language);
- the **unbanked and underbanked**, and people in financial precarity who are heavily targeted by
  predatory products (payday loans, "credit repair," rent-to-own, MLMs);
- adult learners and the financially excluded served by libraries, adult-education, and nonprofit
  counseling programs.

**Who is helped (ultimately):** the same learners as they make better-informed money decisions —
starting a budget, building even a small emergency buffer, understanding interest before borrowing,
recognizing a scam — and the educators, counselors, and caseworkers who need vetted material they
can hand out without a commercial agenda attached.

**The need.** Financial illiteracy is costly and unequally distributed. The standard remedies are
either (a) commercially conflicted (content that profits from steering you to a product), (b)
jurisdiction-locked and written for a different country, or (c) pitched above the reading level of
the audience that needs it most. Authoritative, reusable material does exist — many **government
consumer-finance and central-bank educational materials are public domain or openly licensed**, and
some nonprofits publish under Creative Commons — but it is scattered, uneven, and rarely assembled
into a coherent, plain-language, accessible, translation-ready, **provably non-commercial** core.

**Verified need / partner:** **TO BE SECURED.** No delivery partner, sponsoring organization, or
credentialed reviewer has yet committed. Target partner profiles: a **public library system** or
adult-education program; a **community college**; a **nonprofit financial-counseling agency** (e.g., a
member of a national association of accredited financial counselors / nonprofit credit counseling);
a **CDFI** or financial-inclusion nonprofit; a **refugee-resettlement** organization (for the
new-arrival audience). Until one is secured, the project builds the editorial policy + pipeline, the
jurisdiction-neutral core curriculum, and the privacy-preserving tools for review, and marks all
delivery/outcome work `TO BE SECURED`. Outreach is **dated** (see executive summary), with a
**build-vs-release/pivot decision rule** if dates slip.

---

## Goals and non-goals

**Goals**

- Produce an openly-licensed (CC-BY-4.0), plain-language **core curriculum** on budgeting, saving,
  and debt basics — accurate, cited, accessible, translation-ready, and **jurisdiction-honest**.
- Ship an **editorial / product-neutrality / not-advice policy layer** that *provably* keeps the
  content educational and commercially disinterested — enforced by an automated linter and
  credentialed review, not a disclaimer.
- Provide **stateless, privacy-preserving** interactive tools (budget/debt/savings calculators,
  printable worksheets) that **store nothing and transmit nothing** — a learner's financial figures
  never leave their device.
- Have every factual claim **cited** to an authoritative, openly-reusable source, with provenance
  recorded and a **staleness/review cadence** for figures that change (rates, thresholds, examples).
- Get all content **reviewed and signed off by a credentialed financial educator** (AFC® or
  equivalent), with any jurisdiction-specific overlay reviewed by a local expert.
- Be **non-shaming and structurally honest**: never moralize about poverty, never imply hardship is a
  personal failing, route people in distress to free non-commercial help.
- Deliver to **real learners** through a partner and **measure outcome** (comprehension gain and at
  least one concrete, self-reported money-management action).

**Non-goals**

- **Not financial advice.** No individualized recommendations ("what should *I* do with my money");
  no portfolio, retirement, or investment allocation guidance; no securities/crypto/forex advice; no
  market timing or stock/ticker picks.
- **Not product, brand, or institution recommendations** — no naming a "best" bank, card, broker,
  app, loan, or insurer; **no affiliate links, lead-gen, referral fees, or sponsored placement, ever.**
- **Not tax, legal, accounting, or insurance advice** — no tax-return preparation, no bankruptcy
  filing guidance, no legal interpretation; route to qualified non-commercial professionals.
- **Not a get-ahead / wealth / "side-hustle" engine** — no get-rich-quick, day-trading, MLM,
  gambling, dropshipping, "credit repair," or debt-settlement schemes.
- **Not a data collector** — the project never asks for, transmits, or stores a user's personal
  financial information; tools are client-side only.
- **Not a substitute** for a qualified financial counselor, and it says so persistently.
- **Not jurisdiction-comprehensive at launch** — depth on a jurisdiction-neutral core first;
  country-specific overlays only with a local reviewer, never breadth without review.

When a request or use falls in the refused set (e.g., "tell me which fund to buy," "is this a good
loan"), the content/assistant surface refuses the advice, explains the education-vs-advice line in
plain terms, and **redirects to a free, non-commercial resource** (a nonprofit financial counselor, a
public consumer-finance agency) and to the relevant lesson — **never to a commercial product**. This
non-commercial redirect is the project's ethical differentiator and is held to an explicit acceptance
criterion (see *Scope* and *Success metrics*).

---

## Success metrics (outcomes)

Outcome-centric and beneficiary-first. Reach/traffic vanity metrics (page views, downloads) are
**not** success on their own; they only matter as a path to learner outcomes.

| Metric | Baseline | Target (pilot) | How measured |
|---|---|---|---|
| Learner comprehension gain | none | median **+30%** absolute on a short pre/post check across the core modules | Anonymous pre/post quiz in the partner setting (no PII; aggregate only) |
| Learners reporting a concrete money action | 0 | ≥ **20** learners report ≥ 1 action (started a budget, opened/started an emergency buffer, made a debt-payoff plan, identified/avoided a scam) | Anonymous post-survey via partner; attested aggregate |
| Claims cited to an authoritative open source | n/a | **100%** of factual claims carry a citation to a verified, reusable source | Citation-coverage check + reviewer checklist |
| Credentialed expert sign-off before content ships | n/a | **100%** of published lessons have recorded AFC®-or-equivalent sign-off (jurisdiction overlays: local-expert sign-off) | Governance reviewers ledger |
| Product-neutrality violations in shipped content | n/a | **0** product/brand recommendations, affiliate/lead-gen patterns, or "buy/invest" advice phrasings | Automated product-neutrality linter (CI) + reviewer audit |
| "Educational, not financial advice" framing coverage | n/a | **100%** of learner-facing surfaces carry the framing + the non-commercial-help redirect | Framing/lint check + review |
| Readability | n/a | core lessons at **≤ grade 8** (target grade 6 for foundational), with a plain-language pass | Automated readability metric + plain-language reviewer |
| Accessibility | n/a | core flows + printables meet **WCAG 2.2 AA**; printables usable in B/W and screen-reader-friendly | Accessibility audit |
| Privacy: personal financial data collected | n/a | **0 bytes** — tools provably client-side; no analytics on financial inputs; no PII stored | Privacy review + network/storage test on the calculators |
| Stale-figure containment | n/a | **0** time-sensitive figures served past their `validUntil` without an auto-flag and re-verification | Staleness test against `lastVerified`/`validUntil` |
| Translation coverage (pilot languages) | 0 | core curriculum available in **≥ 2** pilot languages, each language-reviewed | Per-language review log |

The **defining success outcome** (Definition of Shipped): real learners, reached through a secured
partner, **demonstrably improve** — measurable comprehension gain **and** at least one concrete,
self-reported money-management action — using content that is cited, expert-signed-off,
product-neutral, accessible, and privacy-preserving.

---

## Scope

**In scope**

- **Editorial / product-neutrality / not-advice policy layer** (the charter): the education-vs-advice
  line, the refused-use set, the non-commercial-redirect rule, the non-shaming/structural-honesty
  rules, and the jurisdiction-honesty rule — enforced by review **and** an automated linter.
- **Core curriculum (jurisdiction-neutral):** Budgeting basics; Saving basics (incl. the emergency-
  buffer concept); Debt basics (interest, principal, compounding, prioritization, the cost of
  borrowing); Banking/accounts basics (generic, product-neutral); Recognizing scams & predatory
  products. Each: plain-language, multi-level where useful, cited, expert-reviewed.
- **Glossary** of money terms (plain definitions, cited, jurisdiction-flagged where relevant).
- **Privacy-preserving interactive tools (client-side only):** a budget worksheet, a debt-payoff
  illustrator (e.g., snowball vs. avalanche, shown as illustration not advice), and a savings-goal
  calculator — **no data leaves the device, nothing stored, no analytics on inputs.**
- **Printable worksheets / one-pagers** (offline, low-bandwidth, B/W-friendly).
- **Provenance + staleness system:** per-claim sources; `lastVerified`/`validUntil`; review cadence.
- **Accessibility, plain-language, and translation-readiness** as first-class, not bolt-on.
- **Optional jurisdiction overlay** (one jurisdiction max at launch, only with a local reviewer):
  clearly-labeled country-specific notes (credit reporting, account types, consumer rights).
- **QA/eval:** product-neutrality linter, citation-coverage check, readability + accessibility audit,
  a "not-advice / redirect" check.

**Out of scope (explicitly will NOT do)**

- Any **individualized financial advice** or recommendation tailored to a person's situation.
- **Investment, securities, crypto, forex, retirement-allocation, or market-timing** guidance of any
  kind; specific tickers/funds; "is now a good time to buy."
- **Naming or ranking specific products, brands, institutions, or apps**; **affiliate links,
  referral/lead-gen, or sponsored content** — categorically forbidden.
- **Tax, legal, accounting, insurance, or bankruptcy** advice or preparation.
- **Get-rich-quick / wealth-building / side-hustle / day-trading / MLM / gambling / "credit-repair"
  / debt-settlement** content.
- **Collecting, transmitting, or storing** a user's personal financial data; user accounts tied to
  financial profiles; analytics on financial inputs.
- Presenting one country's system as **universal**; shipping jurisdiction-specific claims without a
  local reviewer.
- Fear-based, shaming, or moralizing framing of poverty or debt.

When a request falls in the refused set, the surface refuses that part, explains the
education-vs-advice line, and **redirects only to free/non-commercial help** (nonprofit counselor,
public consumer-finance agency) plus the relevant lesson. A refusal that fails to emit a correct,
**non-commercial** redirect is a QA failure — the same as a missed product-neutrality violation.

---

## Solution approach & architecture

This is a **content/OER project with lightweight, privacy-preserving static tooling** — not a
multi-tenant app. The pipeline and tools are deliberately simple so the artifact is durable,
auditable, forkable, and cheap to host (static).

**Stack.** TypeScript + ESM, pnpm workspaces (per Hee-Lee Oss conventions). Content authored as
**Markdown/MDX with structured YAML frontmatter** validated against a JSON Schema. A static-site
generator (e.g., Astro or similar) renders the open site + PWA-style offline support; printables
rendered to PDF from the same source. Interactive calculators are **client-side-only** components
(no backend, no network calls with user data). Optional AI assistance for *authoring/drafting* runs
through Hee-Lee Oss's neutral LLM client (Anthropic Claude as the reasoning resource; model selection and
pricing per the Claude API skill) — but **no learner-facing live LLM endpoint** ships at launch (a
live "ask a question" assistant is backlog and would inherit the full guardrail layer). Code license
**MIT**; content/data **CC-BY-4.0**.

**Components**

1. **Editorial / product-neutrality policy layer (`policy/`) — built first.** A versioned charter
   plus an **automated `product-neutrality` + `not-advice` linter** that scans content and tool copy
   for: brand/product/institution names (curated denylist + heuristics), ticker symbols, affiliate/
   referral URL patterns and UTM/lead-gen markers, advice-phrasing (e.g., "you should buy/invest/
   choose," "the best card/bank/broker is"), unqualified guarantees of returns, and **unflagged
   jurisdiction-specific claims** (e.g., "your credit score," "your 401(k)") outside a labeled
   overlay. Violations **fail CI**. Non-shaming heuristics flag moralizing/blame phrasing for human
   review. This linter is the content analog of a red-team suite: a release gate, not a style guide.

2. **Content model + schema (`schema/`).** A JSON Schema for lesson/glossary frontmatter:
   `id`, `topic`, `readingLevel`, `jurisdiction` (`"neutral"` or an ISO country code),
   `sources[]` (each with citation, URL, license/legal-status, `lastVerified`, `validUntil`),
   `reviewer` + `reviewedVersion` + `signoffDate`, `plainLanguageChecked`, `a11yChecked`, `license`,
   `notAdviceFraming: true`. A claim cannot ship without `sources[]`; a lesson cannot ship without a
   recorded reviewer sign-off for its current version.

3. **Provenance + staleness subsystem.** Every factual/numeric claim is backed by a `Source`.
   Time-sensitive figures (interest examples, thresholds, statistics) carry a `validUntil` derived
   from a per-type review interval. A **staleness check** flags/withholds any claim past `validUntil`
   until re-verified and **re-signed-off** (fresh `lastVerified`/`validUntil`). Sign-off is
   **version-scoped** — edits require re-review.

4. **Curriculum (`content/`).** The jurisdiction-neutral core modules + glossary, authored in
   MDX, each cited, plain-language, accessible, and translation-ready (strings externalized for i18n).
   Numbers are shown as **labeled illustrative examples**, never as recommendations or benchmarks
   ("a common rule of thumb is X — it may not fit your situation"), and currency is shown
   neutrally/parametrically.

5. **Privacy-preserving tools (`tools/`).** Budget worksheet, debt-payoff illustrator, savings-goal
   calculator — **pure client-side**, computed in-browser, **nothing transmitted or persisted**
   (optional local-only save behind an explicit, clearly-labeled opt-in that uses the user's own
   device storage and is never uploaded). Each tool carries the not-advice framing and an
   "illustration, not a recommendation" label, and is covered by a network/storage test proving no
   data egress.

6. **Build + distribution (`site/`).** Static site + offline/PWA support; PDF printables; structured
   exports (glossary JSON, lesson metadata) for reuse by educators and other OER projects.

7. **QA/eval (`scripts/`).** The product-neutrality + not-advice linter, citation-coverage check,
   readability scorer, accessibility audit, staleness check, and (pilot) the anonymous pre/post
   comprehension instrument — all runnable in CI and documented.

**Key decisions (locked)**

- **Education-not-advice and product-neutral are enforced (linter + review), not asserted.**
- **Jurisdiction-neutral core first;** country-specifics are a labeled, locally-reviewed overlay.
- **No collection of personal financial data; tools are client-side only** — privacy by construction.
- **No affiliate/lead-gen/sponsorship — ever** — commercial disinterest is the trust moat.
- **Non-shaming, structurally-honest** editorial voice is a charter rule, lint-flagged + reviewed.
- **MIT** for code, **CC-BY-4.0** for content; everything sourced from open/PD/CC material only.
- **No learner-facing live LLM** at launch (authoring-only AI); a live assistant is gated backlog.

---

## Data, licensing & compliance

**Source material.** Authoritative, **openly reusable** educational material only:

- **Government consumer-finance / financial-education agencies and central banks**, whose works are
  frequently **public domain** (e.g., U.S. federal works are generally public domain) or openly
  licensed — but **license status varies by country and body** and must be verified per source.
- **Nonprofit and OER materials** published under **Creative Commons** (CC-BY / CC-BY-SA, with
  share-alike compatibility checked) or public domain.
- **Reputable reference** material only where the license permits reuse/derivatives.

**Hard rule:** **every source's reuse terms are verified and recorded before its content ships.** No
scraping of all-rights-reserved commercial "finance" sites; no copying proprietary methodologies;
**no commercial product datasheets, rate tables, or comparison data** (these are both license- and
product-neutrality-hazardous). Government-edict / public-domain status is confirmed per source, not
assumed.

**Provenance model.** Each claim → a `Source` record (name, publisher, jurisdiction, citation, URL,
retrieval date, **license/legal-status note**, `lastVerified`, `validUntil`). A lesson cannot surface
a claim without an attached, verified source; a citation-coverage check enforces this.

**Staleness is fail-safe.** Financial figures, rates, thresholds, and statistics drift. A claim past
its `validUntil` is **auto-flagged or withheld** until re-verified and re-signed-off — the common
failure mode (a figure silently goes stale) becomes a visible, gated event.

**Output licensing.** Code: **MIT**. Content, curriculum, glossary, worksheets, datasets:
**CC-BY-4.0** (attribution to primary sources preserved on redistribution). Where a source is
**CC-BY-SA**, derivative content inherits **share-alike** and is segregated/labeled accordingly to
avoid license conflict. Translations are CC-BY-4.0 (or SA where inherited), crediting translators.

**Privacy / PII stance (conservative — privacy by construction).** The project's strongest privacy
guarantee is structural: **it never asks for, transmits, or stores a user's personal financial
data.** Interactive tools compute **entirely client-side**; there is **no backend that receives
financial inputs**, **no analytics on financial inputs**, and **no user accounts tied to financial
profiles**. Any "save my numbers" feature is **local-device-only, opt-in, and never uploaded**. Pilot
measurement uses **anonymous, aggregate** pre/post instruments with **no PII** and no linkage to
individuals. No secrets/tokens/PII in logs, receipts, or committed files (Hee-Lee Oss rule).

**Attribution.** Content cites primary sources; redistribution preserves CC-BY attribution. Reviewers
and translators are credited (with consent) in a ledger, scoped to the versions they approved.

---

## Quality, review & risk gates

**Risk tier: MEDIUM** (per `docs/good-deed-definition.md`: domain accuracy needed; reviewer with
relevant skill required). The project **deliberately stays out of the HIGH tier** by refusing
individualized/investment/tax/legal advice; if any surface ever crossed into individualized
high-stakes advice it would be HIGH and out of scope. Pure pipeline/site/tooling tasks are low–medium;
anything stating a financial fact, figure, or rule is medium and requires credentialed sign-off.

**Required reviews before a deed is "done":**

- **Maintainer** review on all PRs (engineering quality, agent-neutral core, no secrets/PII, CI green,
  linter green).
- **Credentialed financial-educator sign-off** (AFC® or equivalent; or a nonprofit credit counselor /
  qualified financial educator) recorded before any factual/curriculum content ships. **No reviewer,
  no ship.** Jurisdiction overlays additionally require a **local expert** for that jurisdiction.
- **Product-neutrality / not-advice gate** — the automated linter passes in CI **and** a reviewer
  confirms no product steering, no advice phrasing, and a correct non-commercial redirect on refusals.
- **Plain-language + accessibility review** for learner-facing content (readability target, WCAG 2.2 AA).
- **Privacy review** for any interactive tool (proves client-side-only, no data egress, no PII).

**Persistent framing.** Every learner-facing surface carries **"Educational information, not financial
advice"** and a pointer to free, non-commercial help (a nonprofit financial counselor / public
consumer-finance agency).

**Definition of Shipped (project):** real learners reached via a secured partner **demonstrably
improve** (comprehension gain + ≥ 1 concrete self-reported money action), using content that is
cited, **credentialed-expert-signed-off**, **product-neutral (linter + review clean)**, accessible,
and privacy-preserving — with outcomes recorded as aggregate, anonymous data.

---

## Roadmap & milestones

Phased: policy + pipeline + linter first; cited, reviewed content next; privacy-preserving tools and
i18n; then partner delivery with measured outcomes; then sustain. Dependencies flow M0 → M1 → M2 →
M3 → M4 → M5 → M6.

- **M0 — Editorial policy, pipeline & linter (cold-start).**
  *Goal:* the not-advice/product-neutrality stance and an OER pipeline exist before any lesson.
  *Exit:* editorial/product-neutrality/not-advice **policy charter** merged; **automated linter**
  (product/brand/affiliate/advice-phrasing/unflagged-jurisdiction + non-shaming flags) wired into CI
  and failing the build on violations; content/lesson **JSON Schema** + repo + pnpm/TS/ESM + CI green;
  provenance/staleness fields defined; "educational, not advice" framing + non-commercial-redirect
  pattern wired in; **launch jurisdiction-scope decision** (neutral core confirmed). *Reviewer
  engagement targeted by 2026-09-30 gates M1.*

- **M1 — Budgeting module + provenance proof (first reviewed content).**
  *Goal:* one foundational module, end-to-end, proving the whole pipeline.
  *Exit:* Budgeting-basics lessons drafted, **cited, plain-language, accessible**, linter-clean, and
  **credentialed-expert-signed-off**; provenance + staleness working on real sources; glossary v1 for
  the module; readability + a11y checks passing. **Kill-gate:** if no credentialed reviewer is engaged,
  M1 content does not start (project holds at M0).

- **M2 — Core curriculum (Saving, Debt, Banking, Scams).**
  *Goal:* the rest of the jurisdiction-neutral core, to the same bar.
  *Exit:* Saving, Debt, Banking-basics, and Recognizing-scams modules drafted, cited, plain-language,
  accessible, linter-clean, and expert-signed-off; glossary expanded; all numbers shown as labeled
  illustrative examples; non-commercial-redirect coverage verified.

- **M3 — Privacy-preserving tools & printables.**
  *Goal:* hands-on, stateless tools and offline materials.
  *Exit:* budget worksheet, debt-payoff illustrator, and savings-goal calculator shipped
  **client-side-only** with a passing **no-data-egress / no-PII** privacy test; printable worksheets
  (B/W + screen-reader friendly); each tool carries not-advice + "illustration, not recommendation"
  framing.

- **M4 — i18n, accessibility hardening & QA/eval; pilot readiness.**
  *Goal:* prepare for real learners.
  *Exit:* strings externalized; core curriculum translated into **≥ 2 pilot languages**, each
  **language-reviewed**; WCAG 2.2 AA verified; readability targets met; full QA suite (linter,
  citation coverage, staleness, a11y, readability) green; anonymous pre/post comprehension instrument
  built; pilot facilitation runbook ready.

- **M5 — Partner delivery & measured outcomes (the deed).**
  *Goal:* real learners benefit, measurably.
  *Exit (Definition of Shipped):* a secured partner delivers the curriculum to real learners;
  anonymous pre/post shows the comprehension-gain target and ≥ 20 learners report a concrete money
  action; content expert-signed-off, linter-clean, accessible, privacy-preserving; outcomes recorded
  (aggregate, anonymous). *(Gated on a secured partner — TO BE SECURED.)* **Fallback:** if no partner
  by ~2027-03-31, **release the reviewed curriculum to an OER commons** as a standing public good and
  continue outreach for the measured pilot.

- **M6 — Sustain, review cadence & expansion (post-delivery).**
  *Goal:* durable maintenance and careful growth.
  *Exit:* maintenance rotation + **content review cadence** (figures re-verified on schedule, re-sign-
  off on change) + outcomes dashboard (aggregate, anonymous); documented, locally-reviewed process for
  adding a **jurisdiction overlay** or a new language.

The **launch jurisdiction-scope decision is made in M0 and gates M2/M6** overlays; M1+ content blocks
on the secured credentialed reviewer; M5 blocks on a secured delivery partner.

---

## Work breakdown

The itemized, schema-mapped backlog lives in **`TASKS.md`**: ~18 tasks across milestones M0–M6 plus a
future backlog, each mapped to the Hee-Lee Oss Task JSON schema, with per-task acceptance criteria for the
most important items, milestone Definitions of Done, and a complete example Task JSON for the first M0
task (the editorial / product-neutrality policy charter). The first build item is the **policy charter
+ linter**, reflecting that "education-not-advice / product-neutral" is a hard product requirement; an
early **credentialed-reviewer engagement gate** is sequenced so content investment is gated on a real
reviewer, and a **single-module M1 proof** validates the pipeline before the rest of the curriculum.

---

## Governance, roles & stakeholders

- **Maintainer (Owner): TBD.** Owns architecture, the agent-neutral pipeline, CI, the linter, and
  merge quality.
- **Reviewers / rotation:** at least one engineering reviewer plus a designated **product-neutrality /
  not-advice reviewer** who audits content for product steering, advice phrasing, and correct
  non-commercial redirects independently of authors; a **plain-language/accessibility reviewer**.
- **Credentialed expert reviewer (MEDIUM tier): TO BE SECURED** — an **Accredited Financial
  Counselor (AFC®) or equivalent** (nonprofit credit counselor / qualified financial educator); signs
  off all factual/curriculum content before it ships. Tracked in a reviewers ledger with credentials
  and consent. **Independence / COI:** the reviewer must have **no financial interest in any product
  the content could touch** and **discloses affiliations**; a reviewer tied to a financial-product
  seller **recuses** (the entire trust thesis depends on commercial disinterest). Sign-off is
  **version-scoped** (edits require re-review). **Name-use limits:** a reviewer's name may appear in
  the ledger only for versions they approved, with consent, and may not imply endorsement of the
  product or of content they did not review. **Disagreement fallback:** the expert holds a **veto on
  whether content is accurate/safe to publish**; a maintainer cannot override a "do not ship" on
  substance — the content does not ship, the disagreement is logged and escalated to Hee-Lee Oss governance
  or a second reviewer.
- **Jurisdiction expert (for any overlay): TO BE SECURED** — a local financial educator / consumer-
  finance professional for the specific country; signs off the overlay.
- **Steward (last-mile owner): TO BE SECURED** — owns the delivery-partner relationship and the
  facilitation/measurement that constitutes shipping.
- **Delivery partner / requestor: TO BE SECURED** — the library/adult-ed/community-college/nonprofit-
  counseling/CDFI/resettlement organization that puts the curriculum in front of learners.
- **Community / board:** license edge cases (CC-BY vs. CC-BY-SA inheritance), the jurisdiction-scope
  decision, and any move toward a live learner-facing assistant go through Hee-Lee Oss governance.

---

## Dependencies & integrations

- **External services:** Anthropic Claude API (authoring assistance only, behind Hee-Lee Oss's neutral LLM
  client; model selection/pricing per the Claude API skill); static hosting/CDN for the open site +
  printables. **No backend handling user financial data** (privacy by construction).
- **Datasets / sources:** authoritative open consumer-finance / central-bank / nonprofit OER material,
  each with **verified reuse terms** and recorded provenance.
- **Tooling:** pnpm/TS/ESM toolchain; a static-site generator (Astro or similar); a readability
  scorer; an accessibility audit tool; the custom product-neutrality/not-advice linter.
- **Hee-Lee Oss pieces:** `packages/schema` (Task JSON), `CLAUDE.md` (work rules + refusal guardrails),
  `docs/good-deed-definition.md` (risk tiers), Hee-Lee Oss governance (license/edge-case decisions),
  sibling plans (`planning/projects/public-official-guide/{PLAN,TASKS}.md`) for house style.
- **Human/decision dependencies (critical path):** the **credentialed reviewer** (blocks all M1+
  content), the **jurisdiction-scope decision** (M0; gates overlays), and a **secured delivery
  partner + steward** (blocks M5 measured outcomes).

---

## Risks & mitigations

| Risk | Likelihood | Impact | Mitigation | Owner |
|---|---|---|---|---|
| Content drifts into individualized **financial advice** | High | High | Editorial charter draws the education-vs-advice line; not-advice linter flags advice phrasing; persistent "not advice" framing + non-commercial redirect; credentialed sign-off; refuse "what should I do" requests | Product-neutrality reviewer / Expert |
| **Product/brand steering or affiliate/lead-gen** creeps in | Medium | Critical (destroys trust) | Categorical no-affiliate/no-sponsorship rule; product-neutrality linter (denylist + affiliate-URL + advice patterns) fails CI; reviewer audit; commercial-disinterest is a charter identity rule | Maintainer / Reviewer |
| **Inaccurate or outdated** financial fact/figure | High | High | Per-claim citation to authoritative open source (coverage check); credentialed sign-off; **runtime staleness fail-safe** (`validUntil` auto-flags/withholds until re-verified + re-signed-off); figures shown as labeled examples | Expert reviewer |
| Presenting one country's system as **universal** | High | Medium | Jurisdiction-neutral core; linter flags unflagged jurisdiction-specific terms; overlays labeled + locally reviewed | Maintainer / Jurisdiction expert |
| **Shaming/moralizing** framing of poverty/debt | Medium | High (harm to vulnerable learners) | Non-shaming charter rule; lint heuristics flag blame phrasing for human review; trauma-informed plain-language review; route distress to free help | Plain-language reviewer / Expert |
| Source **license/copyright** misuse (commercial finance content) | Medium | High | Verify + record reuse terms per source before shipping; open/PD/CC only; no commercial rate/product data; CC-BY-SA inheritance handled | Maintainer / Expert |
| **No delivery partner** secured → can't reach measured Shipped | High | Medium | Honest `TO BE SECURED`/`verifiedNeed:false`; **dated outreach** (partners by 2026-08-31, reviewer by 2026-09-30, partner by 2026-12-31); **release to OER commons** fallback at ~2027-03-31 (content is a public good without a pilot) | Steward / Maintainer |
| **No credentialed reviewer** engaged → content blocked | Medium | High | Recruit via AFC/nonprofit-counseling associations, university personal-finance programs, libraries; **no content ships without sign-off** (hard gate); hold at M0 if unmet | Maintainer |
| Privacy failure: a tool **leaks financial inputs** | Low | Critical | Client-side-only by construction; no backend for inputs; no analytics on inputs; **no-data-egress test**; privacy review gate; local-only opt-in save | Maintainer |
| Learner **over-relies** on content as advice / acts on a scam example | Medium | High | Persistent not-advice framing; redirect to qualified non-commercial help; scam module teaches verification not just recognition | Expert / Steward |
| Misused as an **MLM/get-rich/"credit-repair"** funnel by a third party | Low | High | CC-BY attribution + no endorsement; charter forbids it; trademark/no-endorsement notice; community reporting | Maintainer |

---

## Security & privacy

**Threat surface.** The primary risks are **content-integrity and trust** rather than classic
infrastructure compromise: (a) advice-creep and product/affiliate steering, (b) inaccurate/stale
figures, (c) a privacy leak of a learner's financial inputs, (d) license violation, (e) third-party
misuse as a commercial/MLM funnel, and (f) supply-chain/secrets hygiene in the build.

**Privacy by construction (the headline control).** There is **no backend that receives a user's
financial data** and **no analytics on financial inputs**. Interactive tools compute **entirely in
the browser**; nothing is transmitted or persisted server-side. The only optional persistence is a
**local-device-only, opt-in "save my numbers"** that never leaves the device. A **no-data-egress
test** (network + storage) is a release gate for every tool. Pilot measurement is **anonymous and
aggregate** with **no PII** and no individual linkage.

**Content-integrity controls.** The product-neutrality/not-advice **linter** (a CI gate) plus
**credentialed expert sign-off** are the core "security" controls for this project's actual threat
model. Citation-coverage and **staleness fail-safe** prevent inaccurate/stale claims from serving.
The non-shaming heuristics flag harmful framing for human review.

**Standard hygiene.** MIT/CC-BY licensing with attribution preserved; **no secrets/tokens/PII in
logs, receipts, or committed files** (Hee-Lee Oss rule); dependency + secret scanning in CI; the static
build has minimal attack surface; the authoring-only LLM usage never sends learner data (there is no
learner data) and runs behind the neutral client. A no-endorsement notice deters MLM/funnel misuse of
the CC-BY content.

**Abuse/misuse prevention.** The refused-use set (individualized advice; investment/crypto/tax/legal
advice; product/brand recommendation; affiliate/lead-gen; get-rich/MLM/"credit-repair") is enforced
by the linter + review and reflected in the editorial charter — not merely documented — and refusals
emit a **non-commercial** redirect, never a product.

---

## Sustainability & maintenance

After delivery, a named **maintenance rotation** owns the pipeline and site; the **steward** owns the
partner relationship and outcome tracking. Financial content has a real **decay rate** — rates,
thresholds, statistics, and examples change — so the **review cadence is enforced at runtime, not just
on a calendar**: each source's `lastVerified`/`validUntil` drives the fail-safe staleness behavior
(auto-flag/withhold past the review window until re-verified and **re-signed-off** by the credentialed
expert). Outcomes are tracked as **aggregate, anonymous** measures (comprehension gain, money-action
counts, reviewer/linter status) on an outcomes dashboard — **not** engagement vanity metrics. Adding a
jurisdiction overlay or a new language follows a documented, **reviewer-gated** process. The
product-neutrality linter and the curriculum are maintained as living artifacts; community
contributions are accepted under CC-BY with the same review + linter gates. If maintenance lapses, the
content remains a usable, openly-licensed OER artifact in the commons.

---

## Open questions

- **Launch jurisdiction scope — decided in M0, not deferred.** Confirmed default: **jurisdiction-
  neutral core** first (universal concepts; figures as labeled examples; currency-neutral). Open item:
  **which single jurisdiction overlay (if any) to add first**, scored by (1) availability of
  **public-domain/openly-licensed** authoritative sources; (2) availability of a **local credentialed
  reviewer**; (3) size of an underserved, low-literacy audience reachable via a partner; (4) tractable
  consumer-finance complexity. The overlay jurisdiction remains `TO BE SECURED`; the **rule and the
  M0 decision deadline are fixed**.
- **Credentialed-reviewer model** — volunteer vs. a future **funded lane** for review hours (with a
  hard budget cap) without compromising independence/commercial-disinterest? (Affects the dated plan.)
- **CC-BY vs. CC-BY-SA inheritance** — how to segregate/label content derived from share-alike
  sources so the overall corpus stays cleanly reusable? (Hee-Lee Oss governance.)
- **Pilot languages** — which ≥ 2 languages first (driven by the secured partner's audience —
  e.g., new-arrival/ESL communities)?
- **Live learner-facing assistant** — keep as gated backlog only? It would require porting the full
  guardrail layer to a runtime LLM endpoint and a much higher safety bar; default is **no** at launch.
- **Pilot outcome instrument** — exact pre/post comprehension items + the money-action survey, built
  to be valid, short, anonymous, and partner-administrable without PII.
- **Reading-level targets per audience** — grade-6 floor for foundational vs. grade-8 for the rest;
  confirm with the plain-language reviewer and partner.

---

## References

- Proposal: `governance/proposals/financial-literacy-open.md` *(TO BE WRITTEN — no proposal exists yet)*
- Hee-Lee Oss work rules & refusal guardrails: `CLAUDE.md`
- Good-deed definition & risk tiers: `docs/good-deed-definition.md`
- Task JSON schema: `packages/schema/src/schemas.ts`
- Portfolio entry: `planning/ROADMAP.md` (Track 3 — `financial-literacy-open`, ⚪ selected, med)
- Sibling Hee-Lee Oss plan for house style (medium/high-risk, "not advice"): 
  `planning/projects/public-official-guide/{PLAN,TASKS}.md`
- Exemplar plan depth/structure: `C:\code\Ofelia\plan.md`
- Planning spec: `scratchpad/PLAN_SPEC.md`

---

## Appendix A — Improvements applied

Twenty-five specific improvements were identified against the first draft and **applied** above. Each
is a concrete change to the plan, not a vague aspiration.

1. **Reframed from "app" to "OER + static tooling."** Made the artifact a forkable open curriculum
   with client-side tools, not a multi-tenant app — cheaper, more durable, and right for content.
2. **Made product-neutrality an automated CI gate (the linter), not a guideline** — denylist +
   affiliate-URL + ticker + advice-phrasing detection that *fails the build*, mirroring a red-team
   suite.
3. **Added unflagged-jurisdiction detection to the linter** so US/UK-specific terms ("credit score,"
   "401(k)," "ISA") can't ship inside the "neutral" core without a labeled overlay.
4. **Locked the no-affiliate/no-lead-gen/no-sponsorship rule as identity**, not a setting — named it
   the trust moat and made it a charter rule + linter pattern.
5. **Added the non-commercial redirect requirement** (refusals point only to nonprofit counselors /
   public agencies, never a product) and made it a QA-checked acceptance criterion.
6. **Added a non-shaming / structurally-honest editorial rule** with lint heuristics + plain-language
   review — direct "take real care" for vulnerable learners.
7. **Privacy by construction:** stated the strongest possible stance — *no backend receives financial
   data* — and added a **no-data-egress test** as a per-tool release gate.
8. **Constrained pilot measurement to anonymous, aggregate, no-PII** so outcome tracking can't become
   a privacy hazard.
9. **Added the staleness fail-safe** (`lastVerified`/`validUntil` → auto-flag/withhold + re-sign-off)
   because financial figures decay — a common silent-failure mode now gated.
10. **Made expert sign-off version-scoped** so edits require re-review (prevents stale endorsement).
11. **Added reviewer COI/recusal rules** — a reviewer with a financial-product interest recuses;
    commercial disinterest is required, since the whole thesis is trust.
12. **Added the disagreement-fallback veto** (expert can block ship on substance; escalation path).
13. **Set the risk tier explicitly at MEDIUM and stated the line to HIGH** (individualized/investment/
    tax/legal advice = HIGH = out of scope) so scope creep is detectable.
14. **Replaced vanity metrics with learner-outcome metrics** (comprehension gain + concrete money
    action) and marked reach as a path, not a goal.
15. **Added readability + WCAG 2.2 AA as measured targets**, since the neediest audience is often
    low-literacy/ESL — accessibility is core, not bolt-on.
16. **Added i18n / ≥ 2 language-reviewed translations** as an M4 deliverable for the new-arrival
    audience.
17. **Specified labeled illustrative numbers / currency-neutrality** ("a common rule of thumb is X —
    it may not fit you") so examples never read as recommendations or benchmarks.
18. **Added CC-BY-SA inheritance handling** so share-alike sources don't silently contaminate the
    corpus's reusability.
19. **Added a dated partner-acquisition plan + build-vs-release decision rule** with a genuine
    fallback unique to content: **release to an OER commons** if no pilot — the content is a public
    good regardless.
20. **Added a credentialed-reviewer engagement gate (2026-09-30)** that blocks M1 content — no
    reviewer, no content — preventing unreviewed financial claims.
21. **Sequenced a single-module (Budgeting) M1 proof** to validate the whole pipeline before
    investing in the full curriculum.
22. **Scoped out a live learner-facing LLM at launch** (authoring-only AI) to avoid shipping a runtime
    advice surface without a full guardrail port; made it gated backlog.
23. **Added a scam/predatory-product module** (recognize *and verify*) — a high-impact protection for
    exactly the targeted audience, while staying product-neutral (teaches red flags, names no brands).
24. **Excluded commercial rate/product/comparison data** explicitly — it's both a license and a
    product-neutrality hazard.
25. **Added a no-endorsement notice** to deter third parties from repackaging the CC-BY content as an
    MLM / "credit-repair" / get-rich funnel.

---

## Review sign-off

**Reviewer:** plan author (senior staff engineer + TPM), self-review against `PLAN_SPEC.md`,
`CLAUDE.md`, `docs/good-deed-definition.md`, and the Hee-Lee Oss Task schema.

**Completeness.** All 17 required H2 sections are present and in order. The plan states the lane
(donated), risk tier (MEDIUM, with the line to HIGH made explicit), and an honest partner/need status
(`TO BE SECURED`, `verifiedNeed:false`). Roadmap M0–M6 each carry a goal + measurable exit criteria;
the work breakdown points to `TASKS.md`.

**Correctness against Hee-Lee Oss rules.** (a) Agent-neutral core: authoring-only LLM behind the neutral
client; no learner-facing LLM at launch; no vendor logic in content/pipeline. (b) Refusal guardrails:
the refused-use set covers product steering, affiliate/lead-gen, investment/tax/legal advice,
get-rich/MLM/"credit-repair," and individualized advice — with non-commercial redirects.
(c) For-profit benefit: categorically excluded (no affiliate/sponsorship; commercial disinterest is
the moat). (d) License/provenance: open/PD/CC only, per-source verification, CC-BY-SA inheritance
handled, MIT code / CC-BY content. (e) Privacy/PII: privacy by construction, no financial-data
backend, no-data-egress test, anonymous aggregate measurement. (f) Quality bar: "delivered, not
merged" — Definition of Shipped is measured learner improvement via a secured partner.

**Fixes applied during review.** (1) Made explicit that the *measured* Definition of Shipped needs a
partner while the *content* can ship to the OER commons (resolved an ambiguity between the two
"shipped" senses). (2) Aligned the staleness model wording across *Data*, *Roadmap*, and
*Sustainability*. (3) Ensured every risk in the table has an owner and that the no-egress test, linter,
and sign-off appear consistently as the three release gates. (4) Confirmed the example Task JSON in
`TASKS.md` is schema-valid (`verifiedNeed:false`, `requestor:"TO BE SECURED"`, MEDIUM risk,
`outputLicense` present).

**Open items requiring a human decision** (tracked in *Open questions*): engage a credentialed
financial-educator reviewer (gates all content); secure a delivery partner + steward (gates measured
Shipped); pick the first jurisdiction overlay (if any) and the ≥ 2 pilot languages; decide the
reviewer-compensation/lane model; ratify the CC-BY-SA inheritance approach.

**Verdict:** ready to circulate as a Draft (v0.1.0). No content task may begin until a credentialed
reviewer is engaged; no measured-outcome claim may be made until a partner is secured.
