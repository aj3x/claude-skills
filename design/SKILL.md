---
name: design
description: Function-first design guidance for UI, UX, product, information, and visual design. Use when designing, critiquing, or reviewing interfaces, screens, components, layouts, flows, charts, copy structure, APIs/CLIs as user surfaces, or any object meant to be used; when choosing between aesthetic options; when asked to "make it look better/cleaner/simpler/modern"; or when deciding whether to add, keep, or remove an element, animation, or feature.
---

# Design: function first, nothing needless

## Stance

Good design is the shortest honest path between a person and what they are trying to do. Form and function complement each other, and in the best work you cannot tell them apart. Form follows function (Sullivan); less, but better (Rams).

**Precedence rule: when form and function conflict, function wins. Always.** Beauty is earned by clarity, proportion, and fit, never bought with usability, speed, accessibility, or honesty. Nothing needless, nothing frivolous: every element must justify its existence by a job it does.

Quiet is not blandness. The goal is design that disappears into use (Rams' "neutral tools", Morrison and Fukasawa's "supernormal", Muji's "emptiness"), not design that announces itself.

## Decision procedure

Run for each element, feature, style choice, or animation:

1. **Whose task is this serving?** Name the user and the goal in a sentence. If you cannot, stop and find out.
2. **What job does this element do?** (inform, enable an action, group, orient, give feedback, build trust, aid recognition). No job: delete it.
3. **Can it be removed, merged, or deferred?** Try removing it. If nothing is lost, it stays removed. If one thing is lost, ask whether a simpler element could carry it.
4. **Does it hurt any task?** Check speed, clarity, error rate, accessibility, load, attention. Any measurable harm to function loses to function, however nice it looks.
5. **Is the simplest version honest and complete?** Prefer the conventional pattern unless there is a functional reason to deviate (Jakob's Law).
6. **Then refine the form**: alignment, spacing, rhythm, hierarchy, consistency. Care at this stage is thoroughness (Rams #8), not decoration.

When two options function equally, choose the one with fewer parts, fewer states, and fewer words.

## Principles to practice

Attribution is in `references.md`. Paraphrased, not quoted.

| Principle | In practice |
|-----------|-------------|
| Rams: useful | Cut anything that does not serve the task. Features, colours, borders, icons, copy. |
| Rams: understandable | The interface explains itself. Labels over mystery icons; visible state; no manual needed. |
| Rams: unobtrusive | Chrome recedes, content leads. Neutral base palette, one accent for the primary action. |
| Rams: honest | No fake urgency, fake progress, inflated claims, or controls that pretend. Loading shows real state. |
| Rams: long-lasting | Avoid trend tics (glass, gradients-for-their-own-sake, novelty layouts). Use durable type, grid, and tokens. |
| Rams: thorough | Edge cases, empty/error/loading states, long strings, and tiny details are part of the design. |
| Rams: little design as possible | Reduce to the essentials, then check the essentials are right. |
| Hick's Law | Fewer, grouped choices. One primary action per view; progressive disclosure for the rest. |
| Fitts's Law | Frequent and primary targets are large and close to where the pointer/thumb already is. Minimum ~44px touch targets (24px CSS floor per WCAG 2.2). |
| Jakob's Law | Use familiar patterns (nav placement, form behaviour, icons). Novelty needs a functional payoff. |
| Miller's Law / chunking | Do not rely on counting 7 items; group information into meaningful chunks and keep the working set small. |
| Cognitive load | Show only what is needed now. Do not make people remember across screens; carry context forward. |
| Doherty threshold | Respond within ~400ms. Beyond that, show immediate feedback, skeletons, or optimistic updates; never block silently. |
| Tesler's Law | Complexity is conserved. Absorb it in the system (defaults, inference, automation), not the user, unless exposing it is the point. |
| Postel's Law | Accept varied input (spaces, formats, case); emit consistent, strict output. Validate gently, explain precisely. |
| Gestalt: proximity, common region, similarity, connectedness | Group by spacing before borders, borders before boxes. Spacing is the cheapest structure. Similar function, similar look. |
| Aesthetic-usability effect | Polish makes things feel easier and buys tolerance, but it can mask real usability faults. Test with real tasks; never use it as a reason to ship a flawed flow. |
| Von Restorff | Make the one important thing different. If everything is emphasised, nothing is. |
| Serial position, peak-end | Put key items first/last in lists and flows; make the final step and error moments considerate. |
| Zeigarnik, goal-gradient | Show progress on multi-step tasks and save partial work. |
| Tufte: data-ink | In charts and tables, every mark should carry data. Remove chartjunk, heavy gridlines, 3D, redundant legends; label directly. |
| Norman: affordances, signifiers, feedback | Controls look operable; every action gets visible acknowledgement; map controls to effects; make errors recoverable. |
| Vignelli / Müller-Brockmann | A grid, a tiny type scale, few typefaces, consistent spacing. Constraint creates coherence. |
| Munari / Aicher | Solve the problem with the fewest means; systems over one-offs; reuse components rather than inventing. |
| Krug | Do not make people think. Assume scanning, not reading. Obvious beats clever. |
| Wroblewski | Forms: fewer fields, top-aligned labels, inline validation, sensible defaults. Mobile-first forces priorities. |
| Frost (atomic design) | Build from small reusable parts with tokens; consistency comes from the system, not vigilance. |
| Tognazzini | Make state visible, protect user work, keep interactions reversible, favour direct manipulation, keep keyboard paths. |
| Ive / Rams craft | Resolve details until the object looks inevitable. Material honesty over ornament. |

## Review checklist

Function
- [ ] Primary task is completable quickly, with the primary action unmistakable.
- [ ] Every element has a nameable job; nothing decorative remains.
- [ ] Every interactive element has hover/focus/active/disabled/loading/error states.
- [ ] Empty, error, offline, slow, and long-content cases are designed.
- [ ] Actions are reversible or confirmed proportionally to risk.
- [ ] Copy is plain, specific, and action-oriented; errors say what happened and how to fix it.
- [ ] Familiar patterns used unless a functional reason says otherwise.

Form (only after function passes)
- [ ] Clear hierarchy: one focal point per view; squint test passes.
- [ ] Consistent grid, spacing scale, and type scale; few typefaces and weights.
- [ ] Colour is limited, purposeful, and never the sole carrier of meaning.
- [ ] Alignment and rhythm are exact; nothing is "almost" aligned.

Honesty and longevity
- [ ] No dark patterns, fake scarcity, or misleading affordances.
- [ ] Nothing depends on a passing trend.

## Anti-patterns

- **Decoration**: ornamental gradients, shadows, illustrations, icons beside every label, borders around everything, backgrounds that reduce contrast.
- **Gratuitous motion**: animation that delays a task, loops for attention, or parallax. Motion must explain a change (origin, hierarchy, state) and stay under ~200 to 300ms for UI feedback. Respect `prefers-reduced-motion`.
- **Dark patterns**: confirmshaming, hidden costs, pre-ticked opt-ins, disguised ads, roach-motel cancellation, nagging, fake countdowns, asymmetric buttons for accept/decline of equal consequence.
- **Mystery meat**: icon-only controls without labels or tooltips, gesture-only actions without a visible alternative.
- **Choice dumping**: settings and options in place of good defaults.
- **Reinvention**: custom scrollbars, non-standard form controls, bespoke navigation for its own sake.
- **Emphasis inflation**: everything bold, coloured, or badged.
- **Style over content**: designing the container before the content exists; lorem ipsum approvals.
- **Hiding with minimalism**: removing labels, affordances, or states to look clean. Minimal means essential, not missing.
- **Showcase-first**: the portfolio shot looks good, the empty and error states are blank.

## Baselines (non-negotiable)

Accessibility (WCAG 2.2 AA minimum)
- Text contrast 4.5:1 (3:1 for large text and UI boundaries/icons).
- Full keyboard operation, logical focus order, visible focus indicator.
- Semantic HTML first; ARIA only to fill gaps. Labels for all inputs; alt text for meaningful images.
- Never convey meaning by colour alone. Support zoom to 200% and text resizing without loss.
- Honour `prefers-reduced-motion` and `prefers-color-scheme`. No content flashing more than 3 times a second.
- Targets at least 24x24 CSS px, aim for 44x44 on touch.

Responsive
- Design content-first and mobile-first; layout adapts to content, with breakpoints set where the content breaks, not at device names.
- No horizontal scroll at 320px width. Relative units, fluid type, `min()`/`clamp()`.
- Body text ~16px minimum, line length ~45 to 75 characters, line height ~1.4 to 1.6.
- Touch and pointer both work; hover is never the only path.

Performance as design
- Fast is a feature: lean assets, no layout shift, system fonts or few web fonts, meaningful content before enhancement.

## When form may lead (narrow exceptions)

Form may take the lead only where it serves function. Each use must name the function:

- **Recognition**: brand mark, colour, or consistent visual signature that helps people identify and trust a product.
- **Trust and credibility**: professional polish where lack of it signals risk (payments, health, security).
- **Legibility and scanning**: typographic scale, whitespace, and contrast chosen to make reading and finding easier.
- **Emotional fit to the task**: tone matched to context (calm for medical, playful for children's learning) when mood affects completion or comfort.
- **Delight with a job**: a single, brief, skippable moment that confirms success or teaches a mechanic (never on frequent or blocking paths).
- **Art-directed contexts**: editorial, marketing, games, and portfolios where the experience itself is the product. Even there, navigation, reading, and purchase paths remain function-first.

If the exception cannot be stated as "this helps the user do X", it is not an exception.

## Working method

1. Write the user, task, and constraints in 2 to 3 sentences.
2. Content and structure first (information hierarchy, flow), visuals last.
3. Use real content, real data volumes, and real edge cases.
4. Start with the plainest conventional solution; add only what a test or a stated need justifies.
5. Review with the checklist; delete before you add.
6. When reporting a design decision, state the function it serves, and say explicitly if a pleasing option was rejected because it hurt function.
