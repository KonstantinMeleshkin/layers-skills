---
name: layers-product-strategy
description: Connects user opportunities to business outcomes and solution bets — produces a strategy tree and prioritised experiments
---

# /layers-product-strategy

*Assumes `/layers-intro` has been loaded for framework context.*

Strategy is the first layer of the solution space — the point where problem space understanding converts into deliberate decisions about scope and direction. It is about choices: which user needs to serve, and which business outcomes to target.

**Decisions this layer needs to make:**
- What is the business outcome this work serves?
- Which user opportunities (needs, pains, desires) connect genuinely to that outcome?
- What solution bets are we placing on those opportunities?
- How do we test the riskiest assumptions cheaply?
- Which bets to pursue first, and why?

**Methods:**

| Method | When |
|---|---|
| **Opportunity Solution Tree (OST)** (Teresa Torres) | Default. Makes outcome → opportunity → solution → experiment connections explicit. Good for ongoing discovery cadences. |
| **Impact mapping** (Gojko Adzic) | B2B products with multiple stakeholders who each need to change behaviour. |
| **Jobs portfolio mapping** | Many job stories; need to decide which to target. Map by frequency, severity, and strategic fit. |
| **Now / Next / Later roadmap** | Team needs a shared timeline view of bets. Lightweight communication tool. |
| **Kano analysis** | Candidate features; understand which are hygiene (expected), performance (more is better), or delight (unexpected value). |
| **HEART / North Star** (Google / Amplitude) | Clarity on which outcome metric to target. HEART structures the choice; North Star distils to one metric representing core value. |
| **Wardley mapping** (Wardley) | Positioning depends on where capabilities sit on the evolution curve. Build/buy/partner decisions; spotting competitive moves. |
| **Bundling / unbundling** (Christensen) | Should this product own more of the workflow, or own one job precisely? Competitive positioning lens for established markets. |
| **NPE Canvas** | Consumer products: identify the Narrative (core user behaviour being tapped), Primitive (minimal atomic interaction), and Enablers (amplifying features). |
| **Critical User Journeys (CUJs)** (Google / Reforge) | Which flows to prioritise. A CUJ is the minimal path to realise core product value. Types: high-traffic, high-revenue, or metric-critical. |

Default: **Opportunity Solution Trees**.

**Quality signals — what good looks like:**
- The desired outcome is measurable, meaningful, and bounded — not "grow the product"
- Every opportunity is a customer need/pain/desire anchored to a specific journey moment — not a business metric or a solution in disguise (apply the flip test)
- Every opportunity in the tree connects to that outcome; unconnected needs aren't in this tree
- Every solution bet has a named assumption — what would have to be true for this to work?
- Every prioritised bet has an experiment that's the smallest possible way to validate the core assumption
- The tree shows options, not one inevitable path; multiple bets per opportunity

---

## Guided session

*Tell me what business outcome you're working toward and what user needs you have, or say "guide me" to start an OST session.*

Ask: *"Where should I capture the work from this session?"* (see `/layers-intro` for options)

Ask: *"Do you have job stories or user needs to work from, or are we building strategy from an informal understanding of the user?"* Note explicitly that strategy built without grounded user needs is a bet on assumptions.

Also ask: *"Is this a new product, a new feature on an existing product, or a strategic review of something in market?"*

---

**Phase 1 — Define the desired outcome**

The business result this work is trying to move. Not a feature, not a vanity metric — a genuine outcome that matters to the business.

Push toward specificity:
- Not "grow the product" but "increase users who activate in the first 30 days"
- Not "improve retention" but "reduce churn among users active 3–6 months"

A good outcome is measurable, meaningful, and bounded. If the team has multiple outcomes in mind, choose one for this tree.

**Phase 2 — Map the opportunities**

Opportunities are customer **needs, pain points, and desires**, written from the customer's perspective in the first person — "I don't know which streaming service has this movie", not a job story and not a feature. Three disciplines keep them honest (Teresa Torres):

1. **First-person, problem space.** Phrase as the customer would. Apply the **flip test**: if you can restate the opportunity as a feature, it's a solution in disguise — "order takeout" is a solution; "I don't have time to cook dinner" is the opportunity.
2. **Specific, not generic.** "I can't find something to watch" is too broad to solve. "I like intriguing sci-fi but not dumb action films, and I can't tell if I'll like this movie" is actionable.
3. **Grounded in a moment.** A well-framed opportunity happens in a specific moment, a specific context, for a specific customer. **Group the opportunities by journey moment** — this is the forcing function: it exposes vague opportunities and surfaces moments you've left unaddressed.

Not every customer need belongs in this tree — only those where serving it moves the business outcome. For each, ask: *"If we served this well, would it move the desired outcome? How?"*

Build from broad to specific within each journey moment — sub-opportunities are closer to actionable.

**Phase 3 — Generate solution bets**

For each prioritised opportunity, generate bets. These are lightweight hypotheses, not specifications.

Format: *"We could [solution], which we believe would [serve the opportunity] because [reasoning]."*

For each bet: What assumption is it most dependent on? Are there simpler ways to serve the same opportunity? Generate multiple bets per opportunity — resist early convergence.

**Phase 4 — Identify experiments**

For the most promising bets: what's the cheapest way to find out if the bet is right? Prototypes, fake door tests, concierge experiments, customer interviews about a specific scenario, data analysis. Days rather than months.

**Phase 5 — Build the strategy diagram**

Generate a strategy tree: desired outcome at the top, branching downward through opportunities (grouped by journey moment), solution bets, and experiments. Top-to-bottom orientation — the hierarchy reads as dependency, not sequence. In Mermaid: `graph TD`.

Ask: *"Does this tree reflect your current thinking? Branches missing, connections wrong?"*

**Phase 6 — Prioritise the bets**

Choose which bets to pursue first:
- **Opportunity size** — how many users, how often, how severely?
- **Assumption risk** — how uncertain is the core assumption?
- **Effort** — cost to build or test
- **Reversibility** — how hard to undo if it doesn't work?

Start with high opportunity size, manageable assumption risk, and a clear experiment path — not necessarily the most ambitious.

---

### Completion

Produce:
1. **Desired outcome**
2. **Opportunity tree** — Mermaid diagram, opportunities grouped by journey moment
3. **Prioritised solution bets** — top 2–3, with the experiment for each
4. **Deferred bets** — other bets worth returning to
5. **Open questions** — assumptions untested, needs not yet grounded in evidence

Close with: *"The solution bets chosen here define the scope of what needs to be designed. Next: define the conceptual model — the objects, relationships, and vocabulary those solutions will work with. Run `/layers-conceptual-model`."*

If user needs were weak or assumed: *"This strategy is built on assumed needs. Plan to validate them before committing to build."*
