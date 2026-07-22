# Competitive & Improvement Analysis — `financial-literacy-open`

*Prepared 2026-06-29. Sources are cited inline as URLs; all web claims were grounded against the
linked pages. Scope: PLAN.md v0.1.0 (+ TASKS.md skim) for the open, plain-language, product-neutral
financial-literacy curriculum.*

---

## 1. Correctness & completeness review of PLAN.md

The plan is unusually strong and internally coherent. It already does the single most important thing
right: it treats **independence from financial-product sellers** and the **education-not-advice line**
as *enforced* product requirements (charter + automated linter + credentialed sign-off + version-scoped
review), not as a disclaimer footer. That is the correct architecture for this domain and is well above
the bar of nearly every incumbent. Detailed findings:

**Education-not-advice boundary — correct and defensible.** The plan sets risk tier MEDIUM, explicitly
draws the line to HIGH (individualized/investment/tax/legal advice = out of scope), enumerates a
concrete, testable refused-use set, and requires a *non-commercial* redirect on refusal. This is the
right boundary and is testable. One gap: the boundary between "labeled illustrative example" (allowed)
and "implied benchmark/recommendation" (forbidden) is genuinely hard to lint — e.g. the debt-payoff
illustrator showing snowball vs. avalanche, or "a common rule of thumb is 3-6 months of expenses,"
can read as advice. The plan acknowledges this ("illustration, not recommendation" label) but should
make the *reviewer* (not the linter) the named owner of this judgment, with documented examples of the
line in the charter. Recommend a small "advice-creep" golden-test corpus of borderline phrasings.

