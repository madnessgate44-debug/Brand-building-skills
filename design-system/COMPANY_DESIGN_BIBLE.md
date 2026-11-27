# Company Design Bible

**Version:** 1.0  
**Status:** Active foundation; product-specific visual systems are applied in sequence.  
**Owner:** Product design / frontend  
**Canonical design workspace:** [Miss Noor — Product Design System](https://www.figma.com/design/V6FT94iIIc07v8ccRh0uL2)  
**Scope:** Miss Noor, Gahiz, Smart Farm / الأستاذ بليغ, and future company products.

## 1. Purpose

This bible defines one coherent design and interaction language for the company's products. It does **not** force every product to look identical. Shared foundations govern usability, accessibility, motion, component behaviour, responsive rules, and quality. Each product receives a distinct brand skin suited to its audience and job.

The design system must produce working interfaces, not static decoration. A visual concept is not accepted until its interactions, states, responsive behaviour, and accessibility are specified and implemented.

## 2. Company-wide design principles

1. **Clarity before decoration.** One dominant task per view. Clear hierarchy, plain language, progressive disclosure, visible system status.
2. **Task-first composition.** Do not replace a working product with a generic dashboard or piles of cards. Preserve the user's mental model and existing navigation unless evidence justifies a change.
3. **Motion with meaning.** Motion teaches, guides attention, or confirms state. It must be brief, purposeful, interruptible, and never the only carrier of information.
4. **Real interaction.** Every control has defined states, feedback, keyboard/touch access, and a recovery path. No dead controls or fake functionality.
5. **Accessible by default.** Contrast, readable type, focus visibility, captions, touch targets, reduced motion, and assistive-technology semantics are acceptance criteria.
6. **Internationalisation at the foundation.** RTL and LTR are layout modes, not last-minute translations. Test real strings and mixed-direction content.
7. **Trust over theatre.** Never imply an AI response, voice, score, progress update, or data result happened when it did not.
8. **Preserve working behaviour.** Redesigns must not silently change curriculum, records, workflows, business rules, or data semantics.

## 3. Shared design tokens

Tokens are semantic. Components consume roles rather than hard-coded product colours.

### 3.1 Core roles

| Token | Default foundation | Usage |
|---|---:|---|
| `color.text.primary` | `#30251F` | Primary text |
| `color.surface.canvas` | `#FFF8EE` | Warm neutral canvas |
| `color.surface.default` | `#FFFFFF` | Raised/content surface |
| `color.border.subtle` | `#E8DCCB` | Quiet boundaries |
| `color.focus.ring` | `#245C9C` | Visible keyboard focus |
| `space.1` … `space.6` | 4, 8, 12, 16, 24, 32 px | Spacing scale |
| `radius.small` | 8 px | Small controls |
| `radius.medium` | 14 px | Standard surfaces |
| `radius.large` | 22 px | Large containers |
| `motion.micro` | 150 ms | Press/selection feedback |
| `motion.ui` | 240 ms | UI transitions |
| `motion.character` | 420 ms | Character gestures |

Product skins may override brand roles and neutral surfaces when justified. They must not weaken contrast, focus, touch, motion, or state contracts.

### 3.2 Miss Noor brand skin — selected warm direction

The owner selected the **first orange and warm-yellow visual direction** for Miss Noor. Use warm orange as the brand signal and sun-yellow as a highlight/reward colour. Keep the environment warm and bright, with dark readable text and calm neutral surfaces.

| Token | Value | Use |
|---|---:|---|
| `noor.canvas` | `#FFF8EE` | Warm page background |
| `noor.surface` | `#FFFFFF` | Lesson and reading surfaces |
| `noor.ink` | `#30251F` | Primary text |
| `noor.brand.primary` | `#B8471C` | Primary action, selected state, links |
| `noor.brand.orange` | `#E97832` | Illustration and non-text emphasis |
| `noor.brand.sun` | `#F2C45A` | Highlights, reward, progress accents |
| `noor.border` | `#E8DCCB` | Quiet dividers |

**Measured WCAG contrast for these pairs:** primary text on canvas 14.12:1; primary orange on white 5.31:1; dark text on sun-yellow 9.09:1; dark text on orange 5.10:1; muted text on canvas 6.56:1. Orange `#E97832` on white is 2.92:1 and must **not** be used for normal-size text or essential icons. Use the darker primary orange for text and controls.

The colour values define the selected direction, not a claim that the missing master artwork has been inspected. The handoff identifies approved art under `public/noor/*.webp` and `public/noor/cut/*.png`; those paths were not present in the inspected main tree. Do not redraw, replace, or reinterpret Noor's approved character art. Recover the exact selected first-set files before final character composition.

## 4. Typography

- Use the product's established typeface where verified; do not silently replace it during redesign.
- Define semantic roles: display, page title, section title, body, supporting, caption, control label, and numeric/data.
- Arabic and French need separately tuned line-height, wrapping, punctuation, and mixed-script behaviour.
- Child-facing reading screens must prioritise comfortable reading size; do not design to platform minimums.
- Never rasterise essential text into images. Provide scalable, selectable text and captions.

## 5. Layout, navigation, and responsive behaviour

- Design mobile-first; validate at 360 and 390 CSS px, then 768 and 1280 px.
- Preserve established primary navigation. Navigation is for destinations; contextual actions belong in the view.
- Use a consistent spacing scale and alignment system. Avoid arbitrary one-off gaps.
- Touch targets: at least 44 × 44 CSS px for primary interactive controls.
- Support safe areas, zoom/text scaling, long translations, loading, empty, error, offline, and success states.
- On narrow screens, prioritise the task and its next action; do not compress desktop layouts.

## 6. RTL and localisation

- Mirror layout direction, alignment, navigation order, and directional progress where appropriate.
- Do not mirror photographs, character artwork, logos, or scientific illustrations.
- Keep numerals, formulas, code, URLs, and mixed-language runs directionally stable.
- Mathematical number-line direction and chart axes require explicit locale review; do not assume that every visual should be mirrored.
- Arabic (Egyptian) and French are first-class in Miss Noor. Gahiz is English-first. Smart Farm is Arabic RTL-first.
- Every release must include real RTL and LTR screenshots for every supported locale.

## 7. Motion, animation, and sound

### Shared timing

- Micro feedback: 120–180 ms.
- UI transitions: 180–280 ms.
- Character gestures: 250–600 ms.
- Explanatory animations: paced to narration, with pause, replay, and step controls.
- Prefer ease-out for entrances. Use spring motion sparingly for playful reward, never for frequent or precision interactions.

### Mandatory behaviour

- Respect `prefers-reduced-motion` and provide an in-product reduced-motion setting where motion is central.
- No essential information may depend on animation or sound alone.
- Audio must not start unexpectedly. Provide pause, replay, mute, captions/transcript, and a clear error state.
- Synchronise speech, captions, and visible animation. Do not claim lip-sync unless it follows actual audio timing.
- Always provide a static or text alternative and learner/user-controlled pacing.

## 8. Interaction and component states

Every reusable control must define: default, hover (where relevant), focus, pressed, selected, disabled, loading, success, and error. Components must use semantic HTML and accessible names. Forms must explain validation and preserve entered data after recoverable errors.

## 9. Product design adapters

### Miss Noor — interactive learning studio

- Warm orange and sun-yellow direction; teacher-led, welcoming, story-rich.
- Noor is the teacher inside the lesson, not a decorative side widget.
- Preserve the four existing destinations and current architecture.
- Core journey: Noor greets and listens → learner chooses a passage → Noor introduces the goal → passage transforms into a visual model → Noor explains and gestures → learner manipulates/answers → Noor returns and checks understanding.
- Character states include idle, greeting, listening, speaking, explaining, thinking, encouraging, celebrating, and error/recovery. Expression and movement must remain consistent with the approved artwork.
- Voice requires actual speech playback, synchronised mouth/gesture timing, captions, replay, pause, mute, language choice, and graceful no-audio fallback.
- **Every lesson receives a pedagogically meaningful visual model and interaction.** Use a graph for quantitative relationships; a number line or manipulable objects for number concepts; a labelled diagram or simulation for science; a timeline/map for sequence and geography; animated word/sentence construction and pronunciation for literacy. Do not force a Cartesian graph onto a language lesson when it does not teach the concept.
- Learners can pause, replay, step through, manipulate, and answer. Record progress only after a real learner action.
- Lesson source and curriculum alignment must be verified before presenting content as authoritative.

### Gahiz — interview pressure simulator

- English-first, focused, mature, energetic, and credible; not childish.
- Make the practice loop unmistakable: scenario → prompt → timed response → evidence-based feedback → retry/progress.
- Under pressure, reduce competing decoration and cognitive load. Keep timer, current task, and response affordances legible.
- Never fabricate scoring, testimonials, outcomes, or AI evaluation. Clearly label unavailable capabilities.

### Smart Farm / الأستاذ بليغ — field assistant

- Arabic RTL-first, practical, grounded, and high-legibility.
- Prioritise field conditions, actionable alerts, units, recommendations, and clear next steps.
- Use diagrams, trend charts, maps, and status visuals only when they improve a real farming decision.
- Design for sunlight, large touch controls, intermittent connectivity, and clear stale/offline data states.
- Never imply live sensor data or automated action without a verified integration.

## 10. Design-to-build and release quality gates

A screen is not accepted on screenshot quality alone. Every product slice must pass:

1. Requirements and existing behaviour inspected before redesign.
2. Visual hierarchy and interaction flow specified.
3. Correct product tokens and approved assets used.
4. Responsive checks at 360 / 390 / 768 / 1280 px.
5. RTL/LTR checks for all supported locales.
6. Contrast and touch-target audit.
7. Keyboard, focus, semantic, and screen-reader review.
8. Reduced-motion and no-audio behaviour checked where relevant.
9. Loading, empty, error, offline, and success states handled.
10. Real source content/data and real interactions verified.
11. Build, tests, and changed-file diff inspected.
12. No merge or deployment without the required release authority.

## 11. Portfolio application order

1. **Miss Noor first:** establish the warm art direction, token implementation, and one complete interactive lesson; then generalise to the remaining lesson types and four destinations.
2. **Gahiz second:** apply shared foundations with its own performance-oriented product skin.
3. **Smart Farm third:** apply shared foundations with its own Arabic field-operations skin.
4. **Other active products:** inventory and apply the same foundations one product at a time.

## 12. Governance

This is the company-level source of truth for design foundations. Product-specific specifications may extend it but may not silently contradict it. Any exception must state the rationale, affected products, accessibility impact, and migration path. Changes to tokens require a version note and a check of every consuming product.
