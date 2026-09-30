---
name: grill-me
description: Turn an idea or ambiguous request into an approved, actionable brief through a focused collaborative interview. Use before planning or building non-trivial work when intent, scope, or constraints are unclear.
---

# Grill Me

Run a focused discovery conversation that replaces assumptions with decisions. Start from what the user has already said; do not ask questions whose answer is evident from the request or available project context.

Ask the highest-leverage unanswered questions first in an interactive format. Present one question at a time by default; combine up to three only when the choices are independent and answering them together is genuinely easier.

For every question, offer two to four concise, mutually exclusive answer choices that represent the meaningful decisions. Put the recommended/default choice first and state the practical trade-off for each choice. Always leave room for a custom answer (for example, an `Other` option or a short free-text reply). Do not manufacture choices when the answer needs open-ended context: ask a focused free-text question instead.

Use the client’s interactive choice controls when they are available. Otherwise, render the question and numbered options in chat and invite the user to reply with a number or their own answer. Treat an answer as a decision, record it, and adapt the next question rather than following a fixed questionnaire.

Prioritize decisions that would change the outcome:

- The problem, desired outcome, users, and observable definition of success.
- Scope, non-goals, affected workflows, and existing behavior that must remain intact.
- Constraints such as deadline, compatibility, platforms, security, privacy, budget, and operational expectations.
- Relevant examples, designs, data, integrations, and decision owners.

Adapt the interview to the work. For an existing codebase, inspect relevant context before asking the user to repeat information it can supply. For a small, unambiguous request, show the inferred brief and offer an interactive confirmation choice instead of prolonging discovery.

After enough information is available, produce a concise brief containing:

1. Goal and success criteria.
2. In scope and explicitly out of scope.
3. Constraints and notable context.
4. Decisions made, assumptions, and unresolved questions.
5. A recommended next action, usually `writing-plans` for an approved change.

Ask for approval of the brief with an interactive choice before handing off to the next action. Do not design, plan, or implement the solution while the user is still choosing requirements. Surface meaningful alternatives when a decision is genuinely open, but do not turn the conversation into a fixed questionnaire.
