# TODO — Gaps in v1 (2026-05-28 audit)

Authored by Artemis after fresh-eyes pass on README, STRATEGY.md, leads.json. Goal: more Maggiano's-style deals (upscale-casual, design-forward, 10–70 units, real hardwood + leather, single design/dev VP as decision-maker, FF&E spend that justifies custom).

## This week (ship blockers for Trip A)

1. **Build the Maggiano's tear-sheet.** One page. Photo + spec + per-location operating-cost data Peter already has. Strategy treats this as the single highest-leverage artifact in any 5-minute meeting and it doesn't exist yet. Without it, every trip ships under-armed.
2. **Build the printed lookbook.** 50 units, foil-stamped, completed HI projects: Nikki Beach, Hyatt Place Boca, Joia, Boatyard. ~$40/unit. Prerequisite: confirm HI has print-quality photography of all four projects. If not, that's the actual blocker.
3. **Ask Peter for his Maggiano's-era Brinker warm-network names.** One question over coffee: "who from your Brinker years is now a VP at one of these brands or a peer who would walk us in?" Strategy flags this as the best lead source not on the list. Five days since authored. Log answers to `peter-warm-network.md`.

## Data model changes (leads.json schema)

4. Expand `status` enum from `cold | active` to: `cold | contacted | replied | meeting-set | meeting-held | sample-sent | in-spec-review | won | lost`. Binary states can't render a funnel.
5. Add `last_touched_at` and `next_action_at` (ISO dates) per lead. Without them leads rot silently.
6. Add `expected_value_usd` per lead — single-deal estimate, plus a separate `lifetime_value_usd` for designer/GC cards. Tier letters answer fit, not size. FRC win opens four brands x N units/year for years; Earls Boston Seaport is one build. They are not both "A."
7. Add an `events` array per lead — `{date, type, who, note}`. Type: call, email, meeting, sample-shipped, voicemail. So three weeks from now we know who's been touched and don't look amateur on follow-up.

## Promote first-class cards

8. **Designers as their own lead cards** (currently buried inside brand entries): Aria Group Architects, Studio Murnane, Meyer Davis Studio, NELSON Worldwide, Shepley Bulfinch. Strategy is explicit that landing one designer spec-list spot pays a decade of automatic leads. Aria alone outranks most brands on lifetime value.
9. **GC stable as their own lead cards**: Jokake Construction, MCI Builders, R.C. Mathews Contractor, Encore Construction. Same shape — recurring relationships, free referrals on the next build.

## UI (index.html)

10. **Trip-mode view.** Filter by Trip A / B / C, ordered by anchor meeting, with addresses and active-build sites surfaced. Peter packing for Phoenix should not be mentally cross-referencing leads.json against STRATEGY.md.
11. **Windows-closing-in-30-days badge.** Compute from `expansion_intel` open dates. North Italia Katy opens June 10 — the active-build drop-in window closes in 13 days and nothing in the UI is shouting about it. Same for permit-stage builds.
12. **Click-through to LinkedIn / source_url from prime_contacts.** Currently surfaced in JSON, should be one-tap in the card.

## Risk hedges

13. **Peter dependency.** He's the closer AND the only traveler in the plan. Trips A+B+C are weeks 5–13 of Peter's calendar. Either confirm he's bought in to that cadence, or design a Plan B where Michael flies the lower-stakes designer sample drops and Peter only flies the anchor meetings.

## Backlog (research, not blocking)

14. L Catterton operating partner overseeing bartaco / Barcelona Wine Bar / Uncle Julio's. Land that one person, three brands open at once.
15. Sumeet Mittal's replacement at Earls (VP Construction & Facilities). Still unconfirmed publicly. Defer Earls outreach until identified.
16. True Food Kitchen development lead under the new (unnamed) CDO — Slemons-to-Sweetgreen correction means that seat status is unknown. Direct outreach to Jonathan Perez (CAO/GC) to identify the dev lead.
