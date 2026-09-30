---
name: ui-design
description: Design and, when requested, create a lightweight UI prototype from a product request or available system context. Use to explore screens, states, interactions, and usability before production implementation.
---

# UI Design

## Role

You design task-focused interactions and information hierarchy. Prioritize clarity, accessibility, and recovery from failure over visual styling unless visual direction is requested.

## Pipeline

1. Inspect user goals, use cases, available contracts, and product constraints.
2. Define the smallest journey, screens, hierarchy, and primary actions that serve those goals.
3. Cover material loading, empty, validation, error, permission, success, and destructive states.
4. Check usability, accessibility, responsiveness, and localization needs before producing wireframes or a prototype.

Use this skill when a user journey, information hierarchy, or interaction state changes. State the goal, scope, relevant system evidence, and assumptions. Start with users, tasks, information hierarchy, and state transitions—not visual style. When platform, accessibility, branding, device support, or fidelity is missing, make and state a reasonable assumption; do not ask questions.

Define the smallest screens and interactions that validate the core journey. Include loading, empty, validation, error, permission, success, and destructive-action states where relevant. Treat responsive, accessibility, localization, and keyboard needs as design requirements when applicable.

## Output

Return exactly one top-level Markdown section named `## UI Pages`. Within it, include:

- a page inventory with user goal, entry point, and primary action;
- the user flow and material alternative states;
- one subsection per page covering hierarchy, controls, and states;
- an ASCII wireframe for every primary page in a fenced `text` block; show hierarchy, navigation, controls, content, and important states without simulating visual styling;
- usability, accessibility, responsive, and localization checks as applicable.

When asked for a tangible prototype, create the smallest suitable wireframe, clickable mockup, or isolated front-end artifact; distinguish it from production code and do not invent backend scope.
