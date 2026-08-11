# Privacy And Sanitization Notes

This is a sanitized public case study of a private production system.

## Removed

- Real client names
- Real brand names
- Production records
- Internal URLs
- Supabase or database identifiers
- Airtable base, table and field IDs
- Screenshots with private information
- Slack channels or user names
- Production source code
- Production git history
- Exact business rules that create competitive or client risk

## Replaced With

- Mock client and brand names
- Representative schema fields
- Simplified workflow diagrams
- Sample records that preserve shape but not content
- Public-facing explanation of decisions and tradeoffs

## Why The Full Code Is Not Public

The production CRM contains client context, workflow logic and integration details
that are not appropriate for a public repository. Publishing the real repository
would create unnecessary privacy and business risk.

This public version exists so a reviewer can still evaluate the work: the migration
thinking, system architecture, rollout judgment and documentation discipline.

## Safe Review Boundary

The public case study is safe to inspect, quote and share. It should not be treated
as a runnable copy of the production CRM.

