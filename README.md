# Internal CRM Migration Case Study

[View the visual project portfolio](https://www.by-evamarquez.com/portfolio/internal-crm-migration). This repository contains sanitized delivery documentation, not private application source code.

Sanitized public case study of a private production CRM migration.

This repository does not publish the production CRM. It shows the problem,
architecture, rollout approach and representative data model used to replace an
Airtable-based operation with a custom internal tool for a 12-person team.

## What It Is

The production system became the operating layer for an agency team managing clients,
brands, projects, deliverables and ownership. It replaced an Airtable base that had
grown beyond what a spreadsheet-shaped workflow could support.

The public version is a case study. It is designed for reviewers who want to evaluate
technical project management, workflow design, migration judgment and internal-tool
thinking without seeing private client data or business logic.

## Problem

The team was coordinating daily work through Airtable. It worked until the process
became too complex:

- status fields were acting like workflow stages;
- filtered views were acting like role-specific screens;
- business rules lived in people's heads;
- delivery visibility depended on manually maintained fields;
- changes to the process became harder and riskier over time.

The real job was not just to move data. It was to identify the actual operating model
and design a system the team would keep using.

## My Contributions

- Process mapping across clients, brands, projects and deliverables
- A cleaner data model for operational ownership and delivery status
- Custom dashboard views for the team
- Migration plan from Airtable to the new CRM
- Coexistence period so the team could validate the new system while work continued
- Known-issues register and decision log
- SOPs and handoff documentation

## Architecture

```text
Intake / existing records
        |
        v
Data cleanup and schema mapping
        |
        v
Custom CRM data model
        |
        +--> Client and brand views
        +--> Project delivery views
        +--> Deliverable ownership views
        +--> Status and risk visibility
        |
        v
Team rollout, SOPs and adoption support
```

See [architecture.md](architecture.md) for the expanded model.

## Design Decisions

**Migration as a coexistence period, not a single switch.** The old and new systems
ran together long enough to discover hidden assumptions and missing workflow states.

**Schema before screens.** The team did not need a prettier Airtable. It needed the
real entities and relationships made explicit.

**Documentation was part of delivery.** SOPs, decision logs and known issues were
created so the system could keep running after handoff.

## Results

- Replaced the Airtable workflow for a 12-person team
- Centralized visibility across clients, brands, projects and deliverables
- Created a system that stayed in daily use after contract end

## What Was Sanitized

This public case study removes:

- client and brand names;
- real records;
- internal URLs;
- production database IDs;
- screenshots with private information;
- exact business rules that are not safe to publish;
- production git history.

See [privacy.md](privacy.md) for the full sanitization notes.

## What Reviewers Can Evaluate

- How the migration was framed
- How the data model was simplified
- How rollout risk was handled
- How private production work can be made reviewable without exposing confidential data

## Project documentation

Read the delivery evidence as a case study:

- [Project brief](docs/project-brief.md)
- [Delivery plan](docs/delivery-plan.md)
- [Risk and decision register](docs/risk-and-decisions.md)
- [Status report](docs/status-report.md)
- [Close-out report](docs/close-out-report.md)

The [documentation index](docs/README.md) explains how the artefacts fit together.
