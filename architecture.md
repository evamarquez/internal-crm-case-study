# Architecture

This is a sanitized model of the CRM migration. Names and fields are representative,
not copied from production.

## Core Entities

```text
Client
  id
  name
  status
  owner

Brand
  id
  client_id
  name
  market
  lifecycle_stage

Project
  id
  brand_id
  type
  status
  delivery_owner
  due_date

Deliverable
  id
  project_id
  title
  status
  assignee
  blocker
  last_updated
```

## Workflow Shape

```text
Intake
  -> client and brand created
  -> delivery scope defined
  -> project records generated
  -> deliverables assigned
  -> team works from role-specific views
  -> status and blockers reviewed
  -> completed work archived or moved into reporting
```

## Migration Approach

1. Map the existing Airtable base and identify fields that were actually process
   states.
2. Separate real entities from convenience views.
3. Define the target schema.
4. Build the first dashboard around the team's highest-frequency workflows.
5. Run Airtable and the CRM in parallel.
6. Capture missing assumptions in a known-issues register.
7. Update SOPs and handoff docs.
8. Move the team fully once the new system covered daily work.

## Risk Controls

| Risk | Control |
|---|---|
| Hidden workflow rules | Coexistence period and user feedback loop |
| Data mismatch | Schema mapping before migration |
| Team rejection | Role-specific views instead of generic admin screens |
| Lost operational context | Decision log and SOPs |
| Incomplete handoff | Known-issues register and ownership notes |

## Why This Was Not Just A Database Move

The previous tool was carrying process, ownership and team memory. Moving records
without redesigning the operating model would have recreated the same problems in a
new interface.

The migration succeeded because the system was built around how the team actually
worked, not around the shape of the old tables.

