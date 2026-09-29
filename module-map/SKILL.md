---
name: module-map
description: Decompose a new project or feature into cohesive modules, responsibilities, use cases, and dependencies. Use after project goals are clear and before detailed data, API, or implementation design.
---

# Module Map

Map approved product scope into cohesive units of responsibility, starting from user journeys, business capabilities, and external boundaries—not frameworks, folders, or an assumed microservice topology.

For each module, define its purpose, owned concepts or data, primary use cases/functions, inputs and outputs, collaborators, and boundary with other modules. Keep closely changing behavior together; split only when ownership, lifecycle, operational needs, or coupling gives a concrete reason.

Present a module map, key use cases, dependencies and flows, boundary decisions, and open questions. Avoid turning every noun into a service or every method into a public module. Do not define tables, endpoint payloads, or implementation file structure unless asked.