**Independence from industry — the strongest part, but tighten two screws.** The categorical
no-affiliate/no-lead-gen/no-sponsorship rule + reviewer COI/recusal rule is excellent and is the real
moat (see §2/§4 — most "free" fin-lit is bank/payment-network/publisher marketing). Two tightenings:
(a) the plan forbids reviewers with a product COI but does not yet address **funding-source COI** for
the project itself — if a future funded lane pays for reviewer hours (an Open Question), the *source*
of those funds must be disclosed and screened, or the independence claim is undermined. (b) The plan
should state a positive **independence disclosure** ("this project has received no funding from, and
has no commercial relationship with, any bank, lender, broker, fintech, or payment network") as a
published, verifiable artifact — incumbents bury their sponsor; making non-sponsorship *legible* is the
differentiator, so publish it.

**Accuracy + sourcing — correct, and the open-source base is real.** Per-claim citation, provenance
records, and the staleness fail-safe (`validUntil` → auto-withhold + re-sign-off) are exactly right;
financial figures decay and most incumbents silently rot. The plan's premise that authoritative open
source material exists is **confirmed**: CFPB content is explicitly public domain — "Information created
by the [CFPB] is in the public domain and you may reproduce, publish, or otherwise use it without the
Bureau's permission"
([consumerfinance.gov educator tools](https://www.consumerfinance.gov/consumer-tools/educator-tools/));
and U.S. federal works (FTC, Treasury/FLEC `MyMoney.gov`, FDIC Money Smart) are generally PD. Gap: the
plan should name a **citation-quality standard** distinguishing primary authoritative sources (CFPB,
central banks, peer-reviewed) from secondary/advocacy sources, and should record *which jurisdiction* a
PD claim is valid for — U.S.-PD does not make a *claim* globally true (see jurisdiction below).

**Region/product-specificity — correctly prioritized; watch the "neutral core" illusion.** The
jurisdiction-neutral-core-first decision with locally-reviewed overlays is the right call and a genuine
differentiator (most incumbents silently assume one country). Caution: many "universal" concepts smuggle
in jurisdiction assumptions — "credit score," "checking/current account," "overdraft," even what counts
as "debt" or "interest" (riba-free/Islamic-finance contexts) vary. The linter's unflagged-jurisdiction
detection is the right tool; expand its denylist beyond US/UK terms (credit score, 401(k), ISA) to
catch the subtler ones, and add a reviewer prompt for "is this concept actually universal?"

**Anti-predatory-lending + scam accuracy — present and well-scoped, but raise it.** The Recognizing-scams
module ("recognize *and verify*") is high-value for exactly the targeted audience and is product-neutral
by teaching red flags, not naming brands — good. Two improvements: (a) ground it in live enforcement
patterns from authoritative PD sources (FTC payday/loan-scam actions:
[ftc.gov](https://www.ftc.gov/news-events/news/press-releases/2020/05/ftc-halts-deceptive-payday-lender-took-millions-consumers);
CFPB) so the red flags are real, not invented; (b) the module must itself be *non-fear-based* and
non-shaming (scam victims are often blamed) — align it with the structural-honesty charter. Consider a
"what to do if it already happened" path (report to a public agency, not a commercial "credit-repair"
firm — which is itself a predatory category the plan correctly excludes).

**Non-commercial framing — correct and made a QA gate.** Making "a refusal that fails to emit a
non-commercial redirect = QA failure" testable is excellent. Minor: ensure the redirect *targets* are
themselves vetted as non-commercial and jurisdiction-appropriate (a "nonprofit credit counselor" list
must be screened; some "nonprofit" counseling agencies have industry ties or upsell debt-management
plans).

**Multilingual — right intent, under-specified.** ≥2 language-reviewed pilot translations is correct
for the new-arrival/ESL audience (the audience most exploited by predatory products). Gaps: the plan
should commit to **translation ≠ localization** (a translated US overlay is still wrong for the target
country), specify RTL/script support and that the readability target must be re-measured *per language*
(grade-level metrics are English-centric), and budget for the fact that plain-language review must be
done by a native speaker, not back-translation.

**Accessibility — correctly first-class.** WCAG 2.2 AA, B/W-printable, screen-reader-friendly,
low-bandwidth/offline PWA, no-registration are all right and match the audience. Add: plain-language is
itself an accessibility feature (cognitive); the grade-6 floor for foundational content is good. Confirm
printables work without color *and* without literacy assumptions (icon support).

**Currency — handled.** Currency-neutral/parametric display with labeled examples is correct; ensure
the calculators are currency-symbol-agnostic and locale-formatting aware.

**Completeness gaps (minor).** (1) No explicit **measurement-validity** plan for the +30% comprehension
instrument — a homegrown pre/post quiz can be invalid; consider adapting validated items (e.g. the "Big
Three"/Big Five financial-literacy questions from Lusardi-Mitchell, which are openly used). (2) The
**effectiveness evidence base is mixed** and the plan should cite it honestly: older work found tiny
effects (Fernandes/Lynch/Netemeyer ~0.1% of variance) while the
[Kaiser-Lusardi-Menkhoff-Urban 2022 meta-analysis of 76 RCTs](https://www.nber.org/papers/w27057) finds
economically meaningful gains, *especially in budgeting, saving, and credit* — i.e. exactly this plan's
core — though a 2024-25 publication-bias re-analysis trims the effect. This *supports* the plan's topic
focus and argues for "just-in-time"/actionable framing. (3) Sustainability depends on a credentialed
reviewer who is `TO BE SECURED`; the dated decision rule is good, but reviewer *recruitment* should
start now (M0), not at the M1 gate.

---

## 2. Competitive landscape

| Competitor | What it is | Strengths | Weaknesses / independence gap |
|---|---|---|---|
| **CFPB** ([educator tools](https://www.consumerfinance.gov/consumer-tools/educator-tools/)) | U.S. federal consumer-finance agency; AskCFPB, guides, library/educator tools | Authoritative; **explicitly public domain / freely reusable**; independent of sellers; research-based | U.S.-only; fragmented across the site, not a coherent plain-language curriculum; reading level often high; political/funding volatility for the agency itself |
| **Khan Academy + Bank of America "Better Money Habits"** ([bettermoneyhabits.bankofamerica.com](https://bettermoneyhabits.bankofamerica.com/en/khan-academy-partnership)) | Free videos/articles, EN+ES, since 2013; KA produces video with "no outside editorial control" | Free, polished, bilingual, ad-free, in-branch workshops, huge reach | **Bank-branded and bank-funded** — the independence question incarnate; US-centric; KA content not openly licensed for commercial reuse/derivatives; product ecosystem adjacency |
| **Practical Money Skills (Visa)** ([practicalmoneyskills.com](https://www.practicalmoneyskills.com/en/about.html)) | Visa's flagship program; 18 languages, 49 countries, deals with 49 US states | Multilingual, global, free lesson plans/games, enormous reach (11M+ pageviews/mo) | **Owned by a payment network** — direct conflict (cards/credit); not openly licensed; "financial education" adjacent to card products |
| **NGPF (Next Gen Personal Finance)** ([ngpf.org](https://www.ngpf.org/curriculum/), [terms](https://www.ngpf.org/terms/)) | Leading free US K-12 (gr 6-12) curriculum; 51k+ teachers, ~75% of US high-schoolers' schools | Excellent pedagogy, teacher PD, current, *some* CC licensing | **CC BY-NC 3.0 only — commercial reuse, and full open redistribution, prohibited**; teacher/classroom-shaped (not adult/immigrant/unbanked); US-only; stock images non-reusable |
| **MyMoney.gov / FLEC** ([mymoney.gov](https://www.mymoney.gov/)) | Federal aggregator of 22 agencies' resources; MyMoneyFive; EN+ES | PD, authoritative, central index | An *index*, not a coherent plain-language course; US-only; uneven; not accessibility/ESL-optimized |
| **Jump$tart Coalition** ([jumpstart.org](https://jumpstartclearinghouse.org/)) | Coalition + clearinghouse + national standards | Standards alignment; large resource directory | Many members are **industry/financial firms**; clearinghouse not curriculum; US-only |
| **Investopedia** ([Dotdash Meredith](https://en.wikipedia.org/wiki/Dotdash_Meredith)) | Reference/encyclopedia | Comprehensive, well-known | **Ad + affiliate revenue model** (Dotdash makes ~2× on commerce/affiliate per visit) — structurally conflicted; reference not curriculum; reading level high; not for vulnerable/ESL learners |
| **GCFGlobal / GCFLearnFree (Goodwill)** ([edu.gcfglobal.org/en/edlmoney](https://edu.gcfglobal.org/en/edlmoney/)) | Goodwill-funded free "Money/Everyday Life" tutorials; EN+ES, no registration | Plain-language, nonprofit-funded (donated-goods revenue, **no product conflict**), accessible, free, well-regarded | Not openly licensed (copyrighted, not CC); not citation-driven; US-centric; light on predatory-lending/scam depth |
| **Banks' own fin-lit (generic)** | Lender/fintech "education" hubs | Free, polished | **Lead-gen / marketing** — the category the plan defines itself against; conflict of interest is well-documented ([Brookings](https://www.brookings.edu/articles/financial-literacy-what-works-how-could-it-be-more-effective/)) |

**The structural finding** the research confirms: the conflict-of-interest critique is real and
documented — "there is a fundamental conflict of interest for a product provider to offer just-in-time
education that could turn out to undermine the sale of the company's product" ([Kitces](https://www.kitces.com/blog/financial-literacy-program-effectiveness-just-in-time-training-by-financial-advisors/)),
and policy literature flags "limits based on issues related to the independence and credibility" of
privately-funded education. **The two best-positioned-on-independence incumbents — CFPB (PD, independent)
and GCFGlobal (Goodwill, no product) — are precisely the ones that are NOT openly licensed-as-a-coherent-
adult-curriculum / not citation-engineered / US-only. That gap is the opening.**

---

## 3. Gaps we can fill

1. **Independent *and* openly licensed.** Independent sources (CFPB, GCFGlobal) aren't CC-BY-reusable-as-a-
   curriculum; openly-ish sources (NGPF) are CC BY-**NC** (no commercial reuse, e.g. a CDFI or social
   enterprise can't build on them). No one ships *independent + CC-BY-4.0 + coherent plain-language adult
   curriculum*. This is the white space.
2. **Adult / immigrant / unbanked audience.** Incumbents skew K-12 classroom (NGPF) or general consumer
   (BoA/Visa). The under-served, low-literacy, ESL, refugee, unbanked audience is under-served by a
   *coherent, vetted, handoutable* curriculum.
3. **Jurisdiction-honesty.** Almost every incumbent is silently US-only (or single-country). A genuinely
   jurisdiction-neutral core with labeled, locally-reviewed overlays does not exist as an open artifact.
4. **Provable non-commercial-ness + provenance.** A *legible*, audited "no sponsor, every claim sourced,
   stale figures withheld" artifact a librarian/caseworker can trust on sight — no incumbent makes this
   machine-checkable.
5. **Privacy-by-construction tools.** Stateless, client-side calculators that store/transmit nothing — vs.
   bank/fintech calculators that are lead-gen funnels.
6. **Predatory-lending & scam literacy as a first-class module**, grounded in FTC/CFPB enforcement, for
   the exact audience that is most targeted — thin or absent in most "saving/investing"-led curricula.
7. **Plain-language + WCAG + multilingual as gates**, not afterthoughts.

---

## 4. Differentiators to win

**The single strongest differentiator: structurally provable INDEPENDENCE from the financial industry,
made machine-checkable.** Every major free competitor is funded by a bank (BoA/KA), a payment network
(Visa), an ad/affiliate publisher (Investopedia), or carries industry-member coalitions (Jump$tart) — and
the credibility cost of that is documented in the literature. Even the clean ones (CFPB, GCFGlobal) don't
combine independence with open licensing and a coherent adult curriculum. Hee-Lee Oss can own
"**the financial literacy you can trust *because* no one profits from your decisions** — and you can
prove it: no sponsor, CC-BY-4.0, every claim sourced, a CI linter that fails the build on product steering."

Supporting differentiators:
- **CC-BY-4.0 (vs NGPF's CC BY-NC, vs everyone else's all-rights-reserved):** a CDFI, library, or social
  enterprise can *build on and redistribute* our content. Genuinely open, not "free to view."
- **Jurisdiction-honest by construction** (vs silent US-default everywhere).
- **Privacy-by-construction tools** (vs lead-gen calculators).
- **Staleness fail-safe + version-scoped sign-off** (vs silently-rotting incumbent content).
- **Non-shaming, structurally-honest voice** for vulnerable learners (vs moralizing/poverty-blame common
  in the genre).
- **Predatory-product/scam literacy** centered on the targeted audience, grounded in enforcement data.

vs **Khan/NGPF specifically:** beat NGPF on *audience* (adult/immigrant/unbanked vs gr 6-12), *license*
(CC-BY vs CC-BY-NC), and *jurisdiction-honesty*; beat Khan/BoA on *independence* (no bank) and *open
reuse*. Don't try to out-produce their video polish — win on trust, openness, reach into under-served
audiences, and reusability.

---

## 5. Claude API leverage — and the hard limits

**Where Claude adds leverage (authoring-only, behind the neutral client — never learner-facing at launch,
per plan):**
1. **Plain-language drafting + reading-level compression.** Draft/rewrite lessons from cited PD sources
   (CFPB, FTC, FLEC) to a grade-6/8 target, generate the simplified-English layer, and flag sentences
   above target for the plain-language reviewer. High value for the ESL/low-literacy audience.
2. **Scam/predatory-pattern scenario generation.** Turn real FTC/CFPB enforcement patterns into concrete,
   *non-fear-based*, brand-neutral "spot the red flag" scenarios and verification checklists — synthetic
   examples avoid naming real brands (product-neutral) while staying true to real tactics.
3. **Powering the product-neutrality / not-advice linter and review.** Claude as a *flagging* layer:
   detect advice-phrasing ("you should buy/choose"), unflagged-jurisdiction terms, advice-creep in
   "illustrative" numbers, brand mentions, and shaming/moralizing tone — surfacing candidates for the
   human reviewer (the linter fails CI; Claude widens recall beyond regex).
4. (Secondary) **Translation drafting + glossary/term extraction + source-summarization** for reviewer
   triage, citation-coverage checks, and i18n string externalization.

**Where Claude must NOT decide (hard gates — these are the project's identity):**
- **Never gives personalized financial advice** — no "what should I do," no product/fund/ticker picks;
  the education-vs-advice line is human-owned. A live learner-facing LLM is correctly out of scope.
- **Never the final word on accuracy or sourcing.** No claim ships on Claude's say-so; a credentialed
  AFC®-or-equivalent signs off, version-scoped. Claude must **never fabricate figures, rates, statistics,
  or citations** — every number traces to a verified open source with `lastVerified`/`validUntil`.
- **Never decides jurisdiction-correctness** — a US-PD source does not make a claim globally true; a local
  expert owns overlays.
- **Never decides the independence/product-neutrality line** — Claude flags, humans rule; a missed
  product-steering or missed non-commercial-redirect is a release-blocking QA failure.
- **No learner data** ever touches the model (there is none; tools are client-side).

---

## 6. Ten concrete optimizations

1. **Publish a verifiable "Independence & Funding" statement** (no bank/lender/fintech/network funding or
   relationship) as a first-class, machine-readable artifact — make non-sponsorship *legible*, since that
   is the moat.
2. **Adopt validated comprehension items** (e.g. Lusardi-Mitchell "Big Three/Five") as the spine of the
   pre/post instrument so the +30% claim is measurement-valid, not homegrown.
3. **Build an "advice-creep" golden-test corpus** of borderline phrasings (illustrative-number-as-benchmark,
   snowball/avalanche framing) for the linter + reviewer, with documented rulings in the charter.
4. **Expand the linter's unflagged-jurisdiction denylist** beyond US/UK (credit score, 401(k), ISA) to the
   subtle cases (overdraft, checking/current account, "credit," riba/Islamic-finance assumptions).
5. **Vet and maintain the non-commercial-redirect target list** (screen "nonprofit" counselors for industry
   ties / debt-management upsell; jurisdiction-tag each).
6. **Ground the scam module in live FTC/CFPB enforcement patterns** and add a non-shaming "if it already
   happened, report to a public agency (not credit-repair)" path.
7. **Make readability + plain-language a per-language gate** (English grade metrics don't transfer); require
   native-speaker plain-language review, not back-translation; support RTL/non-Latin scripts.
8. **Seed the curriculum directly from PD/CFPB/FLEC source maps** — pre-build a claim→source matrix so
   citation coverage starts at 100% by construction, not retrofitted.
9. **Add a funding-source COI screen** for any future funded reviewer-hours lane, with public disclosure,
   so independence survives a funding model.
10. **Ship structured exports (glossary JSON, lesson metadata, claim→source records)** so CDFIs, libraries,
    and sibling OER projects can *build on* (CC-BY) the corpus — convert "open license" into actual reuse.

---

## 7. Parallel & perpendicular spin-offs

The reusable asset here is a **sourced-education engine**: a charter + product-neutrality/advice linter +
per-claim provenance + staleness fail-safe + plain-language/i18n/a11y pipeline + version-scoped credentialed
sign-off + privacy-by-construction client-side tools. That engine generalizes to any *high-stakes,
trust-sensitive, jurisdiction-varying, "education-not-advice"* domain:

- **`benefits-navigator`** (public assistance / benefits eligibility): same education-not-advice line,
  same jurisdiction-overlay model, same non-commercial-redirect — direct reuse; shares the immigrant/
  low-income audience and is a natural cross-link from the budgeting module.
- **`microbusiness-toolkit`** (informal/micro-entrepreneur basics): reuses the calculators, plain-language
  pipeline, and product-neutrality rules; perpendicular audience (the same learners as earners).
- **`numeracy-from-zero`** (foundational math): upstream dependency — financial literacy presumes numeracy;
  shares readability/a11y/plain-language engine; feeds the same ESL/low-literacy learners.
- **`know-your-rights`** (consumer/tenant/worker rights): reuses provenance + jurisdiction-overlay + the
  "route to public, non-commercial help" pattern; pairs with the predatory-lending module.
- **`media-literacy-curriculum`** (spotting misinformation/scams): the scam/verification module is a
  bridge; shares the "recognize *and verify*" pedagogy and the non-fear-based framing.
- **A standalone `sourced-education-engine` / OER toolkit** (charter + linter + provenance/staleness schema
  + a11y/i18n pipeline) that any Hee-Lee Oss education project can adopt — the highest-leverage extraction.

---

## 8. Open questions

1. **Reviewer recruitment timing/funding.** The credentialed AFC® reviewer is the critical-path blocker;
   should recruitment + a funded-but-independence-screened reviewer-hours lane start in M0 rather than at
   the M1 gate? How is funding-source COI disclosed?
2. **First jurisdiction overlay.** Which country, scored by PD-source availability + local reviewer +
   underserved audience reachable via a partner? (Open in plan.)
3. **Pilot languages.** Driven by the secured partner's audience — but which, and with RTL/script support?
4. **Measurement validity.** Adopt validated items vs. homegrown quiz; what's the honest, partner-
   administrable, no-PII instrument?
5. **Effectiveness framing.** Given the mixed literature (small older effects vs. meaningful 2022 RCT
   meta-analysis, especially for budgeting/saving/credit), how aggressively to claim impact, and should the
   curriculum lean "just-in-time"/actionable to maximize behavior change?
6. **Redirect-target governance.** Who maintains and vets the non-commercial help list per jurisdiction?
7. **Live learner-facing assistant.** Stay gated-backlog (default no), given the full guardrail-port cost?
8. **License inheritance.** CC-BY vs CC-BY-SA segregation if any share-alike source is used — keep the
   corpus cleanly CC-BY-reusable.

---

## Sources
- CFPB educator/library tools (PD reuse): https://www.consumerfinance.gov/consumer-tools/educator-tools/
- Khan Academy × Bank of America Better Money Habits: https://bettermoneyhabits.bankofamerica.com/en/khan-academy-partnership ; https://www.businesswire.com/news/home/20130409005152/en/Bank-of-America-Khan-Academy-Promote-Better-Money-Habits
- NGPF curriculum: https://www.ngpf.org/curriculum/ ; license (CC BY-NC 3.0): https://www.ngpf.org/terms/
- Practical Money Skills (Visa): https://www.practicalmoneyskills.com/en/about.html
- MyMoney.gov / FLEC: https://www.mymoney.gov/ ; https://www.mymoney.gov/mymoneyfive
- Jump$tart clearinghouse: https://jumpstartclearinghouse.org/
- Investopedia / Dotdash Meredith (ad+affiliate model): https://en.wikipedia.org/wiki/Dotdash_Meredith
- GCFGlobal money tutorials (Goodwill): https://edu.gcfglobal.org/en/edlmoney/ ; https://en.wikipedia.org/wiki/GCFGlobal.org
- FTC payday/predatory-lending enforcement: https://www.ftc.gov/news-events/press-releases/2020/05/ftc-halts-deceptive-payday-lender-took-millions-consumers
- Effectiveness: Kaiser/Lusardi/Menkhoff/Urban 76-RCT meta-analysis: https://www.nber.org/papers/w27057 ; Brookings overview: https://www.brookings.edu/articles/financial-literacy-what-works-how-could-it-be-more-effective/ ; conflict-of-interest critique: https://www.kitces.com/blog/financial-literacy-program-effectiveness-just-in-time-training-by-financial-advisors/
