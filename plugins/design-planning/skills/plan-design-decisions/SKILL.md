---
name: plan-design-decisions
description: Run an adaptive question-and-answer workflow that turns product and visual design decisions into an implementation-ready plan. Use when a user wants to plan or scope a website, application, feature, redesign, prototype, slide deck, document, design system, or other designed artifact; clarify UI/UX or visual direction; compare design alternatives; prepare design decisions for implementation; or convert a rough product idea into sequenced design work. Produce the plan but do not implement it unless the user separately asks for implementation.
---

# Plan Design Decisions

Interview the user to turn ambiguous design intent into a clear, defensible, implementation-ready plan. Adapt the depth to the size and risk of the work.

## Set the boundary

- Plan design work; do not modify files or implement the design unless the user separately authorizes implementation.
- Treat the interview as collaborative discovery, not a fixed questionnaire.
- Ask only questions whose answers could change the plan.
- Inspect any accessible product, brief, codebase, screenshots, brand system, research, or design guidance before asking about information already available.
- Preserve existing requirements and distinguish them from new recommendations.

## Run the interview

Ask one focused question at a time by default. When an interactive question tool is available, use it for bounded choices; otherwise ask directly in plain language. Offer two or three concrete options when that makes the decision easier, put the recommended option first, and explain its tradeoff briefly.

If the user is unsure, propose a reasonable default and let them confirm or correct it. Do not stall on low-risk uncertainty. Record unresolved high-impact questions for the final plan.

Move through these topics adaptively rather than mechanically:

### 1. Outcome and scope

Establish:

- what product or artifact is being designed;
- what change or decision prompted the work;
- the practical outcome the user wants;
- what is in scope and explicitly out of scope;
- whether this is exploration, a prototype, production work, or a revision.

Begin with the single question that most reduces ambiguity about the desired outcome.

### 2. Audience and use

Clarify:

- the primary audience and any important secondary audience;
- the task, need, or situation that brings them to the product;
- what they should understand, feel, decide, or do;
- relevant device, environment, time, attention, ability, or familiarity constraints;
- known research versus assumptions about users.

Do not invent personas or claim assumptions are research.

### 3. Current state and inputs

Identify:

- what exists today and what is working or failing;
- the content, features, flows, or visual assets already available;
- established brand, design-system, accessibility, technical, and format requirements;
- stakeholder commitments or earlier decisions that must be preserved;
- comparable products or references the user wants to emulate or avoid.

When a workspace is available, inspect it first and ask the user to confirm only consequential interpretations.

### 4. Decisions and direction

Surface the design decisions that will materially affect the outcome. These may include:

- information hierarchy and content sequence;
- navigation and interaction model;
- primary actions and workflow;
- page, screen, slide, or component structure;
- tone, imagery, typography, color, density, and motion;
- responsive and accessibility behavior;
- states such as loading, empty, error, success, selected, and disabled;
- system reuse versus new patterns.

For each consequential decision, capture:

1. audience need;
2. project goal;
3. recommended choice;
4. evidence, constraint, or principle supporting it;
5. credible alternative;
6. tradeoff or risk;
7. how to verify the choice.

Do not ask the user to make low-level aesthetic choices without context. Translate vague preferences such as “modern,” “premium,” or “simple” into observable qualities and examples.

### 5. Delivery and validation

Clarify:

- required deliverables and final formats;
- implementation environment and ownership;
- dependencies and sequencing constraints;
- deadline or release stages;
- review and approval participants;
- accessibility, usability, content, visual, technical, and final-format checks;
- what evidence will indicate success after release.

Scale validation to risk. Prefer small reversible checks before expensive irreversible work.

## Manage the conversation

- Maintain a compact working brief from the user's answers.
- Periodically summarize decisions when the conversation becomes long or a phase closes.
- Label statements as **confirmed**, **assumed**, **recommended**, or **open** when the distinction matters.
- Reconcile contradictions explicitly instead of silently choosing one answer.
- Explain why a sensitive or seemingly indirect question affects the plan.
- Stop interviewing when remaining answers would not materially change scope, direction, sequencing, or acceptance criteria.
- Allow the user to request an early plan; mark gaps and use reasonable defaults.

## Build the plan

Produce a self-contained plan that does not require the reader to reconstruct the interview. Use only as much detail as the work warrants.

### Required structure

1. **Outcome** — one paragraph describing the artifact, audience, intended result, and scope.
2. **Decision brief** — confirmed requirements, assumptions, constraints, and exclusions.
3. **Design decisions** — a compact table with decision, recommendation, rationale, tradeoff, and verification.
4. **Implementation sequence** — ordered workstreams or steps with dependencies and concrete outputs.
5. **Acceptance criteria** — observable conditions for completion, including accessibility and required states or formats.
6. **Validation plan** — what to review or test, when, with whom, and what would trigger revision.
7. **Risks and open questions** — only unresolved items that could affect delivery, with an owner or proposed resolution.

### Implementation sequence rules

- Sequence foundations before polish: content and requirements, structure and flow, system decisions, core build, states and responsiveness, content integration, validation, refinement, and release checks.
- Name likely files, components, screens, slides, or artifacts when they are known from inspected context.
- Separate required work from optional enhancements.
- Identify dependencies, decision gates, and parallelizable work.
- Give each step a verifiable completion condition.
- Avoid estimates unless the user asks for them and enough delivery context exists.
- Avoid turning the plan into generic design advice; tie every step to the product described.

## Quality check

Before delivering the plan, verify that:

- every major recommendation connects to an audience need or project goal;
- known facts and assumptions are distinguishable;
- credible alternatives and tradeoffs appear for consequential choices;
- accessibility and non-happy-path states are included where relevant;
- the implementation order respects dependencies;
- acceptance criteria are observable rather than subjective;
- validation matches the risk and medium;
- no unresolved question is presented as a settled decision;
- the plan is actionable without authorizing implementation.
