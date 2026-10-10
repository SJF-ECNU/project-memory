## ADDED Requirements

### Requirement: Separate distribution roles
The repository SHALL publish core protocols, initialization skills and templates from main, and the desktop application from project-memory-app. Bundled initialization assets in the app SHALL be identified as dependencies of the core distribution.

#### Scenario: Default clone
- **WHEN** a user clones the default branch
- **THEN** the checkout contains the core Skill and templates without desktop or plugin source

#### Scenario: Application checkout
- **WHEN** a user selects project-memory-app
- **THEN** the README directs them to desktop and identifies main as the authoritative core source
- **AND** the erroneous core publication is counteracted with ordinary revert commits

### Requirement: Project Memory branding with data continuity
Current repository documentation and desktop display surfaces SHALL use Project Memory. Changing the desktop application name SHALL preserve the existing userData directory.

#### Scenario: Existing project list
- **WHEN** the branded application starts with an existing project list
- **THEN** the list is read from the same userData directory as before
- **AND** the window, document and side bar display Project Memory

#### Scenario: Existing initializer invocation
- **WHEN** a user invokes project-memory-init
- **THEN** the initialization Skill remains discoverable under that compatible identifier
