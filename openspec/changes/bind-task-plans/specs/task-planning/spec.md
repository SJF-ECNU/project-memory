## ADDED Requirements

### Requirement: One bound plan per task
Every new bounded task tracked as a workstream SHALL bind one task plan before substantive execution. A resumed workstream without a plan SHALL receive one based on current evidence, without rewriting historical logs. Ordinary questions SHALL remain outside this workflow.

#### Scenario: New task
- **WHEN** an agent starts a new tracked task
- **THEN** the workstream links one plan containing scope, approach, steps, acceptance criteria and unresolved questions
- **AND** the plan uses the same workstream identifier

#### Scenario: Existing task or OpenSpec design
- **WHEN** a task resumes with an existing suitable plan or OpenSpec design
- **THEN** that document is reused at its existing path without copying the design
- **AND** missing planning content is supplemented using current evidence

### Requirement: Progress and evidence follow the bound plan
Workstreams and new worklogs SHALL link the bound plan. Plan steps SHALL distinguish pending, active, completed, blocked and cancelled work, and completed steps SHALL cite verification evidence. Historical worklogs SHALL remain append-only.

#### Scenario: Task progress or scope changes
- **WHEN** an agent completes a step, encounters a blocker or changes scope
- **THEN** it updates the same plan's steps and the workstream summary
- **AND** the next meaningful closeout log records the evidence or reason and links the plan

### Requirement: Proportional planning and initialization
Initialization assets and local daily skills SHALL support the same plan lifecycle. A small task SHALL retain the core planning content without requiring service-specific design sections or a separate approval stage.

#### Scenario: Small documentation task
- **WHEN** a task has no scheduler, database or external resources
- **THEN** its plan covers the goal, scope, approach, verifiable steps, progress and unresolved items
- **AND** service-specific sections may be omitted

#### Scenario: Project initialization
- **WHEN** project memory is initialized
- **THEN** the project receives the task plan template and the initialization workstream binds a plan
- **AND** the generated daily skill instructs future tasks to read and maintain their bound plans
