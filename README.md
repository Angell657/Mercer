# Mercer 🛠️

**Local-first engineering director and development orchestrator.**

Mercer proactively keeps software, design, engineering and fabrication projects moving. Instead of requiring a new instruction for each bit of housekeeping, Mercer notices opportunities, delegates bounded tasks, validates results and presents decisions that genuinely need the owner.

**Concept stage:** this repository currently defines goals and architecture, not an operational AI agent.

## Responsibilities
- **Repository management:** indexes, newly added files, cross-references, consistent documentation, issue triage, housekeeping branches and reviewable commits.
- **Design discipline:** requirements, decisions and their *rationale*, traceability, change-impact reviews, canonical data and validation.
- **Software and games:** agent-assisted coding, testing, asset organization and worldbuilding continuity across vehicles, manufacturers, NPCs and histories.
- **Hardware and CAD:** design iterations, bill of materials, fabrication preparation and prototype/test records.
- **Agent coordination:** manage scoped tasks for specialized agents, monitor outcomes and escalate conflicting requirements.

## Example
Three new Kessler Sora reference images appear in the racing repo. Mercer detects them, associates them with the known vehicle, refreshes the image index, checks naming conventions and proposes a new manufacturer/vehicle taxonomy. Simple reversible housekeeping can be committed on an approved branch; a large world-data reorganization requires review.

## Team boundaries
| Entity | Function | Relationship |
| --- | --- | --- |
| **Mercer** | Engineering, software, mechanical designs, delegated work | Owns technical workflows |
| **Alden** | Household operations | May request an investigation or propose improvements |
| **Wobble** | Independent companion | Mercer may maintain/test Wobble's software, but does not control personality or daily behavior |
| **Owner** | Vision, decisions, approvals | Holds ultimate authority |

**Candidate projects:** [Racing-Game](https://github.com/Angell657/Racing-Game), [3D-Printer](https://github.com/Angell657/3D-Printer), [Project-Wobble](https://github.com/Angell657/Project-Wobble), the food-planning app, Project Hansel/Gretel and Mechmap. Connect repositories **individually and explicitly**, not by granting automatic access to every account resource.

## Autonomy tiers
1. **Allowed within approved scope:** read repo state, run existing tests, generate indexes, check links and create reversible housekeeping commits in designated branches.
2. **Review first:** architecture changes, schema changes, canonical lore/requirements modifications, significant migrations, new dependencies and main-branch merges.
3. **Explicit strong authorization:** deleting data, spending money, publishing, modifying secrets/access rights, deploying systems or starting fabrication/physical operations.
4. **Never:** bypass safety systems, exfiltrate credentials or silently overwrite approved requirements.

Treat LLM prompts, repo contents and third-party inputs as untrusted. Use sandboxed tool execution, scoped credentials, allowlisted actions, logs and rollback.

## Concept architecture
```text
Owner / Dashboard / CLI / Notifications
                   |
Mercer coordinator + project memory
                   |
 Task queue + bounded specialized agents
                   |
 Policy / approvals / budgets / audit
                   |
GitHub | local repos | tests | CAD | docs | slicer (later)
                   |
 Validation / artifacts / change-impact report
                   |
 Decision log + status briefing
```

Prefer deterministic code for indexing, validation and applying changes. AI reasons about what work should happen, but validators and policies control execution. Preserve **FRS/design intent as the source of truth** where applicable, rather than allowing generated output to rewrite requirements.

## Roadmap
- [ ] Define shared task, agent capability, approval and audit schemas.
- [ ] Build a read-only repository crawler and project inventory.
- [ ] Add a decision-record format: decision, rationale, alternatives, date and impacted components.
- [ ] Implement safe housekeeping via previewable branches and tests.
- [ ] Build an engineering brief: work completed, unresolved issues and required decisions.
- [ ] Pilot with an approved low-risk project; record task success/failure and rollback.
- [ ] Extend to CAD, printer workflows and cross-project coordination only after validation.

## Proposed structure
```text
docs/         Vision, architecture, decision records, policies
agents/       Specialized worker configurations
connectors/   GitHub, filesystem, test and CAD adapters
services/     Planner, task queue, orchestration, memory
policies/     Access and approval rules
tests/        Unit, integration, agent behavior and safety cases
deploy/       Local installation and version-pinned configs
```

## Design goal
> “I've handled the routine work. Here are the two decisions that need you.”

*Engineering manager, not an unrestrained code-writing slot machine.*
