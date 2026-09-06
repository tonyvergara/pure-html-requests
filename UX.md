# UX.md — Shared Design & UX Foundation

> This document applies to every project built on this framework. It sets principles and defaults, not a locked visual system — individual projects (see their `design.md`) may have their own aesthetic inspiration, but should not contradict the philosophy here without a stated reason.

## 1. Core Feeling
Every product should feel **efficient, yet supportive**. The user should never feel like the app is wasting their time, but they should also never feel abandoned, judged, or confused when something goes wrong.

In practice:
- Default to the fastest path through a task. Don't add steps, confirmations, or decoration that don't earn their place.
- When the user is stuck, blocked, or has made an error, the tone shifts from "efficient" to "supportive" — slow down, explain plainly, offer a way forward.

## 2. Visual Direction
A mix of **minimal/clean** and **warm/friendly** — restrained, not sterile.

- Whitespace and restraint are the default. Only add visual weight (color, borders, shadows) where it carries meaning (state, hierarchy, action).
- Warmth comes from tone of language, rounded/soft details, and forgiving micro-interactions — not from heavy decoration.
- Avoid both extremes: not corporate/cold, not playful/gimmicky.
- Individual projects choose their own palette/typography/inspiration in their `design.md`. This doc governs *how* those choices are applied, not the specific tokens.

## 3. UX Principles (decision-making rules)
When a design or interaction decision isn't specified elsewhere, resolve it using these, in order:

1. **Clarity over cleverness.** If a user has to think about how the UI works, simplify it, even if the clever version looks nicer.
2. **Fewest steps that still feel safe.** Cut friction, but don't cut confirmation on destructive/irreversible actions.
3. **Show, don't block.** Prefer inline feedback (validation, loading states, empty states) over interrupting modals or dead ends.
4. **Fail kindly.** Errors are expected, not exceptional — write error states as if explaining to a person, not logging a stack trace.
5. **Consistent before novel.** Reuse an existing pattern in the product before inventing a new one, even if the new one is slightly better — novelty has a learning-curve cost.

## 4. Interaction Patterns

**Navigation**
- Keep primary navigation shallow — favor flat structures over deep nesting.
- The user should always be able to tell where they are and how to get back.

**Forms**
- Validate inline, as the user types or on blur — not only on submit.
- Errors point to the specific field and say what to do, not just what's wrong.
- Preserve user input on error. Never make someone retype something because of a validation failure.

**Feedback & Loading**
- Any action taking >300ms gets a loading indicator; anything longer gets a way to know it's still working (progress, skeleton, or status text).
- Confirm success unobtrusively (toast, inline check) rather than with a blocking modal, unless the action is significant/irreversible.

**Errors & Empty States**
- Empty states explain what goes here and how to fill it — they're an onboarding opportunity, not a dead end.
- Error messages are written in plain language, say what happened, and suggest a next step. Avoid raw technical detail unless the audience is technical.

**Destructive/Irreversible Actions**
- Always require explicit confirmation.
- Prefer undo (where feasible) over a confirmation dialog — it's faster for the common case and still safe.

## 5. Accessibility Baseline
Non-negotiable minimums for every project, regardless of visual style:
- Sufficient color contrast (WCAG AA as a floor).
- All interactive elements keyboard-navigable and focus-visible.
- Meaningful labels/alt text — never rely on color or icon alone to convey state.

## 6. Voice & Tone
- Plain, direct language. Avoid jargon unless the audience is expected to know it.
- Friendly but not chatty — warmth comes from clarity and respect for the user's time, not from filler or forced personality.
- Never blame the user in copy ("Invalid input" → "That email doesn't look right — check for typos").

## 7. How Project-Level design.md Should Reference This
Each project's `design.md` should:
- Note any place its specific direction deviates from this document, and why.
- Inherit Sections 3–6 (principles, patterns, accessibility, voice) by default unless explicitly overridden.
- Feel free to fully define its own Section 2-equivalent (palette, type, specific visual inspiration).
